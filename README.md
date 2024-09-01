# Assembly Programming
To learn assembly language, you should first understand the basic concepts of computer systems.

<p align="center">
  <img src="https://github.com/ehsandastani/Assembly/blob/main/pics/model.gif?raw=true" alt="Computer system components">
</p>

the __system bus__ (shown in yellow) connects the various components of a computer.
The __CPU__ is the heart of the computer, most of computations occur inside the CPU.
__RAM__ is a place to where the programs are loaded in order to be executed.

## Inside the CPU
<p align="center">
  <img src="https://github.com/ehsandastani/Assembly/blob/main/pics/cpu.gif?raw=true" alt="CPU Registers">
</p>

As you can see, we have some types of registers inside the CPU.  

__Why do we have these registers?__
* They are much faster than memory, especially because they are located inside the CPU. Accessing a memory location requires the use of a system bus, so it takes much longer. Accessing data in a register usually takes no time. Therefore, you should try to keep variables in the registers. register sets are very small and most registers have special purposes which limit their use as variables, but they are still an excellent place to store temporary data of calculations. Additionally, we can use them to address memory.

### General Purpose Registers
The 8086 CPU has 8 general-purpose registers, each 16 bits in size. Each register has its own name:
 * __AX__ - The accumulator register (divided into __AH__ / __AL__).
 * __BX__ - The base address register (divided into __BH__ / __BL__).
 * __CX__ - The count register (divided into __CH__ / __CL__).
 * __DX__ - The data register (Devided into __DH__ / __DL__).
 * __SI__ - The source index register.
 * __DI__ - The destination index register.
 * __BP__ - The base pointer register.
 * __SP__ - The stack pointer register.

4 general purpose registers (AX, BX, CX, DX) are made of two separate 8 bit registers, for example if AX = <span style="color: red;">00110000</span><span style="color: blue;">00111001</span>b, then AH = <span style="color: red;">00110000</span>b and AL = <span style="color: blue;">00111001</span>b.  
Therefore, when you modify any of the 8 bit registers 16 bit register is also updated, and vice-versa. the same is for other 3 registers, "H" is for high and "L" is for low part.

### Segment Registers
* __CS__ - Code segment points to the segment address of memory where contains the current program.
    
    <p align="center">
        <img src="https://github.com/ehsandastani/Assembly/blob/main/pics/CS.png?raw=true" alt="CS Registers">
    </p>

* __DS__ - Data segment points to the segment address of memory where variables are defined.
    
    <p align="center">
        <img src="https://github.com/ehsandastani/Assembly/blob/main/pics/DS.png?raw=true" alt="DS Registers">
    </p>

* __SS__ - Stack segment points at the segment containing the stack.
    
    <p align="center">
        <img src="https://github.com/ehsandastani/Assembly/blob/main/pics/SS.png?raw=true" alt="SS Registers">
    </p>

* __ES__ - Extra segment register, it's up to a coder to define its usage.

 Although it is possible to store any data in the segment registers, this is never a good idea. The segment registers have a very special purpose - __pointing at accessible blocks of memory__. Segment registers work together with general purpose register to access any memory value.

### Special Purpose Registers
* __IP__ - The instruction pointer register points to currently executing instruction.

* __Flags register__ - Determines the current state of the microprocessor. Flags register is modified automatically by CPU after mathematical operations, this allows to determine the type of the result, and to determine conditions to transfer control to other parts of the program.

Generally you cannot access these registers directly, the way you can access AX and other general registers, but it is possible to change values of system registers using some tricks that you will learn a little bit later.


## Memory Access
To access memory we can use these four registers: __BX, SI, DI, BP__.

| Left Align | Center Align | Right Align |
|:-----------|:------------:|------------:|
| Row 1, Col 1 | Row 1, Col 2 | Row 1, Col 3 |
| Row 2, Col 1 | Row 2, Col 2 | Row 2, Col 3 |
| Row 3, Col 1 | Row 3, Col 2 | Row 3, Col 3 |












## References
[emu8086 documentation](https://emu8086-microprocessor-emulator.en.softonic.com/)
