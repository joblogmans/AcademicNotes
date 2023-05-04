# ADC and DAC
## ADC
Analog to Digital Converter. Converts a voltage to a number.
Uses successive approximation. Successive approximation uses a built-in [[ADC and DAC#DAC|DAC]] and binary search. It starts with setting the DAC to output the value of the most significant bit and compares this to the input signal. If it is higher than the input signal, the first bit is set to 1, otherwise 0. Then it continues to the second most significant bit combined with the previous bit. Again, if higher than input signal, 1, otherwise 0. Repeat for all bits.

## DAC
Digital to Analog Converter. Converts a number to a voltage.

## Specifications
### Resolution
Number of bits of accuracy it can convert to a number or voltage.

### Conversion rate
Time needed for a single conversion.