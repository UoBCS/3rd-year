# Lecture 3 (30/09/2016)

## OS services

One set of OS services provides functions that are helpful to the user:

- User interface
- Program execution: The system must be able to load a program into memory and to run that program
- I/O operations
- FS manipulation
- Communications: There are many circumstances in which one process needs to exchange information with another process. It may be implemented via shared memory or through message passing.
- Error detection

Another set of OS functions exists not for helping the user but rather for ensuring the efficient operation of the system itself:

- Resource allocation
- Accounting: We want to keep track of which users use how much and what kinds of computer resources.
- Protection and security: When several separate processes execute concurrently, it should not be possible for one process to interfere with the others or with the OS itself.

## System calls

System calls are a collection of functions that form a programming interface to the services provided by the OS. 
They are typically written in a high level language. They are mostly accessed by programs via a high-level Application
Program Interface (API) rather than direct system call.

Three general methods are used to pass parameters to the OS. The simplest approach is to pass the parameters in registers.
In some cases, however, there may be more parameters than registers. In these cases,
the parameters are generally stored in a block, or table, in memory, and the address of the block is passed as a parameter in a register


