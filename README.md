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
Why do we have these registers?
* They are much faster than memory, especially because they are located inside the CPU. Accessing a memory location requires the use of a system bus, so it takes much longer. Accessing data in a register usually takes no time. Therefore, you should try to keep variables in the registers. register sets are very small and most registers have special purposes which limit their use as variables, but they are still an excellent place to store temporary data of calculations.

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





## References
[emu8086 documentation](https://emu8086-microprocessor-emulator.en.softonic.com/)
