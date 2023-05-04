# Week 4
## Contiki and Cooja simulation
Contiki is a hybrid operating system -> modular kernel
- event driven kernel
- supports preemptive multi-threading
- seperates kernel from processes
- communication of services by posting events
- no hardware abstraction layer -> processes communicate with the hardware directly
- load/unload services/applications at run-time
- abstractions implemented as libraries and services
- CPU multiplexing provided by the base system

## The Contiki system
- consists of the kernel, libraries and applications/services
- possible to dynamically replace processes at run-time
- shares the same address space between processes
- A process can be run ineither:
	- cooperative -> processes wait for each other to finish
	- preemptive -> aggresively takes over the cpu

- process control bloack accessed by kernel
- a pointer to the process state used by kernel
- the process state stored in the process' private memory

- core consists of:
	- program loader
	- most commonly used parts of the languager run-time
	- supported libraries
	- communication stack with device drivers
- compiled into a single binary image

## Contiki's kernel architecture
- lightweight event scheduler
- two kinds of events:
	- asynchronous -> stored in event queue and not directly delivered to the process
	- synchronous -> similar to calling a function
- polling mechanism
- single shared stack for all processes
- more...

## Contiki services and libraries
Services:
- implemented as modules
- A form of shared library
- Can be dynamically replaced at run-time
- identified by a textual string
	- string matching to query installed services
- installed and running services are tracked by a service layer
- includes a version number and a function table in a service interface
- stub library
	- linked with the application
	- uses service library to find the service process
	- the process ID is cached for future requests

service replacement:
- dynamically loaded and replaced services
- retaines process ID even if services replaced
- when a service is replaced, the running service is informed, existing data can be passed to the new service. 

Libraries:
- rest of systems is implemented as system libraries
- three types of linking between libraries and applications:
	- statically linked with the part of the core
	- statically linked with the part of the loadable program
	- calling services implementing a specific library -> because library is implemented as service it can be replaced at run-time

## Communication in Contiki I
communication is implemented as a service
- allows for loading multiple services
- synchronous events
- more about Rime

## Communication in Contiki II
Now MicroIP
- supports TCP/IP

## Protothread, multithreading and code sizes
Protothreads:
- implement sequential flow of control in a simple way
- light-weight and stackless threads
- shared stack, thus context switching can be done very simply
- written in standard C
- runs within a single function, can't span over other functions
- implemented using local continuations

Preemptive multi-threading:
- implemented as a library
- optionally linked with applications, if not necessary not in the program
- implementation of he preemption by a timer interrupt
- library is divided into
	- platform independant part
	- platform specific part
- separate stack per thread
- threads executre on their own stack until preempted
- provides API

Over-the-air-programming:
- a way to remotely program nodes using point-to-point communication
- negative acknowledgements

## Cooja simulation
- 