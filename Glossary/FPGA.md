# FPGA
Field-Programmabale Gate Array. A semiconductor device using a matrix of Logic Blocks (LBs) with programmable interconnects. Software almost equals hardware in these systems. FPGAs provide very high efficiency and real-time reliability at the cost of flexibility.
Some FPGAs are one time programmable while others can be programmed multiple times.

## Logic Block
Basic logic unit with varying features in a configurable switch matrix. Here, logic means logic gates as in AND, OR and more functions, together working using combinational logic to make a funtional program. The combinational logic is represented by lookup tables (LUT). Additionally, the logic block contains a register to implement sequential logic, thus introducing clocking and synchronization into the design.
There are also multiplexers in the logic block which allow to either select the LUT or flip flop output.
Complex designs will require many logic blocks to be connected together.

## Other components
Interconnects: connects LBs and routs signals between LBs and I/O.
Memory: Embedded block RAM memory.

## Random comments
Some FPGAs can be dynamically reprogrammed (= while the program is running) while others can only be programmed at the start.