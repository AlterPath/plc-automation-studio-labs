# B&R PLC in Automation Studio

[Русская версия](README.md)

A lab for the course on software for mechatronic and robotic systems (October 2025): a C program for a B&R controller in Automation Studio, debugged in the PLC simulator.

## What the program does

The cyclic task (`Laba_1/Logical/Program/Cyclic.c`) models two DC motors and compares two ways of controlling them:
- **the first motor** runs open-loop: the voltage is set proportionally to the speed setpoint;
- **the second motor** runs under a controller (`FB_Regulator`) that receives the error between the setpoint and the actual speed.

The setpoint changes as a step: speed 40 at cycle 200, reset to 0 at cycle 400. Variable traces in Automation Studio show how both motors follow the step.

`Init.c` and `Exit.c` handle program initialization and shutdown; the motor and controller function blocks are defined in the project libraries.

## Quick start

Open `Laba_1/LABA1.apj` in B&R Automation Studio and run the configuration in the simulator (ARsim).

## Tech stack

C, B&R Automation Studio, Automation Runtime (ARsim).

## License

[MIT](LICENSE)
