# State machine
```plantuml
@startuml  state machine 
skinparam backgroundColor transparent
left to right direction
component valve_assembly
state "PLC Idle" as state0 {
  [*] --> PLC_IDLE : Start
  PLC_IDLE --> PLC_CHECK_COMPONENT : Trigger
}

state "Check Component" as state1 {
  PLC_CHECK_COMPONENT --> SENSOR_DETECTED : Component Detected
  SENSOR_DETECTED --> RED_LAMP_ON : Trigger
}

state "ABB Program" as state2 {
  RED_LAMP_ON --> ABB_PROGRAM_STARTED : Trigger
  ABB_PROGRAM_STARTED --> ABB_PROGRAM_COMPLETED : Program Completed
  ABB_PROGRAM_COMPLETED --> RED_LAMP_OFF : Trigger
  RED_LAMP_OFF --> PLC_IDLE : Process Complete
  PLC_IDLE --> [*] : Back to PLC Idle
}
