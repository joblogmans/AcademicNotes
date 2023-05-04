# Week 2
# Embedded processors and FPGAs
Embedded Processor
- executes instructions sequentially
- commands get broken down to instructions (the smallest programmable element)
- Different instruction sets
	- x86, RISC (ARM), CISC, etc.
- Flexible: one can change the behaviour of an embedded processor by changing the software
- It is a generic platform for many kinds of applications

FPGAs (Field-programmable Gate Arrays)
- Reconfigurable logic (digital circuit), built of logic blocks (AND, OR, etc.)
- Changes in the program require changes in the hardware
- The timing of FPGA-based designs are usually known and must more efficient and fast

## Main features of embedded processors
Specific types of processors are better at certain operations.
DSP Processors are designed specifically for signal processing, which have dedicated units that deal with those routines efficiently.

Different optimization goals when choosing processors:
- Performance
- Energy Consumption
- Versatility
- Cost

Microcontroller:
- CPU
	- Control logic, instruction decoder, ALU, registers
- Program memory
- Program counter
- RAM
- Non-volatile memory (e.g. EEPROM)
- Peripherals (timer, [[ADC and DAC#ADC|ADC]], etc.)

Clock frequency:
- an instruction takes a multiple of clock cycles
- Clock Control unit controls the clock
A microcontroller might have multiple clock sources

Interrupts:
- is a hardware-generated function call
- breaks the current program
- Sources: I/O or peripherals
- Interrupt service routine
- Different priority levels

Peripherals:
Used to give CPU data
Several types:
- Communication units (e.g. [[SPI]], I2C, [[UART]], TWI, [[USB]], Ethernet, CAN)
- Analog units (e.g. [[ADC and DAC]], Analog comparators)
- Timers/counters (e.g. PWM, time intervals measurements)
- Memory (e.g. DMA)

Power modes:
- MCUs have multiple power modes which allows for fine-grained control
- Power modes can be applied to CPU, peripherals and more

Programming interfaces
- Programming:
	- JTAG (Joint Test Action Group)
	- PDI (Program and Debug Interface)
	- ISP (In-System Programming)
	- If there is a bootloader almost any communication protocol will suffice. Does not allow for debugging
- Debugging: JTAG, PDI

## Use-cases of micro-controller platforms
Basically an ad for arduino and STM. Fair enough

## Reconfigurable platforms, FPGAs
-ASIC:  Application Specific Integrated Circuit
	- Expensive, very efficient, not flexible

FPGA nice compromise between processors and ASICs.

See [[FPGA]].

[[FPGA]] can be used to prototype ASICS which are not changeable. They can be used to prototype signal processing and also for low to medium volume products as they are more general components. 

Some vendors of FPGA products:
- Xilinx
- Altera
- Actel
Good starting board to discover FPGAs: Spartan-6 or the SP601 Evaluation kit

## Embedded processors vs. FPGAs
Microcontrollers design flow:
- programming language
	- Assembly (for performance)
	- C/C++ (for large systems) 
	- Or a combination

FPGA design flow:
- Setup project:
	- describe hardware (using VHDL or Verilog)
	- pin assignment
	- constraints
- programming
	- lots of stuff that I didn't follow

Hybrid platforms:
- System on a Chip (SoC)
	- Uses advantages of both an [[FPGA]] and an embedded processor
	- For example the Zyng-7000, has a processor and an [[FPGA]]
