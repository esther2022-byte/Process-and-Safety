# State machine
```plantuml
@startuml  state_machine 
skinparam backgroundColor transparent
left to right direction
component valve_assembly
 {
  state_0 [PLC_idle] [robot_idle]
  PLC_idle -> state_1 [pLC_check_component]-> [sensor detected]-> () red_light_on signal_for_robot
  state_2 [robot_start]-> [robot_finish]->[valve_assembly_completed]->()red_lamp_off-> state_0

}
