# Mesh Analysis 

**Mesh analysis is a circuit analysis method used to find the current flowing in each small closed loop (mesh) of a circuit by applying the Kirchhoff's Voltage Law to every mesh.**

**We use mesh analysis to find current for each loop. The currents to be defined are called mesh or loop current. 'Mesh' means smallest possible planner loop.**
**The numbers of mesh currents is will equal to the number of loop or windows of the circuit. If the planner circuit have 2 loop, mesh current will also be 2 for that circuit.**

# Method of Solving 

### Identify all the meshes.

**1)Find the smallest closed loops in the circuit.**  
**2)Number them as Mesh 1, Mesh 2, Mesh 3, ...**  

### Assume a mesh current for each mesh.

**1)Assign a current to every mesh.**  
**2)Usually we choose clockwise or anticlockwise directions for all mesh currents.**  
Example:
Mesh 1 → I₁  
Mesh 2 → I₂   
Mesh 3 → I₃  

### Apply Kirchhoff's Voltage Law (KVL).

**Write one KVL equation for each independent loop.**  
The rule is:
***Sum of voltage rises = Sum of voltage drops***  
or
***Total voltage around a closed loop = 0*** 

**Resistor in only one mesh: Voltage = R * I.**  
**Resistor shared by two meshes: Voltage = R(I₁ - I₂)  or R(I₂ -  I₁) depending on the direction in which you are writing the KVL equation.**

### Solve the equations.

**Use substitution, elimination, or a calculator to find the values of the mesh current.**  

# Method of solving through a simple circuit 

https://github.com/Tannidey97/RLC--Circuits_Notes/blob/main/IMG_20260706_133757_506.jpg

**Using clockwise direction, if we apply KVL for each loop, we will find these equations :**  

### Equation for the first mesh :  

**2 - 1I₁ - 4 - 1(I₁-I₂) = 0**
**or, (1+1)I₁ - 1I₂ + 0 = 2 - 4**  

### Equation for 2nd mesh :  

**4 - 2I₂ - 3(I₂-I₃) - 1(I₂-I₁) = 0**  
**or, (1+2+3)I₂ - 1I₁ - 3I₃ = 4**  

#### Equation for 3rd mesh :  

**2 - 4I₃ - 3(I₃-I₂) = 0**  
**or, (3+4)I₃ - 3I₂ + 0 = 2**  

### Rewritten all the Equations :  

**2I₁ - I₂ + 0 = -2**  
**- I₁ + 6I₂  - I₃ = 4**  
**0 - 3I₂ + 7I₃ = 2**  

### Solving 

**We can solve these equations using Cramer's rule, Substitutio method, Elimination method and Calculator.**  

***[ In the case of Branch Analysis, we would assume individual currents I for the middle Branches instead of defining the current by two existing current.This is the difference between mesh analysis and branch analysis.]***


