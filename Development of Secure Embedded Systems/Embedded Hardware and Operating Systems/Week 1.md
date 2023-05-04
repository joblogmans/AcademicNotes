# Week 1
## Introduction
Main concerns for embedded systems:
- Reliability
- Security
- Real-time behavior

In Internet of Things:
- Everywhere
- Energy efficient
- Machine learning (to process data)

How to describe an embedded system:
- typically reactive
	- waits for input
	- performs computations
	- generates outputs
	- -> can be modeled as automota

System model:
- input: sensors
- output: actuators
- computation: processing elements. Two types:
	- Embedded processors
	- FPAGs

Design of embedded systems:
- application
- requirements
- characteristics
- Challenges:
	- Dependability
	- Efficiency
	- Real-time constraints
By choosing correct combination of hardware and software these challenges can be met. Also check interactivity between components (concurrency).

Design flow: idea -> specification -> repository (version control and data storage) -> iteration -> evaluation (based on parameters and requirements) -> validation.

Approaches to design:
- Waterfall model: sequentially from the top to the bottom
- Iterative: steps are repeated until the requirements are met

Dependability if reliable, available, maintainable, safe and secure.
Efficiency: amount of useful work done per Joule.
- processors: least efficient
- ASIC: most efficient
- hardware = software -> if the software doesn't use specific features of the hardware efficiency is lost
- code size: must occupy as little space as possible
- physical size: small and portable?
- cost: minimal number of components

## Input/Output (I/O)
- [[GPIO]]
- [[SPI]]
- Analog/Digital

Reading input:
- Time-based (s, ms, etc...)
	- Timer-based
	- software initiated
	- chance to miss an event
	- RX buffer
- Interrupt based
	- Hardware initiated
	- Reliable - event will not be missed

Output:
- Require similar voltages and other compatibilities.
- communication protocols:
	- [[UART]] unit
	- [[SPI]] unit
- Hardware-initiated transfer:
	-> e.g. the driver reads the data directly from memory when it needs it

## Arduino tutorial
Did this [tutorial](https://www.arduino.cc/en/Tutorial/InputPullupSerial) online using this [site](https://wokwi.com/projects/new/arduino-uno).

## Wired communication and ADCs/DACs
Wired communication can wire-based or wireless. Communication requires the same protocol.

[[(A)synchronous Communication#Synchronous Communication|Synchronous Communication]]:
- uses common clock
- pros: no synchronization info need, thus higher throughput

[[(A)synchronous Communication#Asynchronous Communication|Asynchronous Communication]]:
- no common clock
- data stream has synchronization information, thus lower throughput. But also doesn't require dedicated connection for the clock (e.g. an extra cable)

[[Duplex#Full Duplex|Full Duplex]]:
- bidirectional communication at the same time

[[Duplex#Half Duplex|Half Duplex]]:
- bidirectional communication, but only one at a time

See [[USB]], [[SPI]], [[ADC and DAC]] for more learned content.

## Arduino tutorial
Did this [tutorial](https://www.arduino.cc/en/Tutorial/AnalogInput) online using this [site](https://wokwi.com/projects/new/arduino-uno).

## Sensors, actuators, interrupts vs. polling
Sensors:
- measure a physical quantity -> convert physical variables to numbers (weight, velocity, acceleration)
- Can have a digital element on board to output a number

Actuators:
- alters physical quantity driven by voltage (e.g. a motor)

Issues with sensors:
- Range is limited (e.g. min and max temperature).
- Accuracy is also limited (number of bits of information).
- Noise:
	- X(t) - true value
	- X'(t) - error caused by noise
	- S(t) = X(t) + X'(t) - measurement
For example, in an accelerometer X'(t) could be vibrations.
To counter noise one could filter.

Sampling:
- S(t) - function of time
- $S_{d}=S(nT)$
	- T - fixed time interval between two subsequent samples
	- Sampling rate = 1/T Hz
- Smaller T -> more data per second.

Polling vs. interrupts
Polling:
- processor continuously checks the sensors status
	- wastes processor's time
	- difficult to catch fast events
	- simple to implement

Interrupts:
- hardware based way to break the processor flow
	- does not waste processor's time
	- happens when a physical event occurs
	- some peripherals support this without dedicated external pins:
		- [[UART]], [[ADC and DAC#ADC|ADC]]
	- Interrupt the service routine:
		- breaks program flow
		- should be fast

https://www.arduino.cc/en/Tutorial/ReadASCIIString