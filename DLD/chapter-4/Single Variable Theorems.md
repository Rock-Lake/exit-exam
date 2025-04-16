X⋅0=0 
X⋅1=X
X+0=X
X + 1= 1
X + X = X
X *  X = X
### 3. DeMorgan’s Theorems

invert(A + B)  =  invert(A)* invert(B)
invert(A*B)  = invert(A) + invert(B)
### 4. SOP (Sum of Products) & POS (Product of Sums)

#### ✅ SOP (Minterms)

- Form: OR of multiple AND terms
    
- Example: ABC+AB‾CABC + A\overline{B}CABC+ABC
    

#### ✅ POS (Maxterms)

- Form: AND of multiple OR terms
    
- Example: (A+B)(B‾+C)(A + B)(\overline{B} + C)(A+B)(B+C)
    

#### ✅ Conversion Tip:

- SOP missing minterms = POS maxterms
    
- POS missing maxterms = SOP minterms
### 5. Logic Simplification

- Simplify logic expressions using Boolean laws.
    
- **Example**:
    
    Z=  AB+AC+ABC = A(B+C)

### 6. Karnaugh Map (K-map) Simplification

- Visual method to simplify logic using truth table values.
    
- Group 1s in:
    
    - **Pairs (2)** – eliminates 1 variable
        
    - **Quads (4)** – eliminates 2 variables
        
    - **Octets (8)** – eliminates 3 variables
        

#### ✅ Don't Care Conditions

- Marked as "X" in K-map
    
- Can be grouped as 1 or 0 to simplify circuit