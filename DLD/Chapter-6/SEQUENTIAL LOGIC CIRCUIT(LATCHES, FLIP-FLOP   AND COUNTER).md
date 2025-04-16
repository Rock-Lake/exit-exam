
## 1. Introduction to Sequential Circuits

- Unlike combinational circuits, **sequential circuits** depend on both **present inputs and past outputs (history)**.
    
- They have **feedback** from output to input.
    
- Two types:
    
    - **Synchronous** (clock-controlled)
        
    - **Asynchronous** (no global clock)
    - 
Storage Element (memory): Latches & Flip-Flops
	Storage elements that operate with signal levels (rather than signal transitions) are referred to as Latches; 
	those controlled by a clock transition are flip-flops. 
	▪ Latches are said to be level sensitive devices; flip-flops are edge sensitive devices.
### **Latches**

- Level-sensitive memory devices.
    
- Two stable states (bistable).
    
- Output depends on **input levels**.
    
- Types:
    
    - **S-R Latch** (NOR-based active HIGH or NAND-based active LOW)
        
    - **Gated S-R Latch** (with Enable input)
	    - • The latch will not change until EN is HIGH; but as long as it remains HIGH, the output is controlled by the state of the S and R inputs.
	    - •  the invalid state occurs when both S and R are simultaneously HIGH.
        
    - **Gated D Latch** (Data latch)
	    - It differs from the S-R latch because it has only one input in addition to EN.
	    - • This input is called the D (data) input. 
	    - • When the D input is HIGH and the EN input is HIGH, the latch will set.
	    - • When the D input is LOW and EN is HIGH, the latch will reset.
        

📘 **Important Concepts**:

- **S = 1, R = 0 → Set**, **S = 0, R = 1 → Reset**
    
- **S = R = 1 → Invalid** (in S-R latch)
    
- **Gated latches** change state only when **Enable (EN)** is HIGH.

The difference between latch and flip-flop is in the method used for changing their state.

## Flip-Flops (Edge-triggered memory elements)

Flip-flops are edge-triggered, that is that they depend on the transition of a signal. 
• This may either be a LOW-to-HIGH (rising edge) or a HIGH to-LOW (falling edge) transition.

- **Flip-flops** change output **only on clock edge** (rising or falling).
    
- **Edge-sensitive**, unlike level-sensitive latches.
    
- Types:
    

### ✅ a) S-R Flip-Flop

- Similar to S-R latch but clocked.
    
- **Invalid state when S = R = 1**
    
- Output changes on clock **transition**
    

### ✅ b) D Flip-Flop

D FF is useful when a single data bit (1 or 0) is to be stored. ▪

- Stores single bit.
    
- No invalid state.
    
- Output Q = D at clock edge.
    

### ✅ c) J-K Flip-Flop

The difference between J-K and S-R is a J-K has no invalid state as SR.

- **Universal flip-flop**, no invalid state.
    
- **J = 1, K = 1 → Toggle**
    

### ✅ d) T Flip-Flop

- Simplified version of J-K.
    
- **T = 1 → Toggle**, **T = 0 → Hold**

## Tables for Flip-Flops

Each flip-flop has:

- **Characteristic Table** (defines output next state)
    
- **Excitation Table** (determines required input for given state change)

## Counter Design

**Counters** = group of flip-flops used for **counting sequences**.

### ✅ Two types:

1. **Asynchronous Counter** (Ripple counter)
    
    - Flip-flops triggered **one after another**
        
    - Slower, due to **propagation delays**
    - An asynchronous counter is one in which the flip-flops (FF) within the counter do not change states at exactly the same time because they do not have a common clock pulse.
 a) 2-bit Ripple Counter

- Clock given to 1st flip-flop
    
- Each flip-flop toggles on previous FF’s output
    

### ✅ b) 3-bit & 4-bit Ripple Counters

- Count from 000 to 111 (3-bit) or 0000 to 1111 (4-bit)
    

### ✅ c) Decade Counter (MOD-10)

- Counts from 0 to 9 then resets
    
- **Truncated** counter (modulus < 2n2^n2n)
        
2. **Synchronous Counter**
    
    - All flip-flops triggered **simultaneously** by the same clock
        
    - Faster and more accurate
- 
In asynchronous counters, commonly called ripple counters, the first flip flop is clocked by the external clock pulse and then each successive flip-flop is clocked by the output of the preceding flip-flop.
 ▪ In synchronous counters, the clock input is connected to all of the flip-flops so that they are clocked simultaneously.

The modulus is the number of unique states through which the counter will sequence

Maximum possible number of states of counter is 2 the power of  n , n is the number of flip-flops in the counter 
– Example : Modulus 8 = 2 the power of  3 (Need 3 flip flops)
• Counter can be designed to have a number of states in their sequence that is less than maximum, 2 the power of n . This called truncated sequence


## Summary of Key Components

| Component    | Type            | Description                     |
| ------------ | --------------- | ------------------------------- |
| Latch        | Level-sensitive | Memory device without clock     |
| Flip-Flop    | Edge-sensitive  | Clock-controlled memory element |
| Counter      | Sequential      | Series of FFs to count states   |
| Synchronous  | Clocked FFs     | All FFs triggered at same time  |
| Asynchronous | Ripple FFs      | FFs triggered one after another |
