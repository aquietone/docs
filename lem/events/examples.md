# Text Event Examples

=== "Run away on Aten Ha Ra silence emote"

    ```lua
    -- Provides access to MQ functions
    local mq = require('mq')

    -- The zone to be in for the event to be handled
    local required_zone = 'vexthaltwo_mission'

    -- The location to run away to
    local run_away_loc = {
        x=1222.67,
        y=-48.97,
        z=236.41,
    }
    -- The time to wait before returning to the group (15000 is 15 seconds)
    local return_delay = 15000

    local function run_away()
        local my_class = mq.TLO.Me.Class.ShortName()
        -- pause all the things
        mq.cmdf('/%s mode 0', my_class)
        mq.cmd('/mqp on')
        mq.cmd('/twist off')
        mq.cmd('/timed 5 /afollow off')
        mq.cmd('/nav stop')
        mq.cmd('/target clear')
        -- run away
        mq.cmdf('/timed 10 /nav locxyz %d %d %d', run_away_loc.x, run_away_loc.y, run_away_loc.z)
        -- resume all the things
        mq.delay(return_delay)
        mq.cmdf('/%s mode 2', my_class)
        mq.cmd('/mqp off')
        mq.cmd('/twist on')
    end

    local function event_handler(line, target)
        if not mq.TLO.Zone.ShortName() == required_zone then return end

        local i_am_ma = mq.TLO.Group.Member(0).MainAssist()
        local my_name = mq.TLO.Me.CleanName()
        local ma_name = mq.TLO.Group.MainAssist.CleanName()

        -- run away if i am targeted and i am not the MA, or if the MA is targeted and i am not the MA
        if (target == my_name and not i_am_ma) or (target == ma_name and not i_am_ma) then
            run_away()
        end
    end

    return {eventfunc=event_handler}
    ```