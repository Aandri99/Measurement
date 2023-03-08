Measuring uncertainty
============================

Objective
---------------
In this course, we will delve into the concept of measurement uncertainty and explore the various factors that affect the amount of certainty in a measurement.

.. raw:: HTML

Video Lecture: Introduction to Measuring Uncertainty
----------------


Background
---------------
Measurement uncertainty is the doubt that exists in a measured value due to limitations and imperfections in the measurement process. In this course, we will discuss several sources of measurement uncertainty, including random and systematic errors, element tolerance, measurement instrument error, measurement method error, and outside noise error.

Random Error: A Major Source of Uncertainty
-----------------
Random error is a significant source of uncertainty in any measurement process. It is caused by factors that are difficult or impossible to control, such as fluctuations in temperature, pressure, voltage, and measurement instrument noise. These unpredictable and random fluctuations can affect the measurements and cause them to deviate from the true value.

To minimize the effects of random error, it is common practice to perform multiple measurements and calculate the average. This approach is based on the idea that the random errors in each individual measurement will be random and uncorrelated. Therefore, when multiple measurements are performed, the random errors tend to cancel out, and the average of the measurements will be closer to the true value than any single measurement. Other strategies to minimize the effects of random error include using more precise measurement instruments that are less susceptible to fluctuations.

In conclusion, random error is an important consideration when performing measurements, and it is essential to understand the sources of uncertainty and minimize their effects. By performing multiple measurements and using more precise measurement instruments when possible, we can reduce uncertainty and obtain more accurate measurement results.

Systematic Error: A Systematic Deviation from the True Value
-----------------
Systematic error, unlike random error, is a constant deviation from the true value that occurs in every measurement. Systematic error is an important concept in experimental research because it can significantly affect the accuracy and precision of measurements. For example, if a scale used to measure weight is consistently off by a certain amount, it will produce systematic error in every measurement. If this error is not accounted for, it can lead to incorrect conclusions or inaccurate data. To reduce or eliminate systematic error, researchers may need to adjust their instruments or measurement methods, or take additional steps to control environmental factors.

To illustrate the practical implications of systematic error, consider the example of measuring blood pressure using a sphygmomanometer (blood pressure cuff). If the cuff is too small or too large for the patient, or if it is not properly calibrated, it can produce systematic error in every measurement. This error can be significant enough to affect the diagnosis and treatment of the patient. To avoid systematic error in this case, healthcare providers must ensure that the cuff is the appropriate size for the patient, and that it is calibrated regularly to ensure accuracy.

In scientific research, systematic error can also be caused by biases in the experimental design or data analysis. For example, if researchers unintentionally select participants who are more likely to produce a certain result, or if they analyze the data in a way that is biased towards a particular outcome, they can introduce systematic error into their findings. To minimize these types of errors, researchers must use rigorous methods for participant selection and data analysis, and must take steps to avoid biases in their experimental design.

Effect of element tolerance on uncertainty
-----------------
For example, a resistor with a nominal value of 1 kΩ and a tolerance of 5% may have an actual value of anywhere between 950 Ω and 1050 Ω. If this resistor is used in a circuit to measure resistance, the actual value of the resistor will affect the measurement result, leading to uncertainty in the measurement.

To minimize the effect of element tolerance on measurement uncertainty, it is important to use elements with tight tolerances or to calibrate the elements to their actual values before use. This can be done by measuring the actual values of the elements using precision instruments and adjusting the circuit parameters accordingly.

Measurement instrument error
-----------------
In practical applications, element tolerance can have a significant impact on measurement uncertainty. For example, in electronic circuits, resistors and capacitors are often used to control the flow of current and voltage. However, the actual values of these elements may deviate from their nominal values due to manufacturing variations or environmental factors. This can lead to measurement errors and reduce the accuracy and precision of the circuit.

To minimize the effect of element tolerance on measurement uncertainty, it is important to select elements with tight tolerances or to calibrate the elements to their actual values before use. This can be done by measuring the actual values of the elements using precision instruments and adjusting the circuit parameters accordingly. For example, if a 1 kΩ resistor is found to have an actual value of 990 Ω, the circuit parameters can be adjusted to compensate for this deviation and improve the accuracy of the measurement.

In addition to element tolerance, other factors can also contribute to measurement uncertainty, such as noise, interference, and drift. To ensure accurate and precise measurements, it is important to identify and control these sources of uncertainty through careful experimental design, calibration, and data analysis. This requires a systematic approach to measurement and a thorough understanding of the underlying physical principles and mathematical models involved in the measurement process. By minimizing measurement uncertainty, researchers and engineers can improve the reliability and validity of their experimental results and make more informed decisions based on the data.

Outside noise error
------------------------
Examples of outside noise error include electromagnetic interference (EMI) from nearby electronic devices, vibrations from mechanical sources, and temperature fluctuations. These factors can cause fluctuations in the measurement signal and introduce measurement uncertainty. To minimize outside noise error, researchers and engineers may use shielding materials, isolate the measurement setup from external sources of interference, or use active noise cancellation techniques.

For example, in neuroscience research, electroencephalography (EEG) is often used to measure brain activity. However, the EEG signal can be affected by external sources of noise, such as electrical interference from nearby equipment. To minimize outside noise error in EEG measurements, researchers may use shielding materials and grounded cables to reduce electromagnetic interference, or place the measurement setup in a shielded room with controlled temperature and humidity.

In addition to external factors, outside noise error can also be caused by limitations in the measurement equipment or methods. For example, if the resolution of a sensor is not sufficient to detect small changes in the measurement signal, this can lead to measurement uncertainty and errors. To minimize these types of errors, researchers and engineers must carefully select and calibrate their measurement equipment, and use appropriate statistical techniques to quantify and control measurement uncertainty. By minimizing outside noise error, researchers and engineers can improve the accuracy and precision of their measurements, and reduce the likelihood of erroneous conclusions or decisions based on flawed data.

Experiment: Resistor tolerances
------------------

Resistor tolerances refer to the range of values within which the actual resistance of a resistor can deviate from its nominal or labeled value. Resistor tolerances are expressed as a percentage of the nominal value and typically range from 1% to 20%. For example, a 1 kΩ resistor with a tolerance of 5% can have an actual resistance between 950 Ω and 1,050 Ω. Resistor tolerances are important to consider in electronic circuit design, as they can affect the accuracy and reliability of the circuit.

First, we will need to set up the Red Pitaya board to measure resistance. We will use the onboard ADC to measure the voltage across the resistor and the current through it. By applying Ohm's law, we can calculate the resistance:

.. math:: R = \frac{V}{I}

Note that the nominal value of the measured resistors is 1000 Ω with a tolerance of ±5%. The measurements of each resistor are as follows:
982 Ω, 1032 Ω, 1020 Ω, 1030 Ω, 1002 Ω, 978 Ω, 1033 Ω, 1020 Ω, 1966 Ω, 997 Ω

As we can see from the above results, our vendor provided us with resistors in the specified tolerance range, as non of the measured resistors are above 1050 or below 950 ohms.

Experiment: Measuring Uncertainty Due to Random Error
-------------------
To demonstrate how uncertainty can be measured experimentally, we will use the same setup on Red pitaya as before, with the difference that we will only be measuring one resistor multiple times.

The measurements are as follows:

995 Ω, 998 Ω, 997 Ω, 996 Ω, 1000 Ω, 1001 Ω, 999 Ω, 1002 Ω, 1003 Ω, 1001 Ω

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
