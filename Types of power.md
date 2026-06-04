# Real Power 

***Real power (active power) is the actual power in an AC circuit that is consumed by the load and converted into useful work such as heat, light, or mechanical energy.***  
***In AC circuit, the average power is the actual power which is consumed by the load. So average power is the real power.***   

Hence, Real power,  

$$P = V_{\text{rms}} I_{\text{rms}} \cos(\theta_v - \theta_i)$$

# Apparent Power 

**The Average power equation,**

$$P = V_{\text{rms}} I_{\text{rms}} \cos(\theta_v - \theta_i)$$

Here,  
***The product of RMS voltage and RMS current represent a concept called Apparent power.  
Apparent power is the total amount of power that is supplied by the source.***  

Apparent power is denoted by S,  
$$S = V_{\text{rms}} I_{\text{rms}}$$

# Power Factor 

***Power factor represents the phase difference between the voltage and current, and it basically shows how much of apparent power has converted into real power.***  

For Example,  
If power factor = P / S = cosθ = 0.8  

***Meaning of this result:***  

**Only 80% of the supplied power is doing useful work.**  
**The remaining 20% is associated with reactive effects (stored and returned energy).**   

# Reactive Powerer

**Reactive power is the power that flows back and forth between the source and reactive elements without producing useful work. It is a part of total supplied power/apparent power but it doesn't contribute in converting energy. It oscillates between source and reactive elements like capacitor, inductor.**  
Its like,  
**Reactive power = Apparent power - Real Power**  


# Complex Power 
**In AC electrical circuits, complex power is a way of representing both the real power and reactive power in a single complex quantity.** 
**Complex power is the product of rms voltage (V) and complex conjugate of rms current (I)**  

$$
S = V_{rms} I_{rms}^{*}
$$

## RMS Phasors

**We know that for a sinusoidal voltage an current the RMS would be,**   

$$\mathbf{V}_{\text{rms}} = \frac{\mathbf{V}}{\sqrt{2}} = V_{\text{rms}} \angle \theta_v$$

$$\mathbf{I}_{\text{rms}} = \frac{\mathbf{I}}{\sqrt{2}} = I_{\text{rms}} \angle \theta_i$$

---

## Complex Power Equations

$$\mathbf{S} = V_{\text{rms}} I_{\text{rms}} \angle (\theta_v - \theta_i) = V_{\text{rms}} I_{\text{rms}} \cos(\theta_v - \theta_i) + j V_{\text{rms}} I_{\text{rms}} \sin(\theta_v - \theta_i)$$

 **Complex power can be expressed in terms of the load impedance**    
 
$$\mathbf{Z} = \frac{\mathbf{V}}{\mathbf{I}} = \frac{\mathbf{V}_{\text{rms}}}{\mathbf{I}_{\text{rms}}} = \frac{V_{\text{rms}}}{I_{\text{rms}}} \angle (\theta_v - \theta_i)$$

Thus, V_{rms} = Z I_{rms}^{*}  Substituting Z,  

$$\mathbf{S} = I_{\text{rms}}^2 \mathbf{Z} = \frac{V_{\text{rms}}^2}{\mathbf{Z}^*} = \mathbf{V}_{\text{rms}} \mathbf{I}_{\text{rms}}^*$$

Since Z = R + jX,  

$$\mathbf{S} = I_{\text{rms}}^2 (R + jX) = P + jQ$$

---

## Real and Reactive Power Components

**P represent the Real part and Q represent the Imaginary part of the complex power,**  

$$P = \text{Re}(\mathbf{S}) = I_{\text{rms}}^2 R$$

$$Q = \text{Im}(\mathbf{S}) = I_{\text{rms}}^2 X$$

**As P depends on load resistance R, It is the average or real power and since Q depends on load's reactance X, It is called the reactive power.**  

$$P = V_{\text{rms}} I_{\text{rms}} \cos(\theta_v - \theta_i)$$

$$Q = V_{\text{rms}} I_{\text{rms}} \sin(\theta_v - \theta_i)$$

**Notice that,**  
***1) Q = 0 for resistive loads(unity pf)***  
***2) Q < 0 for capacitive loads(leading pf)*** 
***3) Q > 0 for inductive loads (lagging pf)*** 

# AC Power Analysis Summary

## Hence, Complex enables us to obtain the real and reactive powers directly from Voltage and current phasors.  

### Complex Power ($\mathbf{S}$)
$$\mathbf{S} = P + jQ = \mathbf{V}_{\text{rms}}(\mathbf{I}_{\text{rms}})^* = |\mathbf{V}_{\text{rms}}||\mathbf{I}_{\text{rms}}| \angle (\theta_v - \theta_i)$$

### Apparent Power ($S$)
$$S = |\mathbf{S}| = |\mathbf{V}_{\text{rms}}||\mathbf{I}_{\text{rms}}| = \sqrt{P^2 + Q^2}$$

### Real Power ($P$)
$$P = \text{Re}(\mathbf{S}) = S \cos(\theta_v - \theta_i)$$

### Reactive Power ($Q$)
$$Q = \text{Im}(\mathbf{S}) = S \sin(\theta_v - \theta_i)$$

### Power Factor ($\text{pf}$)
$$\text{Power Factor} = \frac{P}{S} = \cos(\theta_v - \theta_i)$$



