
| **Combinational Circuits**            | **Sequential Circuits**                                   |
| ------------------------------------- | --------------------------------------------------------- |
| Output depends only on current inputs | Output depends on current inputs and past states (memory) |
| No feedback or storage                | Uses memory elements                                      |
| Example: Adders, Multiplexers         | Example: Flip-flops, Counters                             |


### **2. Design Procedure for Combinational Circuits**

1. Define the problem.
    
2. Identify inputs and outputs.
    
3. Create a **truth table**.
    
4. Derive **Boolean expressions**.
    
5. Simplify using Boolean algebra or **K-Map**.
    
6. Draw the logic circuit.
    

> **Example**: Design a 2-input AND gate  
> Inputs: A, B → Output: Y = A · B

---

### 🔹 **3. Logic Implementation Using NAND/NOR**

- **NAND and NOR** gates are **universal**: Any logic function can be implemented using just NAND or NOR.
    

> **Example**:  
> Implement `Y = A + B` using **only NAND gates**:

1. Use DeMorgan's theorem:
    
    A+B=A‾⋅B‾‾A + B = \overline{\overline{A} \cdot \overline{B}}A+B=A⋅B
2. Construct with NAND gates.
    

---

### 🔹 **4. Example: Majority Circuit**

> **Problem**: Output = 1 when majority of A, B, C are 1  
> **Truth Table** → Simplified SOP:

Y=AB+AC+BCY = AB + AC + BCY=AB+AC+BC

---

### 🔹 **5. Example: Output = 1 for Binary Numbers > 6**

Inputs: A (MSB), B, C, D (LSB)

> Output Z = 1 when input > 0110 (binary 6)  
> **Simplified Boolean Expression**:

Z=AZ = AZ=A

## **FUNCTIONS OF COMBINATIONAL LOGIC**

These are standard combinational circuits that perform specific tasks. Here's a breakdown:

---

### ✅ 1. **Half-Adder**

**Purpose**: Adds two single-bit binary numbers (A and B)

**Outputs**:

- **Sum (S)** = A⊕BA \oplus BA⊕B (XOR)
    
- **Carry (C)** = A⋅BA \cdot BA⋅B (AND)
    

📘 **Truth Table**:

|A|B|Sum (S)|Carry (C)|
|---|---|---|---|
|0|0|0|0|
|0|1|1|0|
|1|0|1|0|
|1|1|0|1|

📌 Used in constructing full-adders.

### ✅ 2. **Full-Adder**

**Purpose**: Adds three binary bits: A, B, and **Carry-in (Cin)**.

**Outputs**:

- **Sum (S)** = A⊕B⊕CinA \oplus B \oplus CinA⊕B⊕Cin
    
- **Carry-out (Cout)** = AB+Cin(A⊕B)AB + Cin(A \oplus B)AB+Cin(A⊕B)
    

📘 **Truth Table**:

|A|B|Cin|S|Cout|
|---|---|---|---|---|
|0|0|0|0|0|
|0|0|1|1|0|
|0|1|0|1|0|
|0|1|1|0|1|
|1|0|0|1|0|
|1|0|1|0|1|
|1|1|0|0|1|
|1|1|1|1|1|

📌 Can be built using **two half-adders and one OR gate**.

---

### ✅ 3. **Half-Subtractor**

**Purpose**: Subtracts one binary digit (B) from another (A)

**Outputs**:

- **Difference (D)** = A⊕BA \oplus BA⊕B
    
- **Borrow (B)** = A‾⋅B\overline{A} \cdot BA⋅B
    

📘 **Truth Table**:

|A|B|D|Borrow|
|---|---|---|---|
|0|0|0|0|
|0|1|1|1|
|1|0|1|0|
|1|1|0|0|

---

### ✅ 4. **Full-Subtractor**

**Purpose**: Subtracts one bit and borrow from another  
**Inputs**: A, B, **Bin** (borrow in)

**Outputs**:

- **Difference** = A⊕B⊕BinA \oplus B \oplus BinA⊕B⊕Bin
    
- **Borrow-out** = A‾B+Bin(A⊕B‾)\overline{A}B + Bin(\overline{A \oplus B})AB+Bin(A⊕B​)
    

📌 Not shown in detail in the file, but this is its standard logic.

---

### ✅ 5. **Binary Parallel Adder**

**Purpose**: Adds two **multi-bit binary numbers** using full-adders in parallel

📘 Example:

- Add 111 (7) and 101 (5) using a 3-bit adder:
    
    markdown
    
    CopyEdit
    
      `111 + 101 ------  1100  (Sum = 12)`
    

📌 Requires **n full adders for n-bit addition**  
📌 Carry propagates from LSB to MSB.

---

### ✅ 6. **Magnitude Comparator**

**Purpose**: Compares two binary numbers A and B  
**Outputs**:

- A>BA > BA>B
    
- A=BA = BA=B
    
- A<B A < B A<B
    
 ✅ 7.  Decoders

**Purpose**: Converts n input bits into up to 2n2^n2n output lines  
Only one output is HIGH at any time

