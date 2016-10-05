# Lecture 4 (04/10/2016)

## Mechanisms and policies

One important principle is the separation of **policy** (what will be done) from **mechanism** (how to do something).
This separation is important for flexibility. Policies are likely to change across places or over time.

Microkernel-based OS take this separation to one extreme by implementing a basic set of primitive building blocks. These block are almost policy free, allowing
more advanced mechanisms and policies to be added via user-created kernel modules or user programs themselves.

## OS structure

A common approach is to partition the task into small components /modules, rather than have one monolithic system.

### Simple structure

Some systems start small, simple, and limited systems and then grew beyond their original scope. This is the case of MS-DOS.

![MS DOS architecture](https://github.com/UoBCS/3rd-year/blob/master/os/lecture-notes/assets/lecture4-msdos.png)

In MS-DOS, the interfaces and levels of functionality are not well separated. For instance, application programs are able
to access the basic I/O routines to write directly to the display and disk drives. Such freedom
leaves MS-DOS vulnerable to malicious/errant programs, causing entire system crashes when user programs fail.

![Traditional UNIX system structure](https://github.com/UoBCS/3rd-year/blob/master/os/lecture-notes/assets/lecture4-unix.png)

Another example of limited structuring is the original UNIX OS. It consists of 2 separable parts: the kernel and the system programs.
The kernel is further separated into a series of interfaces and device drivers.
This monolithic structure was difficult to implement and maintain.

### Layered approach

OS can be broken into pieces/layers that are smaller and more appropriate that those allowed by the original MS-DOS and UNIX systems.
A system can be made modulary in many ways. One method is the **layered approach**, in which the OS is broken into a number of layers (0 to N where 0 is the hardware).
The main advantage is simplicity of construction and debugging.
One layer can only use lower-level layers services.

### Microkernels

This method structures the OS by removing all nonessential components from the kernel and implementing them as system and user-level programs. The result is a smaller kernel.
Typically microkernels provide minimal process and memory management, in addition to a communication facility.

The main function of the MK is to provide communication between the client program and the various services that are also running in user space.
Communication is provided through message passing.

One benefit of MKs is that they make extending the OS easier. Unfortunately, the performance of MK can suffer due to increased system-function overhead.

### Modules

Perhaps the best current methodology for OS design involves usingo **loadable kernel modules**. Here, the kernel has a set of core components and links in additional services via modules,
either at boot time or during tun time (modern UNIX, Solaris, Linux, Mac OS X, Windows).

The idea of the design is for the kernel to provide core services while other services are implemented dynamically, as the kernel is running.
Linking services dynamically is preferable to adding new features directly to the kernel, which would require recompiling the kernel every time a change was made.

### Virtual machines

The fundamental idea behind a virtual machine is to abstract the hardware of a single computer into several different execution environments.
