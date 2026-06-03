 # The Source-Free Parallel $RLC$ Circuit

A **source-free parallel $RLC$ circuit** occurs when all three basic elements (resistor, inductor, and capacitor) are connected in parallel across each other, and independent external sources are disconnected for $t > 0$. The behavior depends entirely on the initial energy stored in the inductor (initial current $I_0$) and capacitor (initial voltage $V_0$).

---

## 1. Deriving the Governing Differential Equation

Since all components are connected in parallel, they share the **same voltage $v(t)$** across their nodes. 

Applying **Kirchhoff’s Current Law (KCL)** at the top node, the sum of all currents leaving the node must equal zero:

$$\frac{v(t)}{R} + i_L(t) + i_C(t) = 0$$

Substituting the standard voltage-current relationships for the inductor ($i_L = \frac{1}{L}\int_{-\infty}^{t} v(\tau)d\tau$) and the capacitor ($i_C = C \frac{dv}{dt}$):

$$\frac{v}{R} + \frac{1}{L}\int_{-\infty}^{t} v(\tau)d\tau + C\frac{dv}{dt} = 0$$

To eliminate the integral, we differentiate the entire equation with respect to time ($t$) and divide through by $C$:

$$\frac{d^2v}{dt^2} + \frac{1}{RC}\frac{dv}{dt} + \frac{1}{LC}v = 0$$

This is a **second-order linear homogeneous differential equation** in terms of the circuit voltage $v(t)$.

---

## 2. Establishing Initial Conditions

To find the constants for the voltage response, we need **two initial conditions**: $v(0)$ and $\frac{dv(0)}{dt}$.

1. **Initial Voltage:** $$v(0) = V_0$$
2. **Initial Derivative of Voltage:** Evaluated from the original KCL equation at $t = 0^+$:
   $$\frac{V_0}{R} + I_0 + C\frac{dv(0)}{dt} = 0 \implies \frac{dv(0)}{dt} = -\frac{V_0 + RI_0}{RC}$$

---

## 3. The Characteristic Equation & Key Parameters

Assuming a trial solution of exponential form $v = Ae^{st}$ and substituting it back into the differential equation gives the **characteristic equation**:

$$s^2 + \frac{1}{RC}s + \frac{1}{LC} = 0$$

Using the quadratic formula, the characteristic roots ($s_1, s_2$) are:

$$s_{1,2} = -\frac{1}{2RC} \pm \sqrt{\left(\frac{1}{2RC}\right)^2 - \frac{1}{LC}}$$

### Key Parameters
While $\omega_0$ remains identical to the series circuit, the damping coefficient $\alpha$ changes due to the parallel connection:
* **Neper Frequency (Damping Factor), $\alpha$:** $$\alpha = \frac{1}{2RC}$$
* **Resonant Natural Frequency, $\omega_0$:** $$\omega_0 = \frac{1}{\sqrt{LC}}$$

Expressing the roots in terms of $\alpha$ and $\omega_0$:

$$s_{1,2} = -\alpha \pm \sqrt{\alpha^2 - \omega_0^2}$$

---

## 4. The Three Response Types

Depending on the relationship between $\alpha$ and $\omega_0$, the physical voltage response $v(t)$ falls into one of three distinct cases:

### Case I: Overdamped ($\alpha > \omega_0$)
* **Condition:** $L > 4R^2C$
* **Roots:** Real, distinct, and negative ($s_1 \neq s_2$).
* **Behavior:** The voltage returns to zero smoothly without any oscillation.
* **Equation:** $$v(t) = A_1e^{s_1t} + A_2e^{s_2t}$$

### Case II: Critically Damped ($\alpha = \omega_0$)
* **Condition:** $L = 4R^2C$
* **Roots:** Real, equal roots ($s_1 = s_2 = -\alpha$).
* **Behavior:** The voltage returns to equilibrium in the fastest possible time without oscillating.
* **Equation:** $$v(t) = (A_1 + A_2t)e^{-\alpha t}$$

### Case III: Underdamped ($\alpha < \omega_0$)
* **Condition:** $L < 4R^2C$
* **Roots:** Complex conjugate pairs ($s_{1,2} = -\alpha \pm j\omega_d$).
* **Damped Natural Frequency:** $\omega_d = \sqrt{\omega_0^2 - \alpha^2}$
* **Behavior:** The voltage oscillates back and forth within a decaying exponential envelope.
* **Equation:** $$v(t) = e^{-\alpha t}(A_1\cos\omega_dt + A_2\sin\omega_dt)$$

---

## 5. Workflow Checklist for Problems
1. Determine the values of $R$, $L$, and $C$.
2. Calculate $\alpha = \frac{1}{2RC}$ and $\omega_0 = \frac{1}{\sqrt{LC}}$.
3. Compare $\alpha$ and $\omega_0$ to choose the matching response formula (**Over**, **Critical**, or **Under**).
4. Calculate your initial conditions: $v(0)$ and $\frac{dv(0)}{dt}$.
5. Set up the algebraic system equations to solve for the arbitrary constants ($A_1, A_2$).
