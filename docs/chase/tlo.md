# TLO

Chase settings can be accessed via the `Chase` TLO:

| DataType     | Member         | Type      | Description                                       | Example                         |
|--------------|----------------|-----------|---------------------------------------------------|---------------------------------|
| ChaseType    | ToString       | string    | Output the current status                         | /echo ${Chase}                  |
|              | Paused         | bool      | Output whether the script is paused or running    | /echo ${Chase.Paused}           |
|              | Role           | string    | Output the chase role value                       | /echo ${Chase.Role}             |
|              | Target         | string    | Output the chase target value                     | /echo ${Chase.Target}           |
|              | ChaseDistance  | int       | Output the chase distance value                   | /echo ${Chase.ChaseDistance}    |
|              | StopDistance   | int       | Output the stop distance value                    | /echo ${Chase.StopDistance}     |