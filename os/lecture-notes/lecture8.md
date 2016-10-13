# Lecture 8 (12/10/2016)

## Concurrency issues in the kernel (see slides + book)

## Device drivers

The keyboard, mouse and serial ports are controlled by a SuperIO chip, the IDE disks by an IDE controller, SCSI disks by a SCSI controller and so on. Each hardware controller has its own control and status registers (CSRs) and these differ between devices.

The software that handles or manages a hardware controller is known as a device driver.
The Linux kernel device drivers are, essentially, a shared library of privileged, memory resident, low level hardware handling routines. It is Linux's device drivers that handle the peculiarities of the devices they are managing.

All hardware devices look like regular files; they can be opened, closed, read and written using the same, standard, system calls that are used to manipulate files. Every device in the system is represented by a device special file, for example the first IDE disk in the system is represented by /dev/hda.

The system calls associated to each device driver are:

- open: make device available
- read: read from device
- write: write to device
- ioctl: Perform operations on device
- close: make device unavailable

Linux supports three types of hardware device:

- character
- block and
- network

From the kernel side we have that each device driver file may have functions associated with it which
are called when corresponding syscalls are made.

### Interfacing functions between user space and kernel space

The kernel offers several subroutines or functions in user space, which allow the end-user application programmer to interact with the hardware. Usually, in UNIX or Linux systems, this dialogue is performed through functions or subroutines in order to read and write files.

On the other hand, in kernel space Linux also offers several functions or subroutines to perform the low level interactions directly with the hardware, and allow the transfer of information from kernel to user space.

Usually, for each function in user space (allowing the use of devices or files), there exists an equivalent in kernel space (allowing the transfer of information from the kernel to the user and vice-versa).

### Implementing a device driver (see references + book + material)

## References

- http://freesoftwaremagazine.com/articles/drivers_linux/?
- http://www.tldp.org/LDP/tlk/dd/drivers.html