📘 Example: 3-to-8 decoder  
Inputs: A, B, C → 8 outputs: O0 to O7

📌 Can be used to implement **any Boolean function** by combining outputs with OR gates.

---

### ✅ 8. **BCD to 7-Segment Decoder**

**Purpose**: Converts a **4-bit BCD** input into signals to drive a **7-segment LED display** (a–g)

📘 For example, input 0100 (decimal 4) lights up segments: b, c, f, and g

---

### ✅ 9. **Encoders**

**Purpose**: Reverse of decoders

- Converts one of several **active inputs** into a **binary code output**
    

📘 Example: 8-to-3 encoder:

- 8 input lines → 3-bit binary output
    

### 10. **Priority Encoder**

**Purpose**: Like a regular encoder, but **selects the highest priority input** when multiple inputs are active

📘 Adds a **valid bit (V)** to indicate if any input is active

---

### ✅ 11. **Multiplexers (MUX)**

**Purpose**: Selects one input from **multiple input lines** and sends it to one output

📘 Controlled by **select lines**

📘 Example: 4-to-1 MUX

- 4 inputs, 2 select lines → 1 output
    

---

### ✅ 12. **Demultiplexers (DEMUX)**

**Purpose**: Opposite of MUX

- Takes 1 input and routes it to **one of many outputs**
    

📘 Example: 1-to-4 DEMUX

---

### ✅ 13. **Parity Generator and Checker**

**Purpose**: Used for **error detection** during data transmission

#### Parity Bit:

- **Even parity**: total 1s = even
    
- **Odd parity**: total 1s = odd
    

📘 Parity Generator: Adds parity bit  
📘 Parity Checker: Checks if received bits + parity are valid


## 🧾 Summary Table:

|Function|               Purpose|                                               Key Output(s)|

|Half-Adder|           Add 2 bits|                                              Sum, Carry|
|Full-Adder|            Add 3 bits (A, B, Cin)|                                Sum, Carry-out|
|Half-Subtractor|    Subtract B from A|                                   Difference, Borrow|
|Full-Subtractor|     Subtract with borrow|                              Difference, Borrow-out|
|Binary Adder|        Add multi-bit binary numbers|                  Sum, Carry|
|Comparator|         Compare two values|                                   A>B, A=B, A<B|
|Decoder|               Decode n inputs to 2n2^n2n lines|              One high output|
|BCD to 7 Segment|           Display BCD digits|                            Segment control (a–g)|
|Encoder|                  Encode active input to binary|                       Binary code|
|Priority Encoder|     Encodes highest priority input|                 Binary code + valid bit|
|Multiplexer|             Selects 1 input out of many|                      Single output|
|Demultiplexer|          Sends input to one of many lines|          Routed output|
|Parity Circuits|         Error checking/detection|                           Parity bit / Check bit|



DECODERS  
A decoder is a combinational circuit that converts binary information from n input lines to a maximum of 2 the power of n unique output lines.

Normally every commercially available decoder ICs have a special input other than normal working input variables called ENABLE.
 The use of this ENABLE input is that when activated the complete IC comes to the working condition for its normal functioning. 
 If ENABLE input is deactivated the IC goes to sleep mode, the normal functioning is suspended, and all the outputs become logic 0 irrespective of normal input variables conditions.

Encoder 
An encoder is a digital circuit that performs the inverse operation of a decoder.
	  An encoder has 2  the power of n (or fewer) input lines and n output lines. 
	  The output lines generate the binary code corresponding to the input value.
	  It is assumed that only one input has a value of 1 at any given time; otherwise the circuit has no meaning.

Priority Encoder
Accepts multiple values and encodes them • Works when more than one input is active  Consists of: • Inputs (2n) • Outputs – when more than one output is active, sets output to correspond to highest input –V (indicates whether any of the inputs are active) • Selectors / Enable (active high or active low)

MULTIPLEXERS
 A digital multiplexer is a combinational circuit that selects binary information from one of the 2n input channels and transmits to a single output line. 
 That is why the multiplexers are also called data selectors. 
 The selection of the particular input channel is controlled by a set of select inputs.
 Select binary information from one of many input lines and direct it to a single output line  2n input lines, n selection lines and one output line

Demultiplexer 
 A demultiplexer is a circuit that receives information from a single line and directs it to one of 2 the power of n possible output lines. 
 The selection of a specific output is controlled by the bit combination of n elected lines.  The term “demultiplex” means one into many.

One of the simplest and most widely used schemes for error detection is the parity method.  Parity Bit:- A parity bit is an extra bit that is attached to a code group that is being transferred from one location to another.
 The parity bit is made either 0 or 1, depending on the number of 1 is that are contained in the code group. Two different methods are used.
		 The even-parity method, and 
		 The odd-parity method.
		
A parity generator is a combination logic system to generate the parity bit at the transmitting side.
 Parity Checker:- The message bits with the parity bit are transmitted to their destination, where they are applied to a parity checker circuit. 
 The circuit that checks the parity at the receiver side is called the parity checker. 

 The parity checker circuit produces a check bit and is very similar to the parity generator circuit.