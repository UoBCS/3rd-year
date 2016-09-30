# Lecture 2 (29/09/2016)

## GPU architecture

A GPU consists of a max number of CUDA cores. These CUDA cores are split across n Streaming Multiprocessors (SM) each SM consisting of 32 CUDA cores. The GPU has memory.
Each CUDA core consists of an ALU and an FPU (Floating Point Unit).

Each core can execute a sequential thread, but the cores execute in what NVIDIA calls SIMT (Single Instruction, Multiple Thread) fashion; all cores in the same group execute the same instruction at the same time.

The code is actually executed in groups of 32 threads, what NVIDIA calls a warp.

## Compiling for CUDA (nvcc)

The host CPU and the GPU (device) are separate and connected by a communication path. We need to generate separate code for both devices.
nvcc takes a C or C++ program with NVidia extensions, compiles
the GPU Device code, extracts the Host code and passes it to the
local host compiler to be compiled.

The single resulting binary contains both the host and the device binary, which is downloaded to the device from the host when the program runs.

## CUDA thread execution model

Each kernel function is executed in a grid of threads. This grid is divided into blocks also known as thread blocks and each block is further divided into threads.

As said, threads are grouped into blocks, and blocks are grouped into a grid. Each thread has a unique local index in its block, and each block has a unique index in the grid. Kernels can use these indices to compute array subscripts, for instance.

(See warps section)

## Programming in CUDA

### Kernels

We have to identify whether a function runs on the host, the device or both, and where it is callable from:

- the host: `__host__ void f(...)`
	* This is default
	* Callable from the host only

- the device: `__global__ void f(...)`
	* Kernel functions that, when called, are executed N times in parallel by N different CUDA threads
	* Callable from the host only hence this is how the host gets to run code on the GPU

- the device: `__device__ void f(...)`
	* Callable from the device only. Hence they are helper function available to kernel functions and other device functions on the GPU

- both: `__host__ __device__ void f(...)`
	* The host can not call the device version or vice versa

## CUDA getting started exercise

`deviceQuery` output values explained:

- CUDA Capability Major/Minor version number: The compute capability of a device is represented by a version number, also sometimes called its "SM version". This version number identifies the features supported by the GPU hardware and is used by applications at runtime to determine which hardware features and/or instructions are available on the present GPU.

- Total amount of global memory: global memory, which resides in device DRAM, can be used for transfers between the host and device as well as for the data input to and output from kernels. The name global here refers to scope, as it can be accessed and modified from both the host and the device.

- Number of multiprocessors and cores: NVIDIA GPUs have a number of multiprocessors, each of which executes in parallel with the others. A Kepler multiprocessor has 12 groups of 16 stream processors.

- Shared memory: Because it is on-chip, shared memory is much faster than local and global memory. In fact, shared memory latency is roughly 100x lower than uncached global memory latency (provided that there are no bank conflicts between the threads, which we will examine later in this post). Shared memory is allocated per thread block, so all threads in the block have access to the same shared memory. Threads can access data in shared memory loaded from global memory by other threads within the same thread block.

- Warp size: number of threads running concurrently on an MP

