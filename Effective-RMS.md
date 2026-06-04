# Effective RMS 
In AC, voltage and current changes direction continuously, so their average values over a full cycle become zero, which does not represent the real power delivered. Since power depends on the square of voltage or current, it is always positive. Therefore, we use a mathematical concept called RMS (Root Mean Square) to represent an equivalent DC value that produces the same power effect as the AC signal.
In short, RMS is a way to find the “effective” or “equivalent” value of a changing signal.  
#### RMS is determined using three basic steps,  
In simple words  
**1)Square the values**  
*This removes negative signs (so everything becomes positive)*  
**2)Find the mean (average)**  
*Take the average of those squared values over time*  
**3)Take the square root**    
*This brings the value back to the original scale*  
### For any periodic function x(t) in general, the RMS value would be,  
$$
x_{\mathrm{RMS}} = \sqrt{\frac{1}{T} \int_{0}^{T} x^2(t)\, dt}
$$
### For AC sinusoidal voltage   
$$
V_{\mathrm{RMS}} = \sqrt{\frac{1}{T} \int_{0}^{T} v^2(t)\, dt}
$$
**Determined value:**  
$$
V_{\mathrm{RMS}} = \frac{V_{\mathrm{max}}}{\sqrt{2}}
$$
### For AC sinusoidal current   
$$
I_{\mathrm{RMS}} = \sqrt{\frac{1}{T} \int_{0}^{T} i^2(t)\, dt}
$$
**Determined value:**  
$$
I_{\mathrm{RMS}} = \frac{I_{\mathrm{max}}}{\sqrt{2}}
$$
