# Manage Text Events

![](../../images/lem/eventeditor.png)

## Adding a new Text Event

1. Select `Text Events` and click `Add Event...` and a new window will appear.  
2. Enter a name for the new event.  
3. Enter a pattern for the new event. The pattern can include `#*#` for wildcard matches or `#1#` for named matches. Named matches will be passed as arguments to the event handler function.  
4. Optionally, set a category for the event.  
5. Implement the handler function for the new event. Template code is provided, including a function `event_handler`. The function arguments should be updated to match the number of arguments matched in the event pattern. The first argument to the event handler is always the complete line which matched the pattern.  
6. Optionally, also implement the `on_load` function if you would like any actions to be performed immediately upon the event being enabled.  
7. Click `Save` to save the new event.

## Editing Text Events

1. Select `Text Events` and find the event you wish to edit.
2. Select the event and click the `Edit` button.
3. Make updates to the event in the new window that appears, and then click `Save`.

## Viewing Text Events

1. Select `Text Events` and find the event you wish to edit.
2. Double click the event you wish to view and a new event viewer window will appear.

## Removing Text Events

1. Select `Text Events` and find the event you wish to edit.
2. Select the event and click the `Remove` button.

## Toggling Events

Events can be enabled or disabled for a given character.

### Using the UI

1. Select `Text Events` and find the event you wish to edit.
2. Check or uncheck the box next to the event name to toggle the event.

### Using the Command Line

- Run the command `/lem text event_name 0` to disable the event named `event_name`.
- Run the command `/lem text event_name 1` to enable the event named `event_name`.