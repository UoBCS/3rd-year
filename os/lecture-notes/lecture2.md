# Lecture 2 (28/09/2016)

## Fault handling and protection

Events are almost always signaled by the occurrence of an interrupt or a trap.
A *trap* is a software generated interrupt caused either by an error (e.g. division by zero) or by a user program to request OS services.
A properly designed OS must ensure that an incorrect program must not affect the execution of other programs.

### Dual mode operation

To separate OS code from user code OSes use dual mode operation:
- Kernel mode
- User mode

## Process management

A process is a program in execution (active != program which is passive). Processes need various resources throughout their job and it is up to the OS to manage them.
There are 2 kinds of processes: system processes and user processes.
All processes can execute concurrently (e.g. by multiplexing on a single CPU).

OS is responsible for the following in regards to process management:
- Scheduling processes and threads on the CPU
- Creating and deleting processes
- Suspending and resuming processes
- Providing mechanisms for process synchronisation
- Providing mechanisms for process communication

## Memory management

## Storage management
