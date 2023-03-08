Measuring capacitance
============================

Objective
---------------
In this section, we will discuss the measurement of capacitance, which is a fundamental property of electrical circuits. Capacitance is a measure of an object's ability to store electrical charge, and it is expressed in farads (F).

Background
---------------
Capacitance measurement is essential in many areas of electrical engineering, including power transmission, signal processing, and electronic circuit design. Capacitance measurement can be challenging due to various factors, including stray capacitance, parasitic capacitance, and measurement instrument limitations.

Stray Capacitance: A Common Challenge in Capacitance Measurement
---------------
Stray capacitance is a common challenge in capacitance measurement, particularly in high-frequency applications. For example, in radio frequency (RF) circuits, stray capacitance can cause signal loss and affect the performance of the circuit. To minimize the effect of stray capacitance in RF circuits, designers may use specialized components, such as air-core inductors and ceramic capacitors, and place them in a way that minimizes coupling between the components and their surroundings.

In addition to isolation and shielding, other techniques can also be used to reduce the effect of stray capacitance on capacitance measurement. One such technique is calibration, which involves measuring the capacitance of a known reference object and using this value to correct for the effect of stray capacitance. This can be done using a specialized instrument, such as a capacitance meter or a network analyzer, which can measure the capacitance of the reference object and calculate the correction factor.

Another technique that can be used to minimize the effect of stray capacitance is guardring. Guardring involves placing a conductive shield around the object being measured to isolate it from external conductive objects. This shield is connected to a low-impedance ground, which prevents stray capacitance from affecting the measurement signal. Guardring is particularly effective in low-frequency applications, where the capacitance of the shield can be made large enough to effectively isolate the object being measured from its surroundings.

In summary, stray capacitance is a common challenge in capacitance measurement, and can significantly affect the accuracy and precision of the measurement. To minimize the effect of stray capacitance, designers and engineers must use isolation and shielding techniques, as well as calibration and guardring techniques, to reduce the coupling between the object being measured and its surroundings. By taking these steps, researchers and engineers can improve the reliability and validity of their measurements and make more informed decisions based on the data.

Parasitic Capacitance: Another Source of Error
---------------
Parasitic capacitance is another common source of error in electronic circuits, and is similar to stray capacitance in that it arises due to the presence of other conductive objects in the circuit. However, parasitic capacitance is typically caused by unintentional capacitance that arises due to the layout and design of the circuit, rather than external factors.

Parasitic capacitance can cause a range of errors in electronic circuits, including signal distortion, reduced bandwidth, and reduced signal-to-noise ratio. To minimize the effect of parasitic capacitance, designers and engineers must carefully consider the layout and design of the circuit, and use specialized components and techniques to reduce its impact.

One technique that can be used to reduce the effect of parasitic capacitance is to use components with low capacitance values, such as surface-mount capacitors or multilayer ceramic capacitors. These components have a smaller physical size and lower parasitic capacitance than traditional through-hole components, making them ideal for high-frequency applications where parasitic capacitance can be a significant source of error.

Another technique that can be used to reduce the effect of parasitic capacitance is to use guard traces, which are conductive traces that are placed around high-frequency components to reduce the effect of parasitic capacitance. These guard traces are connected to a low-impedance ground, which helps to prevent the buildup of parasitic capacitance in the circuit.

In addition to these techniques, designers and engineers may also use specialized simulation tools, such as SPICE (Simulation Program with Integrated Circuit Emphasis), to model the effect of parasitic capacitance on the circuit and optimize the circuit design to minimize its impact. By taking these steps, researchers and engineers can improve the accuracy and precision of electronic circuits, and reduce the likelihood of errors and erroneous conclusions based on flawed data.

Measurement Instrument Limitations
----------------
Researchers and engineers must also consider the limitations of the measurement instrument when designing experiments and interpreting results. For example, if the measurement range of the instrument is not sufficient to cover the full range of capacitance values that are expected to be measured, this can lead to measurement errors and reduce the accuracy of the results.

To address these limitations, researchers and engineers may use specialized techniques, such as signal averaging or oversampling, to improve the signal-to-noise ratio of the measurement signal and increase the accuracy of the measurement. Signal averaging involves taking multiple measurements of the same signal and averaging them together to reduce the effect of noise and improve the accuracy of the measurement. Oversampling involves taking multiple measurements of the same signal at a higher sampling rate than necessary and then averaging them together to reduce the effect of noise and increase the accuracy of the measurement.

Another technique that can be used to address measurement instrument limitations is to perform a calibration of the measurement instrument before use. Calibration involves comparing the measurements made by the instrument to the known values of a reference standard, and then adjusting the calibration of the instrument to improve the accuracy of the measurement. Calibration should be performed regularly to ensure that the measurement instrument is operating within its specified range and that the measurements are accurate and precise.

