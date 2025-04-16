**# Digital Logic Design - Exam-Oriented Notes**

## **1. Introduction to Digital Logic**

- A number system is a code that uses symbols to represent numbers.

- The **binary number system** and digital codes are fundamental to computers and digital electronics.

- This chapter focuses on the **binary number system** and its relationship with **decimal, hexadecimal, and octal** number systems.

- Key learning outcomes include **number system conversions**, **digital codes**, and **binary arithmetic operations**.


## **2. Number Systems and Conversions**

### **Number Systems**

|Number System|Base|Digits Used|
|---|---|---|
|Binary|2|0,1|
|Decimal|10|0-9|
|Octal|8|0-7|
|Hexadecimal|16|0-9, A-F|
 **Conversions Between Number Systems**

- **Decimal to Binary**: Divide the number by 2 and record remainders.

- **Binary to Decimal**: Multiply each bit by powers of 2 and sum them.

- **Binary to Octal**: Group binary digits in sets of 3.

- **Binary to Hexadecimal**: Group binary digits in sets of 4.

- **Decimal to Octal**: Divide the number by 8 and record remainders.

- **Octal to Decimal**: Multiply each digit by powers of 8 and sum them.


**Example:** Convert (45)₁₀ to binary.

1. 45 ÷ 2 = 22 remainder **1**

2. 22 ÷ 2 = 11 remainder **0**

3. 11 ÷ 2 = 5 remainder **1**

4. 5 ÷ 2 = 2 remainder **1**

5. 2 ÷ 2 = 1 remainder **0**

6. 1 ÷ 2 = 0 remainder **1** **Answer:** (101101)₂


## **3. Digital Codes**

**Binary Coded Decimal (BCD)**

- Represents each decimal digit (0-9) as a 4-bit binary value.

- Example: (25)₁₀ in BCD → 0010 0101


### **Gray Code**

- A binary numbering system where only one bit changes between successive numbers.

- Reduces errors in digital communication.


### **Excess-3 Code**

- A modified BCD where each digit is represented by its BCD + 3.

- Example: (5)₁₀ in Excess-3 → (5 + 3)₁₀ = (1000)₂


### **ASCII Code**

- American Standard Code for Information Interchange.

- Represents text in computers using a 7-bit or 8-bit binary code.


## **4. Binary Arithmetic**

- **Addition, Subtraction, Multiplication, and Division in Binary.**

- **1’s Complement & 2’s Complement: Used for representing negative numbers.**

- **2’s complement is commonly used in computing for signed number representation.**


**Example:** Perform binary addition (1011)₂ + (1101)₂.

```
   1011
+  1101
 --------
  11000
```

**Answer:** (11000)₂

## **5. Expected Exam Questions with Answers**

### **1. Number System Conversion Questions**

**Q1:** Convert (101011)₂ to decimal.

- **Solution:** (1×2⁵) + (0×2⁴) + (1×2³) + (0×2²) + (1×2¹) + (1×2⁰)

- **Answer:** (43)₁₀


**Q2:** Convert (37)₁₀ to octal.

- **Solution:** 37 ÷ 8 = 4 remainder **5** 4 ÷ 8 = 0 remainder **4**

- **Answer:** (45)₈


**Q3:** Convert (2F)₁₆ to binary.

- **Solution:** 2 → (0010)₂, F → (1111)₂
    
- **Answer:** (00101111)₂
    

### **2. Binary Arithmetic Questions**

**Q4:** Perform binary subtraction (10101)₂ - (1001)₂ using 2’s complement.

- **Solution:**
    
    - Find 2’s complement of (1001)₂ → (0111)₂ + 1 = (1000)₂
        
    - Add: (10101)₂ + (1000)₂ = (11101)₂
        
- **Answer:** (1100)₂ (which is 12 in decimal)
    

### **3. Digital Code Questions**

**Q5:** Convert (89)₁₀ to BCD.

- **Solution:** 8 → 1000, 9 → 1001
    
- **Answer:** (1000 1001)BCD
    

**Q6:** Convert (12)₁₀ to Excess-3.

- **Solution:** 1 → (0001)₂ + 3 → (0100)₂, 2 → (0010)₂ + 3 → (0101)₂
    
- **Answer:** (0100 0101)₂
    

**Q7:** Find the Gray code of (1011)₂.

- **Solution:**
    
    - First bit remains same → 1
        
    - Next bits: 1⊕0 = 1, 0⊕1 = 1, 1⊕1 = 0
        
- **Answer:** (1110)₂
    

## **6. Exam Preparation Tips**

✅ Focus on number conversions and binary arithmetic operations. ✅ Practice BCD, Gray Code, and ASCII representations. ✅ Solve previous exam questions related to number system conversions. ✅ Review binary subtraction using 2’s complement.

