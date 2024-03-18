## Quadrature Down Converter

**Overview:**
The quadrature down converter (QDC) illustrated in Fig. 1 is a fundamental component in modern wireless receivers (RX) such as Bluetooth, Wi-Fi, and WLAN. It facilitates interference mitigation and enhances communication quality. This project aims to implement a prototype QDC based on given specifications.
![image](https://github.com/priyamandot/Quadrature-Down-Converter/assets/139869341/24102b3d-9673-49c7-a898-16233eb4cf8f)

**Operation:**
In the depicted QDC setup, the input signal \( v_{in} = A_1 \cos(\omega_{int} t) \) is mixed with \( v_{OSCI} = A_2 \cos(\omega_{OSC} t) \) and \( v_{OSCQ} = A_2 \sin(\omega_{OSC} t) \) to generate in-phase (\( v_{IF I} \)) and quadrature-phase (\( v_{IF Q} \)) intermediate frequency (IF) signals. The in-phase and quadrature-phase signals maintain a 90° phase difference. The mixing process is equivalent to signal multiplication, as depicted by the equations:

\[v_{IF I} = v_{in} \times v_{OSCI} = \frac{A_1 A_2}{2} \left( \cos(\omega_{int} - \omega_{OSC} t) + \cos(\omega_{int} + \omega_{OSC} t) \right) \]
\[
v_{IF Q} = v_{in} \times v_{OSCQ} = \frac{A_1 A_2}{2} \left( \sin(\omega_{int} + \omega_{OSC} t) - \sin(\omega_{int} - \omega_{OSC} t) \right)
\]

**Functionality:**
The mixed signal undergoes low-pass filtering to isolate IF signals with frequency \( \omega_{IF} = (\omega_{IN} - \omega_{OSC}) \). The cutoff frequency \( \omega_{IF} \) is sufficiently low compared to \( \omega_{IN} \) and \( \omega_{osc} \), ensuring effective filtering. For instance, if \( f_{IN} = 2.4 \) GHz and \( f_{osc} = 2.401 \) GHz, then \( f_{IF} = 1 \) MHz.

1. **Quadrature Oscillator Design:**
Design a quadrature oscillator using op-amps to generate two sinusoidal signals (\( v_{OSCI} \) & \( v_{OSCQ} \)) at 100 kHz with a 90° phase difference and oscillation amplitude of 1 Vp−p.

2. **Switch (Mixer) Design:**
Utilize a MOSFET as a switch (mixer) as depicted in Fig. 2. The oscillator signal is applied to the gate, the input at the source, and the intermediate frequency output is extracted from the drain.

![image](https://github.com/priyamandot/Quadrature-Down-Converter/assets/139869341/bd703ff6-a3dc-45dd-9c84-15fd974cd5e6)

3. **Low Pass Filter Design:**
Design a low pass RC filter (LPF) with a -3 dB cutoff frequency of 2 kHz to effectively filter the mixed signal.

The project will include detailed designs, simulations, and verification steps for each component of the QDC.