In summary, measurement instrument limitations can affect the accuracy and precision of capacitance measurements. To address these limitations, researchers and engineers must use high-precision capacitance meters that are well-calibrated and properly maintained, and use specialized techniques such as signal averaging and oversampling to improve the accuracy of the measurement. By taking these steps, researchers and engineers can improve the reliability and validity of their experimental results and make more informed decisions based on the data.

The Bridge Method
----------------
The bridge method is a widely used technique for capacitance measurement. In this method, a bridge circuit is used to measure the capacitance by comparing it to a known reference capacitor. The bridge circuit consists of four arms, one of which contains the unknown capacitance, and the other three arms contain resistors and a reference capacitor. The bridge circuit is balanced by adjusting the resistors until the bridge output voltage is zero. The capacitance is then calculated based on the resistances and the known reference capacitance.

The Charge-Discharge Method
---------------
The charge-discharge method involves charging a capacitor with a known voltage and measuring the time it takes for the capacitor to discharge through a known resistor. The capacitance is then calculated using the following equation:

.. math:: C = \frac{T}{R \ln(1-\frac{V}{V_0})}

where T is the time constant of the circuit, R is the resistance, V is the voltage across the capacitor, and V0 is the initial voltage across the capacitor.

The Phase-Sensitive Detection Method
---------------
The phase-sensitive detection method involves applying an AC voltage to the unknown capacitor and measuring the phase shift between the applied voltage and the resulting current. The capacitance is then calculated using the following equation:

.. math:: C = \frac{1}{2\pi f R \sin(\phi)}

where f is the frequency of the applied voltage, R is the resistance, and φ is the phase shift.

Experiment 1: Measuring Capacitance using Red Pitaya and Charge-Discharge Method
-------------
In this experiment, we will use the charge-discharge method to measure the capacitance of a capacitor using the Red Pitaya board.
Wire a 1kΩ resistor in series with the capacitor to be measured and connect it to Red pitaya 3.3V. Add a switch parallel to the capacitor so we can charge and discharge it and connect oscilloscope probes to the capacitor so we can observe the voltage behavior. To help with the wiring you can use the picture below:


Now let's close the switch to charge the capacitor and monitor the voltage across the capacitor. When the capacitor is fully charged, connect the probes to the resistor, and open the switch so the capacitor discharges through the resistor. Monitor the voltage across the resistor using Red Pitayas oscilloscope, read the time discharge time tau, and we can calculate the capacitor value using the following equation:

.. math:: C= \frac{\tau}{R}

Experiment 2: Uncertainty in Capacitance Measuring using Red Pitaya
--------------------
In any measurement, it is important to consider the uncertainty associated with the measurement. In this experiment, we will investigate the uncertainty in capacitance measurement using the Red Pitaya board. We will use the same circuit as before, repeating the measurements multiple times and recording measured values.

Using the previous experiment procedure, we measured the capacitance of a 10 µF capacitor five times and obtained the following values: 9.8 µF, 10.1 µF, 9.9 µF, 10.2 µF, 10.0 µF. The results of measurements may vary, because of the outside noise and improperly calibrated instruments.
To calculate the standard deviation of a set of measurements, we first calculate the mean value of the measurements:

.. math:: \bar{x} = \frac{1}{n} \sum_{i=1}^{n} x_i
  
Then, we calculate the variance of the measurements:

.. math:: \sigma^2 = \frac{1}{n-1} \sum_{i=1}^{n} (x_i - \bar{x})^2
.. math::\sigma^2 = \frac{1}{5-1} [(9.8-10)^2 + (10.1-10)^2 + (9.9-10)^2 + (10.2-10)^2 + (10-10)^2] = 0.025
  
Finally, the standard deviation of the measurements is calculated as the square root of the variance:

.. math:: \sigma = \sqrt{\sigma^2}
.. math:: \sigma = \sqrt{0.025} = 0.16\text{ }\mu\text{F}
  
The mean value of the measurements is 10.0 µF, with a standard deviation of 0.16 µF. Therefore, the percentage uncertainty in the capacitance measurement is 1.6%.

Conclusion
------------
Capacitance measurement is an essential part of electronic circuit design and testing. It is essential to consider the various sources of measurement error, including stray capacitance, parasitic capacitance, and measurement instrument limitations, when performing capacitance measurements. 

Written by Andraž Pirc

This teaching material was created by `Red Pitaya <https://www.redpitaya.com/>`_ & `Zavod 404 <https://404.si/>`_ in the scope of the `Smart4All <https://smart4all.fundingbox.com/>`_ innovation project.
