** Topics i have covered till now:

What Operating Systems Do
Computer-System Organization
Computer-System Architecture
Operating-System Operations
Process Management
Memory Management
Storage Management
Protection and Security :
     
## Protection: 
Controls access to system resources (like memory, files, devices) within the system by various processes and users.

## Security: 
Protects the system from external threats like malware, unauthorized access, and attacks.


##  What is an Operating System and What Does it Do?

OS is a resource allocator - Manages all resources

Decides between conflicting requests for efficient and fair resource use

OS is a control program  - Controls execution of programs to prevent errors and improper use of the computer
 
OS is software that acts as an intermediary between users and computer hardware.

The one program running at all times on the computer” is -  the kernel

Functions:
Process Management
Memory Management
File System Management
I/O Management
Security and Protection



## Four Components of a Computer System

<img width="256" height="197" alt="image" src="https://github.com/user-attachments/assets/e04e8906-7449-4740-bcf4-dd0fc41fad8d" />


##  Computer System Organization 

One or more CPUs, device controllers connect through common bus providing access to shared memory.   
Concurrent execution of CPUs and devices competing for  memory cycles.

I/O devices and the CPU can execute concurrently

Each device controller is in charge of a particular device type

Each device controller has a local buffer

CPU moves data from/to main memory to/from local buffers

Device controller informs CPU that it has finished its operation by causing an interrupt. Interrupt architecture must save the address of the interrupted instruction



<img width="566" height="381" alt="image" src="https://github.com/user-attachments/assets/0571a3f9-7977-4a8b-9e42-55a02828087a" />


Computer storage, along with most computer throughput, is generally measured and manipulated in bytes and collections of bytes.

A kilobyte, or KB, is 1,024 bytes

a megabyte, or MB, is 1,0242 bytes

a gigabyte, or GB, is 1,0243 bytes

a terabyte, or TB, is 1,0244 bytes

a petabyte, or PB, is 1,0245 bytes

# Storage Structure

Main memory – only large storage media that the CPU can access directly

Random access memory (RAM) - Typically volatile
 
Secondary storage – extension of main memory that provides large nonvolatile storage capacity

Hard disks – rigid metal or glass platters covered with magnetic recording material

The disk controller determines the logical interaction between the device and the computer

Solid-state disks – faster than hard disks, nonvolatile. 
Becoming more popular

# Storage-Device Hierarchy:

Storage systems organized in hierarchy

Speed

Cost

Volatility

Caching – copying information into faster storage system; main memory can be viewed as a cache for secondary storage.

Important principle, performed at many levels in a computer (in hardware, operating system, software)

Cache smaller than storage being cached

<img width="255" height="198" alt="image" src="https://github.com/user-attachments/assets/a13ac75e-8e40-4559-b2cf-21040ebfd3ce" />

**Dual-mode** operation allows OS to protect itself and other system components

**User mode and kernel mode**

**Mode bit** provided by hardware

Provides ability to distinguish when system is running user code or kernel code

Some instructions designated as privileged, only executable in kernel mode

System call changes mode to kernel, return from call resets it to user


# Process Concept
An operating system executes a variety of programs:

Batch system – jobs

Time-shared systems – user programs or tasks

Process – a program in execution; process execution must progress in sequential fashion. Program is passive entity stored on disk (executable file), process is active

Program becomes process when executable file loaded into memory.

Execution of program started via GUI mouse clicks, command line entry of its name, etc. One program can be several processes

# Process in Memory

Multiple parts The program code, also called **text section**

**Stack section** containing temporary data Function parameters, return addresses,local variables

**Data section** containing global variables

**Heap*8 containing memory dynamically allocated during run time

<img width="237" height="381" alt="image" src="https://github.com/user-attachments/assets/a5f49677-e668-4989-bbfb-ef76ae14c8c5" />


<img width="237" height="381" alt="image" src="https://github.com/user-attachments/assets/5e32291f-dfe7-45e9-80b3-624af7f33e99" />