---

**End of Notes**


### **1. Conceptual Questions**

🔹 **Q1:** What is a number system?  
**A:** A number system is a way to represent and count quantities using a specific set of symbols or digits. Examples include Binary (Base-2), Decimal (Base-10), Octal (Base-8), and Hexadecimal (Base-16).

🔹 **Q2:** Why is the binary number system fundamental in digital electronics?  
**A:** The binary system is fundamental because digital circuits use two voltage levels (0 and 1) to represent data and perform operations.

🔹 **Q3:** What are digital codes, and why are they used?  
**A:** Digital codes are special binary representations used for efficient data processing, error detection, and communication in digital systems. Examples include **BCD, Gray Code, Excess-3, and ASCII**.

---

### **2. Conversion Questions**

🔹 **Q4:** Convert (1101.101)₂ to decimal.  
**A:**

(1101.101)2=(1×23)+(1×22)+(0×21)+(1×20)+(1×2−1)+(0×2−2)+(1×2−3)(1101.101)_2 = (1×2^3) + (1×2^2) + (0×2^1) + (1×2^0) + (1×2^{-1}) + (0×2^{-2}) + (1×2^{-3})(1101.101)2​=(1×23)+(1×22)+(0×21)+(1×20)+(1×2−1)+(0×2−2)+(1×2−3) =(8+4+0+1)+(0.5+0+0.125)= (8 + 4 + 0 + 1) + (0.5 + 0 + 0.125)=(8+4+0+1)+(0.5+0+0.125) =(13.625)10= (13.625)_{10}=(13.625)10​

🔹 **Q5:** Convert (73)₁₀ to binary.  
**A:**

- Divide by 2:
    
    - 73 ÷ 2 = **36**, remainder **1**
        
    - 36 ÷ 2 = **18**, remainder **0**
        
    - 18 ÷ 2 = **9**, remainder **0**
        
    - 9 ÷ 2 = **4**, remainder **1**
        
    - 4 ÷ 2 = **2**, remainder **0**
        
    - 2 ÷ 2 = **1**, remainder **0**
        
    - 1 ÷ 2 = **0**, remainder **1**
        
- **Binary Equivalent:** **(1001001)₂**
    

🔹 **Q6:** Convert (2F)₁₆ to decimal.  
**A:**

(2F)16=(2×161)+(F×160)(2F)_{16} = (2 × 16^1) + (F × 16^0)(2F)16​=(2×161)+(F×160) =(2×16)+(15×1)= (2 × 16) + (15 × 1)=(2×16)+(15×1) =(32+15)=(47)10= (32 + 15) = (47)_{10}=(32+15)=(47)10​

🔹 **Q7:** Convert (110011)₂ to octal.  
**A:**

- Group into 3-bit sections: **110 011**
    
- Convert each group:
    
    - (110)₂ = **6**
        
    - (011)₂ = **3**
        
- **Octal Equivalent:** **(63)₈**
    

---

### **3. Digital Code Questions**

🔹 **Q8:** Convert (1011)₂ to BCD.  
**A:**

- In BCD, each decimal digit is represented by a 4-bit binary value:
    
    - Decimal **(11)** is not valid in BCD.
        
    - Correct approach: Convert decimal digits separately.
        
    - **(11)₁₀ is not a valid single BCD representation.**
        

🔹 **Q9:** What is the Gray code equivalent of (1011)₂?  
**A:**

1. First bit remains the same: **1**
    
2. XOR first and second bits: 1⊕0=11 \oplus 0 = 11⊕0=1
    
3. XOR second and third bits: 0⊕1=10 \oplus 1 = 10⊕1=1
    
4. XOR third and fourth bits: 1⊕1=01 \oplus 1 = 01⊕1=0
    
5. **Gray Code = (1110)₂**
    

---

### **4. Arithmetic Questions**

🔹 **Q10:** Perform binary addition: (1011)₂ + (1101)₂  
**A:**

markdown

CopyEdit

   `1011 +  1101 ------------   11000  (Binary)`

**Answer:** (11000)₂

🔹 **Q11:** Perform binary subtraction: (1010)₂ - (110)₂ using 2’s complement.  
**A:**

1. Take 2’s complement of (110)₂:
    
    - 1’s complement of **110** → **001**
        
    - Add **1** → **010**
        
2. Add (1010)₂ + (010)₂:
    
    markdown
    
    CopyEdit
    
       `1010 +  0010 ---------   1100  (Binary)`
    

**Answer:** (100)₂

---

These questions cover multiple aspects of **number systems, conversions, digital codes, and arithmetic operations**—all key areas for your exit exam. Do you want me to add more **complex** questions or focus on a particular area?