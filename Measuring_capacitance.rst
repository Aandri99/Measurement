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
Stray capacitance is an unwanted capacitance that arises due to the presence of other conductive objects near the object being measured. Stray capacitance can cause measurement errors and decrease the accuracy of capacitance measurements. To minimize the effect of stray capacitance, it is essential to keep the object being measured isolated from other conductive objects and to use a shield to reduce the coupling between the object and its surroundings.

Parasitic Capacitance: Another Source of Error
---------------
Parasitic capacitance refers to the capacitance that arises due to the inherent capacitance of conductive elements in an electronic circuit. Parasitic capacitance can affect the performance of electronic circuits and cause measurement errors. To minimize the effect of parasitic capacitance, it is essential to use low-capacitance components and minimize the length of conductive paths.

Measurement Instrument Limitations
----------------
Measurement instrument limitations can also affect the accuracy of capacitance measurements. These limitations can arise due to factors such as the accuracy of the measurement instrument, the noise in the measurement system, and the measurement range of the instrument. It is essential to use a high-precision capacitance meter that is well-calibrated and properly maintained to ensure accurate measurements.

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
Wire a 1kΩ resistor in series with the capacitor to be measured and connect it to Red pitaya 3.3V. Add a switch pararell to the capacitor so we can charge and discharge it and connect oscilloscope probes to the capacitor so we can observe the voltage behavior. To help with the wiring you can use the picture bellow:


Now let's close the switch to charge the capacitor and monitor the voltage across the capacitor. When capacitor is fully charged, connect the probes to resistor, open the switch so the capacitor discharges through the resistor. Monitor the voltage acor the resistor using Red Pitaya oscilloscope, read the time discharge time tau, and we can calculate the capacitor value using the following equation:

.. math:: C= \frac{\tau}{R}

Experiment 2: Uncertainty in Capacitance Measuring using Red Pitaya
--------------------
In any measurement, it is important to consider the uncertainty associated with the measurement. In this experiment, we will investigate the uncertainty in capacitance measurement using the Red Pitaya board. We will use the same circuit as before, repeating the measurements multiple times and record measured values.

Using the previous experiment procedure, we measured the capacitance of a 10 µF capacitor five times and obtained the following values: 9.8 µF, 10.1 µF, 9.9 µF, 10.2 µF, 10.0 µF. The results of measurements may vary, becouse of the outside noise and improperly calibrated instrument.
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

This teaching material was created by `Red Pitaya <https://www.redpitaya.com/>`_ & `Zavod 404 <https://404.si/>`_ in the scope of the `Smart4All <https://smart4all.fundingbox.com/>`_ innovation project.
