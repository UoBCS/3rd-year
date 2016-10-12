# Lecture 7 (11/10/2016)

## Linux Kernel programming

The kernel has access to all resources and is not subject to any memory consraints. Faulty kernel programs can cause the computer to crash.

The kernel provides its functions only via special functions called system calls.
OSs have strict separation of kernel data and data for user programs. There is a need for explicit copying between user program and kernel:
`copy_from_user` and `copy_to_user` are used for this purpose.

In addition to syscalls kernels have **interrupts** (kernel asks HW to perform an operation, HW sends interrupt to the CPU which calls a interrupt handler routine in the kernel). The interrupt code
must be small and quick (no sleep).

Any code running in process context may be pre-empted at any time by an interrupt. Interrupts also have priority; high priority interrupts can preempt low priority ones.

## Kernel modules (see examples in material)

Kernel modules are the mechanism by which the Linux kernel can load and unload object code on demand.

Support for modules allows systems to have only a minimal base kernel image, with optional features and drivers supplied via loadable, separate objects.

Commands to manage modules:

- `modprobe` or `insmod`: inserts a module into running kernel
- `rmmod`: removes module from running kernel
- `lsmod`: lists currently running modules
- `modinfo`: gets module info
