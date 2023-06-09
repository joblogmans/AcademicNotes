# Week 3
## Embedded operating systems
Operating System:
- intermediate software
- resource management
- provides an environment for executing applications

IoT OS:
- Vital functions:
	- Memory management
	- Processor management
	- Device management
	- File management

## Linux kernel functions and advantages
Processes:
- a program in execution
- linux uses a process descriptor containing:
	- run-state (running, waiting (interruptible and uninterruptible), stopped, zombie (stopped, but its resources have not yet been removed by the kernel))
	- address space
	- open files

Memory management
- linux uses virtual memory system
- memory addresses used by software are not the ones used for the hardware (but the kernel knows which belongs to what memory)
- large address space
	- allows for processes to allocate more memory than physical memory is available
- memory protection
- memory mapping
- fair physical memory allocation
- shared virtual memory

Scheduling
- defines running order of processes
- linux scheduler is a priority scheduler
- multi-processor systems there is one process queue per processor
- the scheduler allows for moving process queue content to a less busy processor

Interrupts
- -> event generated by hardware which changes the sequence of executed instructions
- Two categories:
	- Synchronous: produced by CPU's control unit (synchronous because the CPU control unit will only fire this one after completing the current instruction)
	- Asynchronous: produced by other hardware
- linux uses interrupt handlers (also known as Interrupt Service Routines)
	- main difference between interrupt handlers and other functions in the Kernel is that an interrupt handler is executed in a special context named Interrupt Context

## The microkernel
In the microkernel, many services are not ran in kernel mode and moved to the user space. This minimizes the kernel size.
The only things the kernel now does are:
- interrupt handling
- low-level process management
- message passing handling

Interprocess communication (IPC):
- IPC for exchanging information between processes
- IPC uses message registers from which the receiving process can be read
- IPC is synchronous, both processos have to agree on the moment of message passing
- IPC doesn't use intermediate buffers, thus improving performance

Advantages of microkernel:
- minimal kernel
- more secure (small trusted computing base)
- scalability
- extensibility

Disadvantages of microkernel:
- expensive context switching (going from kernel to user space and back)
- slower hardware reaction because of this
- waiting queue

## The modular kernel
- A sort of hybrid between monolithic kernel and microkernel.
- Comprises many modules, each dedicated to a specific task, only loaded when needed
- modules stay loaded until explicitly removed
- when used by multiple processes it creates copies of the module

advantages:
- reduces number of times for rebuilding a kernel
- diagnoses system problems easier
- only loads modules when needed -> reduces kernel's memory footprint
- increased overall performance while smaller size

disadvantages:
- possibility for instability
- security vulnerabilities
- might be hard to maintain if modules are made by multiple third-parties

## Introduction to Contiki
Open source OS with a Modular kernel for IoT. Built for networked and memory-constrained systems. Focused on low-power and IoT devices.

features:
- protothreads
- full TCP/IP networking
- Low-power standards are supported
- dynamic module loading
- power awareness
- running on low-power wireless devices
- possible to port existing code to new hardware
- Cooja network simulator to simulate IoT networks

## Introduction to TinyOS
- open source embedded OS
- monolithic kernel
- built for networked and memory-constrained systems and low power
- written in NesC:
	- separation of construction and composition
	- specification of component behaviour
	- bidirectional interfaces
	- statically linked components via interfaces
	- whole-program compiler

features:
- lightweight in space and time
	- small code footprint
	- low overhead of fine-grain modules
- simple scheduler based on deadlines
- synchronous code (SC): only reachable from code
- asynchronous code (AC): also reachable from interrupts
- supports race condition detection (between AC and SC code)
- active messages: small packets (32 bytes with 1 handler id byte) used for communication between code and devices

## TinyOS hands-0n
To install I followed [this guide](https://inrg.soe.ucsc.edu/howto-setup-instant-contiki-with-virtualbox/). 
1.  Download [Instant Contiki 3.0](https://sourceforge.net/projects/contiki/files/Instant%20Contiki/Instant%20Contiki%203.0/)
2. Unpack to a somewhat permanent location (e.g. /Documents)
3. Start VirtualBox
	1. New virtual machine
	2. Name: Contiki, Type: Linux, Version: Ubuntu 32-bit
	3. Memory: 2048MB
	4. Use an existing virtual hard disk drive -> in the unzipped folder select "Instant_Contiki_Ubuntu_12.04_32-bit.vmdk"
	5. Create
6. Login using password: user
7. Set keyboard layout to English (US, international with dead keys).
8. Devices -> Insert Guest Additions CD -> follow the prompts to install
9. Enable bidirectional copy pasting and drag-n-drop
10. Reboot the virtual machine
11. Updating stuff:
	1. ```bash 
	sudo apt-get update
	2. ```bash
	sudo apt-get install nescc
	3. ```bash
	sudo apt-get install python-dev
	4. Add TinyOS to sources:
		```bash
		sudo nano /etc/sources.list  
		```
		Add the following line to the bottom of this file  
		```bash
		deb http://tinyos.stanford.edu/tinyos/dists/ubuntu lucid main
	5. ```bash
	sudo apt-get update && sudo apt-get upgrade
12. Install and configure tinyOS:
	1. ```bash
	sudo apt-get install tinyos-source
	2. ```bash
	git clone https://github.com/tinyos/tinyos-release.git
	3. ```bash
	cd /home/user/tinyos-release
	4. ```bash
	cd tools
	5. ```bash
	./Bootstrap
	6. ```bash
	./configure --prefix=/opt/tinyos
	7. ```bash
	make
	8. ```bash
	sudo make install
	9. ```bash
	cd ..
	10. ```bash
	touch tinyos.sh
	11. In tinyos.sh put in:
```bash
#! /usr/bin/env bash  
# Here we setup the environment  
# variables needed by the tinyos  
# make system  
echo "Setting up for TinyOS 2.1.2 Repository Version"  
export TOSROOT=  
export TOSDIR=  
export MAKERULES=  
TOSROOT="/home/user/tinyos-release"  
TOSDIR="$TOSROOT/tos"  
CLASSPATH=$CLASSPATH:$TOSROOT/support/sdk/java:.:$TOSROOT/support/sdk/java/tinyos.jar  
MAKERULES="$TOSROOT/support/make/Makerules"  
export TOSROOT  
export TOSDIR  
export CLASSPATH
export MAKERULES
```

12. Run the following commands:
```bash
source /home/user/tinyos-release/tinyos.sh export TOSROOT="/home/user/tinyos-release"
```
```bash
export TOSDIR=$TOSROOT/tos	
```
```bash
export CLASSPATH=$CLASSPATH:$TOSROOT/support/sdk/java
```
```bash
export MAKERULES=$TOSROOT/support/make/Makerules
```
```bash
export PYTHONPATH=$PYTHONPATH:$TOSROOT/support/sdk/python
```
```bash
export PATH=/opt/msp430/bin:$PATH
```
```bash
export APP="$TOSROOT/apps"
```
```bash
cd ..
```
```bash
sudo chown -R user:user ~
```
Setup done.

### Report:
Nothing but pain and outdated crap.

### Introduction to RIOT OS
- open source
- built for networked and memory-constrained, low power, IoT devices
- written in ANSI C
- Based on microkernel architecture

features:
- modularity
	- customization of the system's configuration
	- minimized kernel size
- tickless scheduler
	- allows for fully idling
- straight forward interrupt handler
- 