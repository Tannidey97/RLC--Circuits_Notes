# Nodal Analysis 

**Nodal analysis is a circuit analysis method used to determine the voltage at each node of an electrical circuit by applying Kirchhoff's Current Law (KCL).**
 **We apply KCL at the nodes to determine Voltage at that node.**
 
**[The number of nodes for which the voltage must be determined using nodal analysis is 1 less than the total number of nodes. So the number of equations required to solve for all the nodal voltages of a network is 1 less than the total number of independent nodes.]**

# Analysis Procedure 

### Identify all the nodes.

**Find every point where two or more elements are connected.**  

### Choose a reference (ground) node.

**Select one node as 0 V (ground).**
[Usually, choose the node connected to the most elements because it makes the equations simpler.]  

### Assign voltages to the remaining nodes.

**Label the remaining node voltages as V₁, V₂, V₃, ...**  
**These are the unknown Voltages which need to be solved.**  

### Apply KCL at each unknown node 

The rule is : 
***The total current entering a node is equal to the total current leaving the node.***  
                                  **I(entering) = I(leaving)**  

**Write each current using Ohm's Law.**  
                   **I = Voltage / Resistance**

# Solving method through a simple Circuit 

https://github.com/Tannidey97/RLC--Circuits_Notes/blob/main/IMG_20260707_121513_219.jpg

**Converting the voltage source into current source for convenient in solving :**  

https://github.com/Tannidey97/RLC--Circuits_Notes/blob/main/IMG_20260707_121523_503.jpg

**We got 4 nodes in the circuit diagram. According to the analysis procedure, the node at the bottom is assumed 0V or grounded as it is connected to the all branches of the circuit.**  

The equations would be :   

## Equation for first node  

**At first node voltage is V₁ & 20A current source is connected. Assuming I₁, I₂, I₃ is leaving the node through 12(ohm), 6(ohm) & 4(ohm) resistor respectively and 20A is entering the node we can write the equation like :**

**20 = I₁ + I₂ + I₃**  
**or, 20 = V₁/12 + V₁/6 + (V₁-V₂)/4**  
**or, V₁(1/12+1/6+1/4) - V₂/4 + 0 = 20**  

## Equation for 2nd node 

**At the 2nd node voltage is V₂ is assumed. Assuming currents I₃, I₄, I₅ leaving the node through 4(ohm), 6(ohm), 1(ohm) respectively. we can write the equation like:**

 **I₃ + I₄ + I₅ = 0** 
**or, (V₂ - V₁)/4 + V₂/6 + (V₂ - V₃)/1 = 0**  
**or, V₂(1/4+1/6+1/1) - V₁(1/4) - V₃(1/1) = 0**

## Equation for the 3rd node 

**At the 3rd node V₃ voltage is assumed. Assuming I₅ , I₆ currents are leaving the node through 1(ohm) and 2(ohm). The equation would be :** 

**I₅ + I₆ = 0**  
**or, (V₃ - V₂)/1 + V₃/2 = 0**  
**or, V₃(1/1+1/2) - V₂/1 = 0**  

## Final Equations 

### V₁(1/12+1/6+1/4) -      V₂/4      +       0    = 20

###    -V₁(1/4)    +   V₂(1/4+1/6+1/1) - V₃(1/1)     = 0

###     0         -    V₂/1      +       V₃(1/1+1/2) = 0**
 
## Solving 

**Using Cramer's rule, Substitution, Elimination, Calculator we can solve these equations.**
 



