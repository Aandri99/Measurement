Measuring inductance
============================

Objective
---------------
In this section, we will discuss the measurement of inductance, which is a fundamental property of electrical circuits. Inductance is a measure of an object's ability to store electrical energy in a magnetic field, and it is expressed in henries (H).

Background
---------------
Inductance measurement is essential in many areas of electrical engineering, including power transmission, signal processing, and electronic circuit design. Inductance measurement can be challenging due to various factors, including stray inductance, parasitic inductance, and measurement instrument limitations.

Stray Inductance: A Frequently Encountered Obstacle in Inductance Measurement
-----------------
Stray inductance is a frequently encountered obstacle in inductance measurement, particularly in high-frequency applications. For example, in radio frequency (RF) circuits, stray inductance can cause signal loss and affect the performance of the circuit. To minimize the effect of stray inductance in RF circuits, designers may use specialized components, such as air-core inductors and ferrite beads, and place them in a way that minimizes coupling between the components and their surroundings.

In addition to isolation and shielding, other techniques can also be used to reduce the effect of stray inductance on inductance measurement. One such technique is calibration, which involves measuring the inductance of a known reference object and using this value to correct for the effect of stray inductance. This can be done using a specialized instrument, such as an inductance meter or a network analyzer, which can measure the inductance of the reference object and calculate the correction factor.

Another technique that can be used to minimize the effect of stray inductance is to use guard traces. Guard traces involve placing a conductive shield around the object being measured to isolate it from external conductive objects. This shield is connected to a low-impedance ground, which prevents stray inductance from affecting the measurement signal. Guard traces are particularly effective in low-frequency applications, where the inductance of the shield can be made large enough to effectively isolate the object being measured from its surroundings.

In summary, stray inductance is a frequently encountered obstacle in inductance measurement, and can significantly affect the accuracy and precision of the measurement. To minimize the effect of stray inductance, designers and engineers must use isolation and shielding techniques, as well as calibration and guardring techniques, to reduce the coupling between the object being measured and its surroundings. By taking these steps, researchers and engineers can improve the reliability and validity of their measurements and make more informed decisions based on the data.

Parasitic Inductance: An Additional Cause of Inaccuracy
-----------------
Parasitic inductance is another common cause of inaccuracy in inductance measurement. Parasitic inductance arises due to the layout and design of the circuit, and is typically caused by unintentional inductance in the conductive traces, components, and other elements of the circuit.

Parasitic inductance can cause a range of errors in electronic circuits, including signal distortion, reduced bandwidth, and reduced signal-to-noise ratio. To minimize the effect of parasitic inductance, designers and engineers must carefully consider the layout and design of the circuit, and use specialized components and techniques to reduce its impact.

One technique that can be used to reduce the effect of parasitic inductance is to use components with low inductance values, such as surface-mount inductors or multilayer ceramic inductors. These components have a smaller physical size and lower parasitic inductance than traditional through-hole components, making them ideal for high-frequency applications where parasitic inductance can be a significant source of error.

Another technique that can be used to reduce the effect of parasitic inductance is to use ground planes and power planes in the circuit layout. Ground planes and power planes are large conductive planes that are placed adjacent to the circuit board, and help to reduce the inductance of the conductive traces by providing a low-inductance path for current flow.

In addition to these techniques, designers and engineers may also use specialized simulation tools, such as SPICE (Simulation Program with Integrated Circuit Emphasis), to model the effect of parasitic inductance on the circuit and optimize the circuit design to minimize its impact. By taking these steps, researchers and engineers can improve the accuracy and precision of electronic circuits, and reduce the likelihood of errors and erroneous conclusions based on flawed data.


Measurement Instrument Limitations
-----------------
Measurement instrument limitations can also affect the accuracy of inductance measurements. These limitations can arise due to factors such as the accuracy of the measurement instrument, the noise in the measurement system, and the measurement range of the instrument. It is essential to use a high-precision inductance meter that is well-calibrated and properly maintained to ensure accurate measurements.


The Bridge Method
-----------------
The bridge method is a widely used technique for inductance measurement. In this method, a bridge circuit is used to measure the inductance by comparing it to a known reference inductor. The bridge circuit consists of four arms, one of which contains the unknown inductance, and the other three arms contain resistors and a reference inductor. The bridge circuit is balanced by adjusting the resistors until the bridge output voltage is zero. The inductance is then calculated based on the resistances and the known reference inductance.

The Resonant Method
------------------------
The resonant method involves applying an AC voltage to the unknown inductor and measuring the resulting current. The inductance is then calculated using the following equation:

.. math:: L = \frac{1}{4\pi^2 f^2 C}

where f is the frequency of the applied voltage and C is a known reference capacitor.

Experiment: Measuring Inductance using Red Pitaya and Resonant Method
------------------------
In this experiment, we will use the resonant method to measure the inductance of an unknown inductor using the Red Pitaya board.
Wire the unknown inductor in series with a known capacitor to form a resonant circuit.The resonant frequency of a series resonant circuit is given by the equation:??

.. math:: f_res = 1/(2pisqrt(L*C))

To measure the inductance of an unknown inductor using the resonant method, we need to first determine the resonant frequency of the circuit. This can be done by sweeping the frequency of the AC voltage applied to the circuit using the Red Pitaya board and measuring the resulting current through the circuit. When the frequency of the applied voltage is equal to the resonant frequency, the current through the circuit will be at its maximum.

Once we have determined the resonant frequency, we can calculate the inductance of the unknown inductor using the resonant frequency and the known capacitance of the reference capacitor. For example, if the resonant frequency is found to be 10 kHz and the reference capacitor has a value of 1 microfarad, then the inductance can be calculated as follows:

.. math:: L = 1/(4pi^2f_res^2*C)
.. math:: L = 1/(4pi^2(10,000 Hz)^2*(1x10^-6 F))
.. math:: L = 39.8 microhenries

Therefore, the inductance of the unknown inductor is approximately 39.8 microhenries.

Written by Andra?? Pirc

This teaching material was created by `Red Pitaya <https://www.redpitaya.com/>`_ & `Zavod 404 <https://404.si/>`_ in the scope of the `Smart4All <https://smart4all.fundingbox.com/>`_ innovation project.
