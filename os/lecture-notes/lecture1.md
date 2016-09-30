# Lecture 1 (27/09/2016)

## What is an OS

An OS is a program that acts as middleware between the hardware and the applications.

Layers of a computer system:
- Hardware
- OS (composed of kernel, system programs - which are not part of the kernel - and application programs)
- Applications
- Users

We have 2 definitions of OS:
- OS as a resource allocator -> manages all resources and resolves conflicts arising from requests to the same resource
- OS as a control system -> controls execution of programs and ensures that the right level of security is guaranteed (e.g. secure access to OS-reserved memory)

## Computer system operation

The first program to run on a computer is the *bootstrap program* (small) typically stored in ROM or EEPROM. It initializes all aspects of a OS (e.g loading into main memory the kernel).

### Interrupts

The occurrence of an event is usually signalled by an interrupt generated from hardware (via the system bus) or software (via system/monitor calls).
When the CPU is interrupted it transfers control to a fixed location which contains the code of the interrupt handler (service routing for the interrupt).
The interrupt service routine executes; on completion, the CPU resumes the interrupted computation.

## Storage (see CSA stuff)


