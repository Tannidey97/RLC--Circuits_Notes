# Transient Response of an RC Circuit: Capacitor Charging

## 1. What is a Transient Response?

A **transient response** is the temporary behaviour of an electrical circuit when it changes from one steady condition to another because of a sudden change or disturbance.

For example, when a DC supply is connected to an initially uncharged capacitor, the capacitor does not charge instantaneously. Its voltage and current change with time. The period during which these changes occur is called the **transient period**.

- **Transient state:** the temporary period during which voltage and current change with time.
- **Steady state:** the condition reached after the transient changes have practically disappeared.

In an RC charging circuit, the transient response describes how the capacitor gradually charges after the supply is connected.

---

## 2. Charging of a Capacitor in an RC Circuit

Consider a series RC circuit with:

- A DC voltage source $E$
- A resistor $R$
- A capacitor $C$
- A switch

Assume the capacitor is initially uncharged.

**At the moment the switch is closed ($t = 0$):**

- The capacitor voltage is zero.
- The entire supply voltage appears across the resistor.
- The charging current is maximum.

**As time increases:**

- The capacitor accumulates charge and its voltage rises.
- The voltage across the resistor falls.
- The charging current falls.

**After a long time:**

- The capacitor voltage approaches the supply voltage.
- The resistor voltage approaches zero.
- The charging current approaches zero.
- The circuit reaches steady state.

> For an ideal RC circuit, the capacitor approaches the supply voltage asymptotically. It never reaches it exactly in finite time.

---

## 3. Derivation of the Capacitor Charging Equation

Apply Kirchhoff's Voltage Law (KVL):

$$E = V_R + V_C$$

We know:

$$V_R = iR \qquad \text{and} \qquad i = C\frac{dV_C}{dt}$$

Substituting into KVL:

$$E = RC\frac{dV_C}{dt} + V_C$$

Rearranging:

$$RC\frac{dV_C}{dt} = E - V_C \quad\Rightarrow\quad \frac{dV_C}{dt} = \frac{E - V_C}{RC}$$

Separating the variables:

$$\frac{dV_C}{E - V_C} = \frac{dt}{RC}$$

Integrating both sides:

$$-\ln(E - V_C) = \frac{t}{RC} + K$$

**Finding the constant $K$.** At $t = 0$, $V_C = 0$, so:

$$-\ln(E) = K$$

Substituting $K$ back:

$$-\ln(E - V_C) + \ln(E) = \frac{t}{RC}$$

$$\ln\left(\frac{E}{E - V_C}\right) = \frac{t}{RC}$$

Taking the exponential of both sides:

$$\frac{E - V_C}{E} = e^{-t/RC}$$

$$E - V_C = E\,e^{-t/RC}$$

Rearranging:

$$V_C = E - E\,e^{-t/RC} = E\left(1 - e^{-t/RC}\right)$$

Since $RC$ is called the **time constant** $\tau$:

### Final Charging Equation

$$V_C = E\left(1 - e^{-t/\tau}\right), \qquad \tau = RC$$

Where:

| Symbol | Meaning | Unit |
|---|---|---|
| $V_C$ | Instantaneous capacitor voltage | V |
| $E$ | DC supply voltage | V |
| $e$ | Exponential constant (≈ 2.718) | none |
| $t$ | Elapsed time | s |
| $\tau$ | Time constant | s |

---

## 4. Physical Meaning of the Charging Equation

$$V_C = E\left(1 - e^{-t/\tau}\right)$$

This tells us how much voltage the capacitor has at any moment during charging.

**Meaning of $E$:** the supply voltage. It is the final voltage the capacitor approaches in an ideal RC circuit. If the supply is 10 V, the capacitor voltage gradually approaches 10 V.

**Meaning of $t$:** the time elapsed since the switch was closed. As time increases, the capacitor accumulates more charge and its voltage rises.

**Meaning of $\tau$ (time constant):** $\tau = RC$ controls how quickly the capacitor charges.

- Higher resistance → larger $\tau$ → slower charging.
- Higher capacitance → larger $\tau$ → slower charging.
- Lower resistance or capacitance → smaller $\tau$ → faster charging.

After **one time constant**, the capacitor voltage reaches approximately **63.2%** of its final value.

---

## 5. Why Does the Equation Contain $(1 - e^{-t/\tau})$?

Start with:

$$V_C = E\left(1 - e^{-t/\tau}\right)$$

Divide both sides by $E$:

$$\frac{V_C}{E} = 1 - e^{-t/\tau}$$

Rearranging:

$$\frac{E - V_C}{E} = e^{-t/\tau}$$

This has a clear physical interpretation:

- $\dfrac{V_C}{E}$ is the **fraction of the final voltage already achieved** by the capacitor.
- $\dfrac{E - V_C}{E}$ is the **fraction of the final voltage still left to gain**.

Together they account for everything:

$$\text{achieved fraction} + \text{remaining fraction} = 1$$

$$\frac{V_C}{E} + e^{-t/\tau} = 1$$

