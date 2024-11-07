# 8x128 LED Matrix Display Controller

## Project Overview
This project involves programming a microprocessor to control an 8x128 LED matrix display, capable of showing characters and custom animations stored in buffer memory. It is part of the GEL445 Microprocessors course, showcasing low-level programming and hardware interface skills.

## Features
- Display of alphanumeric characters on an 8x128 LED matrix.
- Use of multiple 74LS373 latches for column selection.
- Dynamic character and animation display via buffer memory.
- Efficient handling of I/O operations with assembly programming.

## Hardware Components
- Microprocessor (Generic model used for educational purposes)
- 8x128 LED matrix display
- 74LS373 latches for output and selection control
- Basic interfacing hardware (wires, resistors, breadboard)

## Software and Tools
- Assembly language (specific to the microprocessor model used)
- Programming toolchain that supports assembly compilation and direct hardware interfacing

## Installation
Clone this repository to your local machine:


## Usage
To run this project, load the assembly code into the microprocessor's memory, ensuring that all hardware connections are correctly set up according to the project schematics. Details for running simulations or actual hardware testing are provided in the supplementary project documentation.

## Code Snippet
Here is a brief excerpt from the main control logic implemented in assembly:
```asm
ORIGIN 0050:0050H
COL1:	DB FF;0 
        DB 00;1
        ... (additional data definitions)
ORIGIN 0050:0400H 
	DB 00; BUFFER MEMORY
        ... (additional buffer definitions)

START:	MOV BX,0050H;BX POINT TO START OF TABLE
        MOV AH,00H;HIGH BYTE = 0
        ... (code continues)
