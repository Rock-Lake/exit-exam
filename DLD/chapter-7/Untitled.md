==Applications of Flip Flop==

•Registers: (data storage and data movement) 
•Shift Registers 
•Counters (Ring, Twisted Ring, ripple, Up/ Down, Synchronous)
•Sequence generator

A register is a digital electronic device capable of storing several bits of data
– Normally made from D-type flip-flops with asynchronous RESET inputs 
– Operates on the bits of the data word in parallel (parallel in / parallel out)

### ==Shift Register==

•A shift register is a sequential logic device made up of flip-flops that allows parallel or serial loading and serial or parallel outputs as well as shifting bit by bit.
•Common tasks of shift registers:
	- – Serial/parallel data conversion
	- – Time delay 
	- – Ring counter
	- – Twisted-ring counter or Johnson counter
	- – Memory device
	====
==Types of Shift Register==

1. Serial In Serial Out (SISO) 
2. Serial In Parallel Out (SIPO) 
3. Parallel In serial Out (PISO) 
4. Parallel In Parallel Out (PIPO)

==Shift Register as Counter==

✓ A shift register counter is basically a shift register with the serial output connected back       to the serial input to produce special sequences. 
✓ Two of the most common types of shift register counters, the Johnson counter and the         ring counter

==*Ring Counter*==

A ring counter is obtained from a shift register by directly feeding back the true output of the output flip-flop to the data input terminal of the input flip flop

*==Johnson counter / Twisted Ring counter==*

The Johnson counter is similar to the Ring counter.
• The only difference between the Johnson counter and the ring counter is that the inverted outcome Q' of the last flip flop is passed to the first flip flop as an input.
• The remaining work of the Johnson counter is the same as a ring counter.
• The Johnson counter is also referred to as the Creeping counter. 
• Number of unique sates are 2 time the number of bits(flip flops) • For 4 bits there 4*2 = 8 unique states