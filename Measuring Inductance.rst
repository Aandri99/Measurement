OpAmps 101
============================

Objective
---------------
In this section, we will discuss the measurement of inductance, which is a fundamental property of electrical circuits. Inductance is a measure of an object's ability to store electrical energy in a magnetic field, and it is expressed in henries (H).

Background
---------------
Inductance measurement is essential in many areas of electrical engineering, including power transmission, signal processing, and electronic circuit design. Inductance measurement can be challenging due to various factors, including stray inductance, parasitic inductance, and measurement instrument limitations.

Stray Inductance: A Frequently Encountered Obstacle in Inductance Measurement
-----------------
Stray inductance is an unwanted inductance that arises due to the presence of other conductive objects near the object being measured. Stray inductance can cause measurement errors and decrease the accuracy of inductance measurements. To minimize the effect of stray inductance, it is essential to keep the object being measured isolated from other conductive objects and to use a shield to reduce the coupling between the object and its surroundings.

Parasitic Inductance: An Additional Cause of Inaccuracy
-----------------
Parasitic inductance refers to the inductance that arises due to the inherent inductance of conductive elements in an electronic circuit. Parasitic inductance can affect the performance of electronic circuits and cause measurement errors. To minimize the effect of parasitic inductance, it is essential to use low-inductance components and minimize the length of conductive paths.


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
Wire the unknown inductor in series with a known capacitor to form a resonant circuit.The resonant frequency of a series resonant circuit is given by the equation:ć

.. math:: f_res = 1/(2pisqrt(L*C))

To measure the inductance of an unknown inductor using the resonant method, we need to first determine the resonant frequency of the circuit. This can be done by sweeping the frequency of the AC voltage applied to the circuit using the Red Pitaya board and measuring the resulting current through the circuit. When the frequency of the applied voltage is equal to the resonant frequency, the current through the circuit will be at its maximum.

Once we have determined the resonant frequency, we can calculate the inductance of the unknown inductor using the resonant frequency and the known capacitance of the reference capacitor. For example, if the resonant frequency is found to be 10 kHz and the reference capacitor has a value of 1 microfarad, then the inductance can be calculated as follows:

.. math:: L = 1/(4pi^2f_res^2*C)
.. math:: L = 1/(4pi^2(10,000 Hz)^2*(1x10^-6 F))
.. math:: L = 39.8 microhenries

Therefore, the inductance of the unknown inductor is approximately 39.8 microhenries.

Written by Andraž Pirc

This teaching material was created by `Red Pitaya <https://www.redpitaya.com/>`_ & `Zavod 404 <https://404.si/>`_ in the scope of the `Smart4All <https://smart4all.fundingbox.com/>`_ innovation project.
