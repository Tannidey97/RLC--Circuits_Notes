# Solving Second-Order Circuits: Step-by-Step Complete Response (Example 8.9)

This note details the complete response analysis ($v(t)$ and $i(t)$) for a second-order circuit experiencing a switching event at $t = 0$. It breaks down the problem using the standard 4-phase chronological methodology ($t < 0$, $t = 0^+$, $t \to \infty$, and $t > 0$).

---

## 1. Circuit Analysis at Steady State ($t = 0^-$)

https://github.com/Tannidey97/RLC--Circuits_Notes/blob/main/IMG_20260603_202122_879.jpg


# Before the switch changes positions, the circuit is connected to the $12\text{ V}$ DC source for a very long time ($t < 0$). Under DC steady-state conditions:
* **Inductors** act as a **short circuit**.
* **Capacitors** act as an **open circuit**.
* The **switch** is **open**.

Because the capacitor blocks DC current path at steady state, no current can flow through the main loop. 
* Inductor current:  
  $$i(0^-) = 0\text{ A}$$
* Capacitor voltage (by KVL, it charges fully to match the source):  
  $$v(0^-) = 12\text{ V}$$

---

## 2. Establishing Initial Conditions ($t = 0^+$)

According to the laws of energy conservation, the state variables (inductor current and capacitor voltage) cannot change instantaneously. Thus:
* **Capacitor Voltage Continuity:** $$v(0^+) = v(0^-) = 12\text{ V}$$
* **Inductor Current Continuity:** $$i(0^+) = i(0^-) = 0\text{ A}$$

### Finding the First Time Derivative: $\frac{dv(0^+)}{dt}$
Right after the switch closes ($t = 0^+$), we apply Kirchhoff's Current Law (KCL) at node $a$ (the node above the $2\ \Omega$ resistor):

$$i(0^+) = i_C(0^+) + \frac{v(0^+)}{2}$$

Substitute our known boundary conditions ($i(0^+) = 0$ and $v(0^+) = 12\text{ V}$):

$$0 = i_C(0^+) + \frac{12}{2} \implies i_C(0^+) = -6\text{ A}$$

Using the capacitor's fundamental $i\text{-}v$ relationship ($i_C = C\frac{dv}{dt}$):

$$\frac{dv(0^+)}{dt} = \frac{i_C(0^+)}{C} = \frac{-6}{0.5} = -12\text{ V/s}$$

---

## 3. Finding Final Steady-State Values ($t \to \infty$)

Long after the switch closes ($t \to \infty$), the circuit settles into a new DC steady state. 
* **Inductors** revert to a **short circuit**.
* **Capacitors** revert to an **open circuit**.

The $12\text{ V}$ independent source remains active in the system. The remaining active loop consists only of the source, the $4\ \Omega$ resistor, and the parallel $2\ \Omega$ resistor branch.
* Final Inductor Current:  
  $$i(\infty) = \frac{12}{4 + 2} = 2\text{ A}$$
* Final Capacitor Voltage (taken across the parallel $2\ \Omega$ branch):  
  $$v(\infty) = 2 \cdot i(\infty) = 2(2) = 4\text{ V}$$

---

## 4. Deriving the Transient Behavior ($t > 0$)

To find the natural response characteristics, we deactivate the independent source ($12\text{ V}$ voltage source $\to$ replaced by a short circuit).

1. Apply KCL at node $a$:
   $$i = \frac{v}{2} + C\frac{dv}{dt} \implies i = \frac{v}{2} + \frac{1}{2}\frac{dv}{dt}$$

2. Apply KVL around the left mesh:
   $$4i + L\frac{di}{dt} + v = 0 \implies 4i + 1\frac{di}{dt} + v = 0$$

Substituting the KCL expression for $i$ into the KVL mesh equation yields our second-order homogeneous differential equation:

$$\frac{d^2v}{dt^2} + 5\frac{dv}{dt} + 6v = 0$$

### The Characteristic Equation & Roots
From the differential equation, we extract the characteristic equation:

$$s^2 + 5s + 6 = 0 \implies (s + 2)(s + 3) = 0$$

The roots are **$s_1 = -2$** and **$s_2 = -3$**. Because the roots are distinct, real, and negative, the transient response is **overdamped**:

$$v_n(t) = Ae^{-2t} + Be^{-3t}$$

---

## 5. Formulating the Complete Solution

The complete response matches the mathematical structure: $\text{Total Response} = \text{Steady-State Response } (v_{ss}) + \text{Transient Response } (v_n)$.

$$v(t) = v(\infty) + v_n(t)$$
$$v(t) = 4 + Ae^{-2t} + Be^{-3t}$$

### Evaluating Constants $A$ and $B$
Using the initial boundary condition $v(0) = 12\text{ V}$:
$$12 = 4 + A + B \implies A + B = 8 \quad \text{--- (Eq. 1)}$$

Differentiating the complete expression for $v(t)$:
$$\frac{dv(t)}{dt} = -2Ae^{-2t} - 3Be^{-3t}$$

Using the initial boundary condition $\frac{dv(0)}{dt} = -12\text{ V/s}$:
$$-12 = -2A - 3B \implies 2A + 3B = 12 \quad \text{--- (Eq. 2)}$$

Solving the linear algebraic system (**Eq. 1** and **Eq. 2**):
* $A = 12$
* $B = -4$

---

## Final Output Expressions ($t > 0$)

### Complete Capacitor Voltage Response:
$$v(t) = 4 + 12e^{-2t} - 4e^{-3t}\text{ V}$$

### Complete Inductor Current Response:
Obtained by substituting $v(t)$ and its derivative back into the KCL equation ($i = \frac{v}{2} + \frac{1}{2}\frac{dv}{dt}$):
$$i(t) = 2 - 6e^{-2t} + 4e^{-3t}\text{ A}$$
