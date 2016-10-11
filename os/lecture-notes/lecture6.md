# Lecture 6 (07/10/2016)

## Memory management in the Linux Kernel

We have four segments in total:

- Kernel code
- Kernel data
- User code
- User data

Paging is used as described in lecture 5.

## Kernel memory and user memory

When a process running in user rnode requests additional memory/ pages
are allocated from the list of free page frames maintained by the kernel.

Kernel memory/ however is often allocated from a free-memory pool
different from the list used to satisfy ordinary user-mode processes. There
are two primary reasons for this:

1. The kernel requests memory for data structures of varying sizes, some of which are less than a page in size. Therefore the kernel must use the memory conservatively.
2. Certain hardware devices interact directly with physical memory-without the benefit of a virtual memory interface and consequently may require memory residing in physically contiguous pages.

There are two strategies for managing free memory
that is assigned to kernel processes: the "buddy system" and slab allocation.

### Buddy system

The buddy system allocates memory from a fixed-size segment consisting of
physically contiguous pages. Memory is allocated from this segment using a
power-of-2 allocator, which satisfies requests in units sized as a power of 2.

![Buddy system allocation](https://github.com/UoBCS/3rd-year/blob/master/os/lecture-notes/assets/lecture6-buddy-system.png)

Using **coalescing** we can merge two adjacent buddies to form larger segments.

### Slab allocation

A **slab** consists of is made up of one or more physically contiguous pages. A **cache** consists of one or more slabs.
There is a single cache for each unique kernel data structure.
Each cache is populated with objects that are instantiations of the kernel data structure the cache represents.
