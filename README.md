# Dumb8-CPU

Continuing my exploration of the lower-level world...

This project is the implementation of a CPU in a high-level language, C. It aims to have a reduced (minimalist) instruction set and still be Turing complete.

## How to test

You can run a test program like that. I'll try making a developer's manual so one can make its own programs using the custom assembly here. 

```
make
./dumb8 program.asm
```

## Technical specifications

- 8-bit processing unit
- RISC (reduced instruction set computer)
- 4 general purpose registers (labeled R0 to R3)
- 1 input port, 1 output port (via getchar and putchar)
- Turing-completeness: bitwise and arithmetic operations

## Instruction set reference (for programmers)

```
; Move register RY to register RX
MOV RX, RY 

; Arithmetic addition and substraction stored in RX
ADD RX, RY
SUB RX, RY

; Bitwise operations stored in RX
OR RX, RY
AND RX, RY
XOR RX, RY

; Output RX to screen
OUT RX

; Input RX from keyboard
IN RX

; Jump to memory offset ADDR (decimal)
JMP ADDR

; Jump to memory offset ADDR (decimal) if equal flag is set by previous comparison
JEQ ADDR

; Compare RX and RY, sets equal flag if true
CMP RX, RY

; No operation; does nothing
NOP

; Halts the processing unit
HLT

```
