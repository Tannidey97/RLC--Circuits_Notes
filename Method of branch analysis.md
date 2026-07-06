# Branch analysis 

**Branch analysis is the process of studying each branch of a circuit separately to determine the current flowing through it and the voltage across it.**

***[A branch is a series connection of elements in the network that has the same current.]***

# Solving Method 

### Assume a current in every branch.

**1)Give each branch a current name like I₁, I₂, I₃.**  
**2)You can choose any direction (clockwise or anticlockwis).**  
**3)If the answer comes out negative, it simply means the actual current flows in the opposite direction.**  
### Mark the voltage polarity (+ and –).  
**For every resistor, mark the + where the current enters.**  
### Apply Kirchhoff's Voltage Law (KVL).  
**Write one KVL equation for each independent loop.**  
**The rule is:  
***Sum of voltage rises = Sum of voltage drops***  
or
***Total voltage around a closed loop = 0***  

### Apply Kirchhoff's Current Law (KCL).

**Choose the required number of nodes.**
At each node, write:
***Current entering = Current leaving***  
### Solve the equations.

# Method of solving through a simple circuit.

https://github.com/Tannidey97/RLC--Circuits_Notes/blob/main/IMG_20260706_122007_075.jpg

**In the circuit, the KVL is applied to the both loop clockwisely.**  

### Equation for first loop  

 **2 - 2I₁ - 4I₃ = 0**  
 
***[ Notice that there are assumed individual current for each branch such as I₁, I₂, I₃ ]***

 ### Equation for the 2nd loop 

 **4I₃ + 1I₁ - 6 = 0**
 
***[ In the given circuit diagram my assumed direction is opposite to the actual direction of the circuit that is why voltage rises across R₃ & R₂ according to my assumed clockwise direction.]***

### Equation for the node a  

**I₁ + I₂ = I₃**

## Rewritten the equations :  

**2I₁ + 0 + 4I₃ = 2**  
**0 + I₂ + 4I₃ = 6**  
**I₁ + I₂ - I₃ = 0**  

### Solving 

**We can solve these equations using Cramer's rule, Substitution method, Elimination method.**  
    

***[ In the case of Mesh Analysis, we wouldn't assume I₃ for the middle Branch, rather than we would define the current through this branch using I₂ & I₃.This is the difference between mesh analysis and branch analysis.]***

