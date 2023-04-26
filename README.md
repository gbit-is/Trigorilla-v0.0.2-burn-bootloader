# How to burn a bootloader to the Trigorilla v0.0.2 board

## Why ?
I have an anycubic chiron 3D printer, depending on the factory version the mainboard either has a bootloader pre-installed or not.
I wanted to try out alternitive firmware but first I needed a bootloader on the mainboard to be able to do so.
It took me several hours to hunt down all the info I needed and I wanted to make it more accessable 

## Parts list:
- Trigorilla v0.0.2 board
- Computer with Arduino IDE installed
- Arduino Uno
- Usb Cable
- 5 female-to-female jumper wires
- 1 female-to-male jumper wire 
- A reason to do this 

### Disclaimer:
If you don't know what you are doing, don't do this.  
If you burn the bootloader but don't know what to do next, you could potentially brick your printer.  
You have been warned


## Steps:

1. Connect the arduino uno to your computer and run the arduino IDE
2. Set Arduino IDE settings: Board: "Arduino uno"
3. In arduino IDE: File -> Examples -> 11.Arduino ISP -> ArduinoISP
4. Upload sketch to your arduino uno
5. disconnect your arduino uno
6. Hook up your arduino uno to the trigorilla board according to the graph
7. Reconnect the arduino to your PC
8. Set Arduino IDE settings: 
  - Board: "Arduino Mega or Mega 2560"
  - Processor: "Atmega 2560 (Mega 2560)"
  - Programmer: "Arduino as ISP"
9. In arduino IDE: tools -> Burn Bootloader

This should result in a bootloader being burned to your Trigorilla v0.0.2 board


![Connection diagram](https://raw.githubusercontent.com/gbit-is/Trigorilla-v0.0.2-burn-bootloader/main/connection_export.png)

