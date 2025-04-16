## **DLD Chapter 3 Notes: Basic and Derived Logic Gates**

### 🔹 1. Boolean Algebra Basics

- Boolean variables have only two values: **0 (False)** and **1 (True)**.
    
- Boolean operations are used in **logic circuits**:
    
    - **OR (+)**
        
    - **AND (·)**
        
    - **NOT (¯)** (Inversion)
- ### 2. Basic Logic Gates

####  **OR Gate**

- Symbol: Y=A+BY = A + BY=A+B
    
- **Output is 1 if any input is 1**
    
- Truth Table:
  #### **AND Gate**

- Symbol: Y=A⋅BY = A \cdot BY=A⋅B
    
- **Output is 1 only if all inputs are 1**
#### **NOT Gate (Inverter)**

- Symbol: Y=A‾Y = \overline{A}Y=A
    
- **Output is the opposite of input**
### 3. Derived Logic Gates

#### ✅ **NAND Gate**

- Y=A⋅B‾Y = \overline{A \cdot B}Y=A⋅B
    
- **Opposite of AND gate**
    
- Output is 0 **only when both inputs are 1**
    

---

#### ✅ **NOR Gate**

- Y=A+B‾Y = \overline{A + B}Y=A+B​
    
- **Opposite of OR gate**
    
- Output is 1 **only when both inputs are 0**
    

---

#### ✅ **XOR Gate (Exclusive OR)**

- Y=A⊕B=AB‾+A‾BY = A \oplus B = A \overline{B} + \overline{A} BY=A⊕B=AB+AB
    
- **Output is 1 only if inputs are different**
    

---

#### ✅ **XNOR Gate (Exclusive NOR)**

- Y=A⊕B‾Y = \overline{A \oplus B}Y=A⊕B​
    
- **Output is 1 only if inputs are the same**
    

---

### 🔹 4. Universality of NAND & NOR

- **Any logic circuit** can be built using **only NAND or only NOR gates**.
    
- These gates are called **universal gates**.
    

---

### 🔹 5. Logic Expressions and Circuit Output

- Use Boolean rules:
    
    1. Perform NOT first
        
    2. Then AND
        
    3. Then OR
        
- Example:
    
    Y=(A+B)‾⋅CY = \overline{(A + B)} \cdot CY=(A+B)​⋅C

---

## 📘 Sample Questions for Exit Exam

### ✨ **1. Multiple Choice Questions**

**Q1.** What is the output of a NAND gate when both inputs are 1?  
A) 0  B) 1  C) Same as AND  D) None  
**Answer:** A) 0

**Q2.** What is the Boolean expression for an XOR gate?  
A) A+BA + BA+B B) ABABAB C) A⊕BA \oplus BA⊕B D) AB‾\overline{AB}AB  
**Answer:** C) A⊕BA \oplus BA⊕B

---

### ✨ **2. Fill in the Blanks**

**Q1.** The output of an OR gate is 1 when ________.  
**Answer:** any input is 1

**Q2.** The NOT operation is also called ________.  
**Answer:** Inversion or Complement

---

### ✨ **3. True or False**

**Q1.** XNOR gate gives output 1 when both inputs are the same.  
**Answer:** True

**Q2.** NAND gate is not a universal gate.  
**Answer:** False

---

### ✨ **4. Problem Solving**

**Q1.** Determine the output of the logic circuit:  
Y=A+B‾⋅CY = \overline{A + B} \cdot CY=A+B​⋅C, where A = 0, B = 1, C = 1

A+B=1⇒1‾=0⇒0⋅1=0A + B = 1 \Rightarrow \overline{1} = 0 \Rightarrow 0 \cdot 1 = 0A+B=1⇒1=0⇒0⋅1=0

**Answer:** Y = 0

