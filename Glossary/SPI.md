# SPI
Serial Peripheral Interface.

## Physical properties
4 wires:
- Master Out Slave In
- Master In Slave Out
- Serial Clock
- Chip Select

Communication is done by doing serial shift registers. Whenever a bit is moved from the slave to the master, a bit from the master is moved to the slave. The shift registers are connected!
SPI can be daisy chained. The shift register of slave 0 will then be connected to the shift register of slave 1 (for example).