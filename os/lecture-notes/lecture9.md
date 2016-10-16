# Lecture 9 (13/10/2016)

## Automatic recognition of devices

Nowadays, automatic HW recognition and insertion and removal of devices is very important.
Each device driver keeps a list for which devices and types it is responsible.
All device-related information available to user space via `/sys` virtual filesystem.

Steps:

- At boot time, kernel probes devices, which respond with unique id indicating vendor and device type
- For each device found, kernel sends info to userspace
- Special program in userspace (`udev`) generates entry in `/dev` and loads appropriate module

## sys virtual fs (aside)

`sys` is a filesystem representation of the system's device tree.
In addition to `/proc`, the kernel exports information to the `/sys` virtual file system (sysfs).
Programs such as the dynamic device manager, `udev`, use `/sys` to access device and device driver information.

## Device management (aside)

### Device files

The `/dev` directory contains *device files* (also sometimes known as device special files and device nodes)
that provide access to peripheral devices such as hard disks, to resources on peripheral devices such as disk partitions,
and pseudo devices such as a random number generator.

The directory has several subdirectory hierarchies, each of which holds device files that relate to a certain type of device.
The device files in subdirectories such as these are actually implemented as symbolic links to device files in `/dev`.

#### Types of devices (revisited):

- **Block devices** support random access to data, seeking media for data, and usually allow data
to be buffered while it is being written or read (e.g. hard disks, CD-ROMs etc...).

- **Character devices** support streaming of data to or from a device, and data is not usually buffered nor is random access permitted to data on a device (e.g. keyboard, mice, terminals etc...).

- **Pseudo**

Some special devices are:

- `/dev/null` is a data sink. Data that you write to `/dev/null` effectively disappears but the write operation succeeds. Reading from `/dev/null` returns `EOF`.
- `/dev/zero` is a data source of an unlimited number of zero-value bytes.
- `/dev/random` and `/dev/urandom` are data sources of streams of pseudo-random bytes.

### `udev` device manager

The `udev` device manager dynamically creates or removes device node files at boot time or if you add a device to or remove a device from the system with a 2.6 version kernel or later.
When creating a device node, udev reads the device's `/sys` directory for attributes such as the label, serial number, and bus device number.

## Handling interrupts in device drivers

