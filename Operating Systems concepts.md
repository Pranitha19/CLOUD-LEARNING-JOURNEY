# Topics i have covered till now:

What Operating Systems Do
Computer-System Organization
Computer-System Architecture
Operating-System Operations
Process Management
Memory Management
Storage Management
Protection and Security :
     
# Protection: Controls access to system resources (like memory, files, devices) within the system by various processes and users.
#  Security: Protects the system from external threats like malware, unauthorized access, and attacks.


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



# Four Components of a Computer System

<img width="256" height="197" alt="image" src="https://github.com/user-attachments/assets/e04e8906-7449-4740-bcf4-dd0fc41fad8d" />


## # Computer System Organization ##

One or more CPUs, device controllers connect through common bus providing access to shared memory.   
Concurrent execution of CPUs and devices competing for  memory cycles.

I/O devices and the CPU can execute concurrently

Each device controller is in charge of a particular device type

Each device controller has a local buffer

CPU moves data from/to main memory to/from local buffers

Device controller informs CPU that it has finished its operation by causing an interrupt. Interrupt architecture must save the address of the interrupted instruction



<img width="566" height="381" alt="image" src="https://github.com/user-attachments/assets/0571a3f9-7977-4a8b-9e42-55a02828087a" />


<img width="255" height="198" alt="image" src="https://github.com/user-attachments/assets/a13ac75e-8e40-4559-b2cf-21040ebfd3ce" />

