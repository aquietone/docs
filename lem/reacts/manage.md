# Manage Condition Events

## Adding a new Condition Event

1. Select `Condition Events` and click `Add Event...` and a new window will appear.  
2. Enter a name for the new event.  
3. Optionally, set a category for the event.  
4. Implement the `condition` function for the new event. The condition function should return a result which can be evaluated to a boolean value, `true` or `false`. If the condition function result evaluates to `true`, then the `action` function will be called. If the condition function evaluates to `false`, then the action function will not be called. Note that in addition to `true` and `false`, `nil` is also considered to be `false` and any other non-nil and non-boolean value is considered to be `true`. Unlike other languages, the number `0` would also evaluate to `true`.  
5. Implement the `action` function for the new event. The `action` function is called when the condition function returns a result which evaluates to `true`, and should perform whatever action you want to be taken when the condition is satisfied.  
6. Optionally, also implement the `on_load` function if you would like any actions to be performed immediately upon the event being enabled.  
7. Click `Save` to save the new event.  

## Editing Condition Events

1. Select `Condition Events` and find the event you wish to edit.  
2. Select the event and click the `Edit` button.  
3. Make updates to the event in the new window that appears, and then click `Save`.  

## Viewing Condition Events

1. Select `Condition Events` and find the event you wish to edit.  
2. Double click the event you wish to view and a new event viewer window will appear.  

## Removing Condition Events

1. Select `Condition Events` and find the event you wish to edit.  
2. Select the event and click the `Remove` button.  

## Toggling Events

Events can be enabled or disabled for a given character.  

### Using the UI

1. Select `Condition Events` and find the event you wish to edit.  
2. Check or uncheck the box next to the event name to toggle the event.  

### Using the Command Line

- Run the command `/lem cond event_name 0` to disable the event named `event_name`.  
- Run the command `/lem cond event_name 1` to enable the event named `event_name`.  