That is why the exponential is subtracted from 1. **The exponential term is the remaining voltage gap, not the capacitor voltage itself.**

### Why does the remaining gap shrink exponentially?

From KVL:

$$V_R = E - V_C$$

From Ohm's law:

$$i = \frac{V_R}{R} = \frac{E - V_C}{R}$$

Since $i = C\,\dfrac{dV_C}{dt}$:

$$\frac{dV_C}{dt} = \frac{E - V_C}{RC}$$

So the **rate at which the capacitor voltage rises depends on the remaining voltage gap**:

- Large gap → voltage rises quickly.
- Small gap → voltage rises slowly.

A quantity whose rate of change is proportional to its own size follows an exponential law. So the exponential term is not arbitrary: it describes how the remaining gap decreases with time.

---

## 6. The Two Curves in the Universal Time Constant Chart

**Curve 1 (decreasing):**

$$y = e^{-t/\tau}$$

This is the fraction of the initial voltage that still remains across the resistor:

$$\frac{V_R}{E} = e^{-t/\tau}$$

(During charging, this is the same as the remaining voltage gap from Section 5.)

**Curve 2 (increasing):**

$$y = 1 - e^{-t/\tau}$$

This is the fraction of the supply voltage the capacitor has achieved:

$$\frac{V_C}{E} = 1 - e^{-t/\tau}$$

The curves are complementary:

$$e^{-t/\tau} + \left(1 - e^{-t/\tau}\right) = 1$$

This comes directly from KVL. Dividing $E = V_R + V_C$ by $E$:

$$\frac{V_R}{E} + \frac{V_C}{E} = 1$$

As the capacitor voltage rises, the resistor voltage falls, and their sum always equals the supply voltage.

---

## 7. Important Values at Different Time Constants

Let the supply voltage be $E$.

| Time | Capacitor voltage | Resistor voltage |
|---|---|---|
| $0\tau$ | 0% of $E$ | 100% of $E$ |
| $1\tau$ | 63.2% of $E$ | 36.8% of $E$ |
| $2\tau$ | 86.5% of $E$ | 13.5% of $E$ |
| $3\tau$ | 95.0% of $E$ | 5.0% of $E$ |
| $4\tau$ | 98.2% of $E$ | 1.8% of $E$ |
| $5\tau$ | 99.3% of $E$ | 0.7% of $E$ |

### Why are 0.632 and 0.368 important?

At $t = \tau$:

$$e^{-1} \approx 0.368 \quad\Rightarrow\quad 1 - e^{-1} \approx 0.632$$

After one time constant, the capacitor has 63.2% of the supply voltage and the resistor has 36.8%.

**Example:** $E = 10\ \text{V}$

$$V_C = 10 \times 0.632 = 6.32\ \text{V}$$

$$V_R = 10 \times 0.368 = 3.68\ \text{V}$$

**KVL check:** $6.32 + 3.68 = 10\ \text{V}$ ✓

---

## 8. Why Is the Charging Curve Exponential?

The capacitor does not charge at a constant rate.

- At the start, the whole supply voltage is across the resistor, so the current is maximum.
- As the capacitor charges, $V_C$ rises, so $V_R = E - V_C$ falls.
- By Ohm's law, $i = V_R / R$, so the current falls too.
- A smaller current means slower charging.

So the capacitor charges quickly at first and then more and more slowly as it nears $E$. This gradual slowdown produces an exponential curve instead of a straight line.

---

## 9. Why Is It Called a Universal Time Constant Chart?

The horizontal axis is marked in multiples of $\tau$ ($0, \tau, 2\tau, \dots, 6\tau$), not in fixed seconds, because different RC circuits have different time constants.

**Circuit A:** $R = 1\ \text{k}\Omega,\ C = 1000\ \mu\text{F}$

$$\tau = RC = 1\ \text{s}$$

**Circuit B:** $R = 10\ \text{k}\Omega,\ C = 1000\ \mu\text{F}$

$$\tau = RC = 10\ \text{s}$$

Both follow the same curve shape, but Circuit B takes ten times longer. The chart works for any RC circuit once you calculate its $\tau$.

---

## 10. Summary

| Quantity | Expression |
|---|---|
| Time constant | $\tau = RC$ |
| Capacitor voltage | $V_C = E\left(1 - e^{-t/\tau}\right)$ |
| Resistor voltage | $V_R = E\,e^{-t/\tau}$ |
| Charging current | $i = \dfrac{E}{R}\,e^{-t/\tau}$ |

- At $t = \tau$: $V_C = 63.2\%$ of $E$, $V_R = 36.8\%$ of $E$.
- At about $5\tau$: the capacitor is practically fully charged (a standard engineering rule of thumb, not an exact value).

### The Central Concept

- $e^{-t/\tau}$ = the fraction of the voltage gap **still remaining**.
- $1 - e^{-t/\tau}$ = the fraction of the final voltage **already achieved**.

$$V_C = E\left(1 - e^{-t/\tau}\right)$$

means

> **Capacitor voltage = Supply voltage × Fraction of final voltage achieved**
