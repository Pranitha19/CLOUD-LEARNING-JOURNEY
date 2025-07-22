## Topics i have covered:

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

## Storage-Device Hierarchy:

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

**Heap** containing memory dynamically allocated during run time

<img width="237" height="381" alt="image" src="https://github.com/user-attachments/assets/a5f49677-e668-4989-bbfb-ef76ae14c8c5" />


<img width="237" height="381" alt="image" src="https://github.com/user-attachments/assets/5e32291f-dfe7-45e9-80b3-624af7f33e99" />


## Process State:

As a process executes, it changes state

new: The process is being created

running: Instructions are being executed

waiting: The process is waiting for some event to occur

ready: The process is waiting to be assigned to a processor

terminated: The process has finished execution


<img width="1024" height="575" alt="image" src="https://github.com/user-attachments/assets/d4e4f325-8ad1-485e-b2a1-1b785b6982c4" />


When CPU switches to another process, the system must save the state of the old process and load the saved state for the new process via a **context switch**

## Amdahl’s Law

Identifies performance gains from adding additional cores to an application that has both serial and parallel components

S is serial portion

N processing cores

That is, if application is 75% parallel / 25% serial, moving from 1 to 2 cores results in speedup of 1.6 times.

As N approaches infinity, speedup approaches 1 / S

Serial portion of an application has disproportionate effect on performance gained by adding additional cores

**SpeedUp <= 1 / ( s + ( (1-S) / N ) )**


## CPU Scheduling

Maximum CPU utilization
obtained with multiprogramming
CPU–I/O Burst Cycle – Process
execution consists of a cycle of
CPU execution and I/O wait
CPU burst followed by I/O burst
CPU burst distribution is of main
concern

**CPU Scheduler:**

Short-term scheduler selects from among the processes in
ready queue, and allocates the CPU to one of them
Queue may be ordered in various ways
CPU scheduling decisions may take place when a process:
1. Switches from running to waiting state
2. Switches from running to ready state
3. Switches from waiting to ready
4. Terminates
Scheduling under 1 and 4 is non-preemptive
All other scheduling is preemptive

**Dispatcher**

Dispatcher module gives control of the CPU to the process selected by the short-term scheduler; this involves:

switching context

switching to user mode

jumping to the proper location in the user program to restart that program

Dispatch latency – time it takes for the dispatcher to stop one process and start another running

## Scheduling Criteria

CPU utilization – keep the CPU as busy as possible

Throughput – # of processes that complete their execution per time unit

Turnaround time – amount of time to execute a particular process

Waiting time – amount of time a process has been waiting in the ready queue

Response time – amount of time it takes from when a request was submitted until the first response is produced, not output (for
time-sharing environment)


## Scheduling Algorithm Optimization Criteria

Max CPU utilization

Max throughput

Min turnaround time

Min waiting time

Min response time




## First- Come, First-Served (FCFS) Scheduling

Process   Burst Time

P1           24

P2            3

P3            3

Suppose that the processes arrive in the order: P1 , P2 , P3

The Gantt Chart for the schedule is:

    0            24           27          30

           P1           P2           P3

Waiting time for P1 = 0; P2 = 24; P3 = 27

Average waiting time: (0 + 24 + 27)/3 = 17P P P1 2 3
0 24 3027


Convoy effect - short process behind long process. This gives bettter waiting time . Means, we schedule P2 ,P3 then P1 as per burst time for better average wait time.


## Shortest-Job-First (SJF) Scheduling

Associate with each process the length of its next CPU burst. Use these lengths to schedule the process with the shortest time

SJF is optimal – gives minimum average waiting time for a given set of processes

The difficulty is knowing the length of the next CPU request Could ask the user

**Example of SJF**

Process        Arrival Time            Burst Time

P1                 0.0                      6

P2                 2.0                      8

P3                 4.0                      7

P4                 5.0                      3

SJF scheduling chart:

    0       3        9         16        24

        P4       P1       P3        P2


Average waiting time = (3 + 16 + 9 + 0) / 4 = 7


## Priority Scheduling:

A priority number (integer) is associated with each process

The CPU is allocated to the process with the highest priority (smallest integer - highest priority)

Preemptive

Nonpreemptive

SJF is priority scheduling where priority is the inverse of predicted next CPU burst time.

Problem : Starvation – low priority processes may never execute.

Solution : Aging – as time progresses increase the priority of the
process

**Example of Priority Scheduling**

Process     BurstTime      Priority
P1             10             3
P2              1             1
P3              2             4
P4              1             5
P5              5             2

Priority scheduling Gantt Chart:

    0        1         6        16        18       19

        P2        P5        P1       P3        P5
    
Average waiting time = 8.2 msec

## Round Robin (RR)

Each process gets a small unit of CPU time (time quantum q), usually 10-100 milliseconds. After this time has elapsed, the process is preempted and added to the end of the ready queue.

If there are n processes in the ready queue and the time quantum is q, then each process gets 1/n of the CPU time in chunks of at most q time units at once. No process waits more than (n-1)q time units. Timer interrupts every quantum to schedule next process Performance

q large  FIFO

q small  q must be large with respect to context switch, otherwise overhead is too high.

**Example of RR** with Time Quantum = 4

Process  Burst Time

P1            24

P2            3

P3            3

The Gantt chart is:

    0       4       7      10      14     18       22      26       30

        P1      P2      P3      P1      P1      P1      P1      P1

Typically, higher average turnaround than SJF, but better response

q should be large compared to context switch time

q usually 10ms to 100ms, context switch < 10 usec


## Rate Montonic Scheduling

A priority is assigned based on the inverse of its period

Shorter periods = higher priority;

Longer periods = lower priority

P1 = 50, t1 = 20. P2 = 100, t2= 35

P1 is assigned a higher priority than P2


## Earliest Deadline First Scheduling (EDF)

Priorities are assigned according to deadlines:

the earlier the deadline, the higher the priority;

the later the deadline, the lower the priority

P1 = 50, t1 = 25. P2 = 80, t2= 35


# Resources:

Operating System Concepts – 10th Edition  5.22 Silberschatz, Galvin and Gagne ©2018

https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.chegg.com%2Fhomework-help%2Fquestions-and-answers%2Fproblem-b-1-list-possible-transactions-five-process-states-diagram-process-state-provide-o-q30807826&psig=AOvVaw0A-_69Wz3XylxDPXCM6CoA&ust=1753283815271000&source=images&cd=vfe&opi=89978449&ved=0CBYQjRxqFwoTCNDqk67h0I4DFQAAAAAdAAAAABAE







