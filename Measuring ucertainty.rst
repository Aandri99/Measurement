Measuring ucertainty
============================

Objective
---------------
In this course, we will delve into the concept of measurement uncertainty and explore the various factors that affect the amount of certainty in a measurement.

.. raw:: html

Video Lecture: Introduction to Measuring Uncertainty
----------------


    <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; height: auto;">
        <iframe src="https://www.youtube.com/embed/uCvupQx2Gsg" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>


Background
---------------
Measurement uncertainty is the doubt that exists in a measured value due to limitations and imperfections in the measurement process. In this course, we will discuss several sources of measurement uncertainty, including random and systematic errors, element tolerance, measurement instrument error, measurement method error, and outside noise error.

Random Error: A Major Source of Uncertainty
-----------------
Random error, also known as statistical error, is one of the major sources of uncertainty in any measurement process. It is caused by factors that are difficult or impossible to control, such as fluctuations in temperature, pressure, or voltage, and measurement instrument noise. These unpredictable and random fluctuations affect the measurements, causing them to deviate from the true value.

Random error can be reduced by performing multiple measurements and averaging the results. The average of multiple measurements tends to be closer to the true value than a single measurement. The variability of the individual measurements is reduced when the average is calculated, leading to a more accurate result.

It's important to note that reducing random error does not eliminate uncertainty in the measurements entirely. There are other sources of uncertainty, such as systematic errors.

Systematic Error: A Systematic Deviation from the True Value
-----------------
Systematic error, unlike random error, is a constant deviation from the true value that occurs in every measurement. It is caused by factors such as a miscalibrated instrument, a biased measurement method, or environmental conditions that affect the measurement process, errors which are coming up next.

Effect of element tolerance on uncertainty
-----------------
For example, a resistor with a nominal value of 1 kΩ and a tolerance of 5% may have an actual value of anywhere between 950 Ω and 1050 Ω. If this resistor is used in a circuit to measure resistance, the actual value of the resistor will affect the measurement result, leading to an uncertainty in the measurement.

To minimize the effect of element tolerance on measurement uncertainty, it is important to use elements with tight tolerances, or to calibrate the elements to their actual values before use. This can be done by measuring the actual values of the elements using precision instruments and adjusting the circuit parameters accordingly.

Measurement instrument error
-----------------
Measurement instrument error refers to the inherent limitations and imperfections of the instrument used to perform the measurement. These errors can be minimized by using a well-calibrated and properly maintained instrument.

Outside noise error
------------------------
Outside noise error is caused by external factors that interfere with the measurement process. This type of error can be reduced by shielding the measurement setup from external interference and selecting an appropriate measurement environment.

Experiment: Resistor tolerances
------------------

Resistor tolerances refer to the range of values within which the actual resistance of a resistor can deviate from its nominal or labeled value. Resistor tolerances are expressed as a percentage of the nominal value and typically range from 1% to 20%. For example, a 1 kΩ resistor with a tolerance of 5% can have an actual resistance between 950 Ω and 1,050 Ω. Resistor tolerances are important to consider in electronic circuit design, as they can affect the accuracy and reliability of the circuit.

To investigate how wiring the resistors in parallel affects the measurement, we will wire the ten resistors in parallel and measure the effective resistance using the Red Pitaya board. The nominal value of the resistors is 1000 Ω with a tolerance of ±5%.

The measurements of each individual resistor are as follows:
Resistor 1: 995 Ω,
Resistor 2: 1001 Ω,
Resistor 3: 990 Ω,
Resistor 4: 1004 Ω,
Resistor 5: 1002 Ω,
Resistor 6: 998 Ω,
Resistor 7: 1003 Ω,
Resistor 8: 1000 Ω,
Resistor 9: 1005 Ω,
Resistor 10: 997 Ω

As we can see from the above results, our vendor really provided us with resistors in the specified tolerance range.

Experiment: Measuring Uncertainty Due to Random Error
-------------------
First, we will set up the Red Pitaya board to measure resistance. Using Ohm's law, we will measure the voltage across one resistor and the current through it to calculate the resistance.

.. math:: R = \frac{V}{I}

We will repeat the same measurement on the same resistor several times to obtain an estimate of the tolerance.
The measurements are as follows:

+-----+-----+-----+-----+------+------+-----+------+------+------+
| | meas.| 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 |
+=====+======+=====+=====+=====+======+======+=====+======+======+======+
| Res.| 995 Ω| 998 Ω| 997 Ω| 996 Ω| 1000 Ω| 1001 Ω| 999 Ω| 1002 Ω| 1003 Ω| 1001 Ω|
+-----+------+------+-----+------+------+------+------+------+------+------+

To determine the uncertainty due to random error, we will calculate the standard deviation of these measurements:

.. math:: \sigma = \sqrt{\frac{1}{n-1} \sum_{i=1}^{n}(x_i - \bar{x})^2}

.. math:: \begin{aligned} \bar{x} &= \frac{x_1 + x_2 + ... + x_{10}}{n} \ &= \frac{995 + 998 + ... + 1001}{10} \ &= 1000 \ \Omega \end{aligned}

.. math:: \begin{aligned} \sigma &= \sqrt{\frac{1}{10-1} ((995-1000)^2 + (998-1000)^2 + ... + (1001-1000)^2)} \ &= 2.34 \ \Omega \end{aligned}

Where ..:math:\sigma is the standard deviation ,..:math:n is the number of measurements ,..:math:x_i is the i-th measurement ,..:math:\bar{x} is the mean of the measurements

The average value of these measurements is 998.2 Ω with a standard deviation of 2.34 Ω.


Conclusion
-----------------------------
Measuring physical quantities comes with inherent uncertainty, which is affected by various factors. By understanding and minimizing the sources of uncertainty, we can increase the accuracy of our measurements.


Written by Andraž Pirc

This teaching material was created by `Red Pitaya <https://www.redpitaya.com/>`_ & `Zavod 404 <https://404.si/>`_ in the scope of the `Smart4All <https://smart4all.fundingbox.com/>`_ innovation project.
