# Instantaneous power 
The Instantaneous power absorbed by an element is the product of the instantaneous voltage v(t) across the element and instantaneous current i(t) through it.
***p(t) = v(t)i(t)***
[The instantaneous power is the power at any instant of time. It is the rate at which an element absorbs energy.]
# For an AC circuit 
Lets Consider the case of instantaneous power absorbed by an arbitrary combination of circuit elements. The circuit contains sinusoidal AC voltage and AC current.
***v(t) = Vₘ cos(ωt + θᵥ)***  
***i(t) = Iₘ cos(ωt + θᵢ)***  
The Instantaneous Power would be,   
***p(t) =  VₘIₘcos(ωt + θᵥ)cos(ωt + θᵢ)***  
**By Using Trigonometric formula we get,**  
***p(t) = 1 / 2 VₘIₘ cos(θᵥ - θᵢ) + 1 / 2 VₘIₘ cos(2ωt + θᵥ + θᵢ)***  
[formula : cosA cosB = 1 / 2 {cos(A - B) + cos(A + B)}]   
In AC circuit the power continuously changes with time as it depends on voltage and current. But in real life we need to know at least the approximate capability of an electrical instrument of converting electrical energy. So we use average power to know the capability.  
From the instantaneous power formula we get two parts, one is time independent and the other is time dependent. The first part of the formula refers the part of a power which remains constant across the whole period. This constant part can help us to know an approximate amount of supplied power which is called average power.
If we want to determine average power for a period T, we can add all the constant part of the instantaneous power p(t) until time T.  
So, we can do,  
            $$P = \frac{1}{T} \int_{0}^{T} p(t) \, dt$$
### If we derive this,  
$$P = \frac{1}{T} \int_{0}^{T} \frac{1}{2} V_m I_m \cos(\theta_v - \theta_i) \, dt + \frac{1}{T} \int_{0}^{T} \frac{1}{2} V_m I_m \cos(2\omega t + \theta_v + \theta_i) \, dt$$

$$P = \frac{1}{2} V_m I_m \cos(\theta_v - \theta_i) \frac{1}{T} \int_{0}^{T} dt + \frac{1}{2} V_m I_m \frac{1}{T} \int_{0}^{T} \cos(2\omega t + \theta_v + \theta_i) \, dt$$

### From the derivation we the formula of Average Power Formula (Time Domain)
$$P = \frac{1}{2} V_m I_m \cos(\theta_v - \theta_i)$$

### Phasor / Complex Power Relation  
If we write the formula in phasor form,  
$$\frac{1}{2} \mathbf{V}\mathbf{I}^* = \frac{1}{2} V_m I_m \angle(\theta_v - \theta_i)$$

$$\frac{1}{2} \mathbf{V}\mathbf{I}^* = \frac{1}{2} V_m I_m \left[ \cos(\theta_v - \theta_i) + j \sin(\theta_v - \theta_i) \right]$$

$$P = \frac{1}{2} \text{Re}[\mathbf{V}\mathbf{I}^ *] = \frac{1}{2} V_m I_m \cos(\theta_v - \theta_i)$$

### Case 1: For Purely Resistive Circuit ($\theta_v = \theta_i$)
$$P = \frac{1}{2} V_m I_m = \frac{1}{2} I_m^2 R = \frac{1}{2} |\mathbf{I}|^2 R$$

### Case 2: For Purely Reactive Circuit ($\theta_v - \theta_i = \pm 90^\circ$)
$$P = \frac{1}{2} V_m I_m \cos(90^\circ) = 0$$         
            
### For an ideal capacitor or inductor, the average power over one complete cycle is zero because they store energy temporarily and then return it to the source, rather than consuming it.

#### Resistor: Converts electrical energy into heat → consumes real power.
#### Inductor/Capacitor: Only exchange energy with the source → consume no net energy.
