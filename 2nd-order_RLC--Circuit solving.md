# The Source-Free Series $RLC$ Circuit

A **source-free series $RLC$ circuit** occurs when its external independent sources are disconnected for $t > 0$.

https://github.com/Tannidey97/RLC--Circuits_Notes/blob/main/IMG_20260603_202122_879.jpg

The circuit's response depends entirely on the energy initially stored in the capacitor (initial voltage $V_0$) and the inductor (initial current $I_0$).

---

## 1. Deriving the Governing Differential Equation

By applying **Kirchhoff’s Voltage Law (KVL)** around the loop, the sum of all element voltages must equal zero:

$$Ri(t) + v_L(t) + v_C(t) = 0$$

Substituting the standard voltage-current relationships for the inductor ($v_L = L \frac{di}{dt}$) and the capacitor ($v_C = \frac{1}{C}\int_{\infty}^{t} i(\tau)d\tau$):

$$Ri + L\frac{di}{dt} + \frac{1}{C}\int_{\infty}^{t} i(\tau)d\tau = 0$$

To eliminate the integral, we differentiate the entire equation with respect to time ($t$) and divide through by $L$:

$$\frac{d^2i}{dt^2} + \frac{R}{L}\frac{di}{dt} + \frac{1}{LC}i = 0$$

This is a **second-order linear homogeneous differential equation**.

---

## 2. Establishing Initial Conditions

Every second-order system requires **two initial conditions** to solve for its constants: $i(0)$ and $\frac{di(0)}{dt}$.

1. **Initial Current:** $$i(0) = I_0$$
2. **Initial Derivative of Current:** Evaluated from the original KVL equation at $t = 0^+$:
   $$Ri(0) + L\frac{di(0)}{dt} + V_0 = 0 \implies \frac{di(0)}{dt} = -\frac{1}{L}(RI_0 + V_0)$$

---

## 3. The Characteristic Equation & Key Parameters

Assuming a trial solution of exponential form $i = Ae^{st}$ and substituting it back into the differential equation gives the **characteristic equation**:

$$s^2 + \frac{R}{L}s + \frac{1}{LC} = 0$$

Using the quadratic formula, the characteristic roots ($s_1, s_2$) are:

$$s_{1,2} = -\frac{R}{2L} \pm \sqrt{\left(\frac{R}{2L}\right)^2 - \frac{1}{LC}}$$

### Key Parameters
To simplify circuit analysis, we define two fundamental frequencies:
* **Neper Frequency (Damping Factor), $\alpha$:** $$\alpha = \frac{R}{2L}$$
* **Resonant Natural Frequency, $\omega_0$:** $$\omega_0 = \frac{1}{\sqrt{LC}}$$

Expressing the roots in terms of $\alpha$ and $\omega_0$:

$$s_{1,2} = -\alpha \pm \sqrt{\alpha^2 - \omega_0^2}$$

---

## 4. The Three Response Types

Depending on the relationship between $\alpha$ and $\omega_0$, the physical response of the circuit falls into one of three distinct cases:

PASTE_YOUR_RESPONSE_CURVES_GRAPH_PHOTO_LINK_HERE

### Case I: Overdamped ($\alpha > \omega_0$)
* **Condition:** $\left(\frac{R}{2L}\right)^2 > \frac{1}{LC}$
* **Roots:** Real, distinct, and negative ($s_1 \neq s_2$).
* **Behavior:** The system returns to steady-state sluggishly without any oscillation.
* **Equation:** $$i(t) = A_1e^{s_1t} + A_2e^{s_2t}$$

### Case II: Critically Damped ($\alpha = \omega_0$)
* **Condition:** $\left(\frac{R}{2L}\right)^2 = \frac{1}{LC}$
* **Roots:** Real, equal roots ($s_1 = s_2 = -\alpha$).
* **Behavior:** The system returns to equilibrium in the fastest possible time without oscillating.
* **Equation:** $$i(t) = (A_2 + A_1t)e^{-\alpha t}$$

### Case III: Underdamped ($\alpha < \omega_0$)
* **Condition:** $\left(\frac{R}{2L}\right)^2 < \frac{1}{LC}$
* **Roots:** Complex conjugate pairs ($s_{1,2} = -\alpha \pm j\omega_d$).
* **Damped Natural Frequency:** $\omega_d = \sqrt{\omega_0^2 - \alpha^2}$
* **Behavior:** The circuit current oscillates back and forth within a decaying exponential envelope.
* **Equation:** $$i(t) = e^{-\alpha t}(B_1\cos\omega_dt + B_2\sin\omega_dt)$$

---

## 5. Workflow Checklist for Problems
1. Determine the values of $R$, $L$, and $C$.
2. Calculate $\alpha$ and $\omega_0$.
3. Compare $\alpha$ and $\omega_0$ to choose the matching response formula.
4. Calculate your initial conditions: $i(0)$ and $\frac{di(0)}{dt}$.
5. Set up the algebraic system equations to solve for the arbitrary constants ($A_1, A_2$ or $B_1, B_2$).
