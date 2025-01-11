# Table Top Pong Controller

The controller/ directory of the project includes the source code for the controller for the Table Pong Game. The controller uses a CH32V003 as the main microcontroller and communicates with the main board via UART through a cable connected between the controller and the main board.

Ideally the controller will end up having a 2 or 4 layer PCB designed to support the microcontroller and the buttons.

# ch32v003Fun
The ch32v003fun project was used to compile and flash the ch32v003. I am hoping to use direct register access for some of the tasks, but it is very likely that I will use some of the convinient APIs provided by the project.

## TODO
# Software Design
- Placeholder

# Hardware Design
- Placeholder

## WSL Setup
To use the debugger in WSL, the following steps must be performed:
1. Open a PowerShell prompt as administrator
2. Find out the busid of the programmer
```
usbipd list
```
3. Attach the usb device to wsl
```
usbipd attach --wsl --busid <busid>
```
3. Bind the device to wsl
```
usbipd bind --busid <bus id> --force
```

## Debugger Setup
Use the following connections between the debugger and the development board.
```
+===============================+
| Debugger  | Development board |
| 3V3       | VCC               |
| GND       | GND               |
| SWDIO     | PD1               |
+===============================+
```

## Build and Flash
Building is flashing is done with the same make command.
1. Navigate to the controller_src directory.
2. Run `make` to build and flash the ch32v003.

