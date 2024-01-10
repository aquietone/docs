# TLO

LEM settings can be accessed via the `LEM` TLO:  

| DataType     | Member    | Type         | Description                                                        | Example                             |
|--------------|-----------|--------------|--------------------------------------------------------------------|-------------------------------------|
| LEMType      | ToString  | string       | Output the current version of LEM which is installed               | /echo ${LEM}                        |
|              | Frequency | int          | Output the frequency which the main LEM loop runs events           | /echo ${LEM.Frequency}              |
|              | Broadcast | string       | Output the broadcast channel used to announce event enable/disable | /echo ${LEM.Broadcast}              |
|              | LogLevel  | string       | Output the current log level for events                            | /echo ${LEM.LogLevel}               |
|              | Event     | LEMEventType | Access the event with the specified name                           | /echo ${LEM.Event[event1]}          |
|              | React     | LEMReactType | Access the react with the specified name                           | /echo ${LEM.React[react1]}          |
| LEMEventType | ToString  | string       | Output the name and enabled status of the event                    | /echo ${LEM.Event[event1]}          |
|              | Enabled   | bool         | Output whether the event is currently enabled                      | /echo ${LEM.Event[event1].Enabled}  |
|              | Category  | string       | Output the category which the event belongs to                     | /echo ${LEM.Event[event1].Category} |
|              | Pattern   | string       | Output the pattern string of the event                             | /echo ${LEM.Event[event1].Pattern}  |
| LEMReactType | ToString  | string       | Output the name and enabled status of the event                    | /echo ${LEM.React[react1]}          |
|              | Enabled   | bool         | Output whether the event is currently enabled                      | /echo ${LEM.React[react1].Enabled}  |
|              | Category  | string       | Output the category which the named event belongs to               | /echo ${LEM.React[react1].Category} |