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
Random error is an unavoidable component of any measurement process. It is caused by unpredictable and fluctuating factors that affect the measurement. Random error can be reduced by performing multiple measurements and averaging the results.

Systematic Error: A Systematic Deviation from the True Value
-----------------
Systematic error, unlike random error, is a constant deviation from the true value that occurs in every measurement. It is caused by factors such as a miscalibrated instrument, a biased measurement method, or environmental conditions that affect the measurement process.

Effect of element tolerance on uncertainty
-----------------
The tolerance of an element, such as a resistor or capacitor, can also contribute to measurement uncertainty. This occurs because the actual value of the element may deviate from its nominal value, leading to a measurement error.

Measurement instrument error
-----------------
Measurement instrument error refers to the inherent limitations and imperfections of the instrument used to perform the measurement. These errors can be minimized by using a well-calibrated and properly maintained instrument.

Outside noise error
------------------------
Outside noise error is caused by external factors that interfere with the measurement process. This type of error can be reduced by shielding the measurement setup from external interference and selecting an appropriate measurement environment.


Experiment: Measuring Tolerance
-------------------
In this experiment, we will measure the tolerance of a resistor using a Red Pitaya board. We will apply a known voltage across the resistor and measure the resulting current, then calculate the resistance using Ohm's Law:

.. math:: R = \frac{V}{I}

We will repeat the measurement several times to obtain an estimate of the tolerance.
The measurements are as follows:

995 Ω 1001 Ω990 Ω 1004 Ω 1002 Ω 998 Ω 1003 Ω 1000 Ω 1005 Ω 997 Ω

To determine the uncertainty due to random error, we will calculate the standard deviation of these measurements:

.. math:: \sigma = \sqrt{\frac{1}{n-1} \sum_{i=1}^{n}(x_i - \bar{x})^2}

.. math:: \begin{aligned} \bar{x} &= \frac{x_1 + x_2 + ... + x_{10}}{n} \ &= \frac{995 + 1001 + ... + 997}{10} \ &= 1000 \ \Omega \end{aligned}

.. math:: \begin{aligned} \sigma &= \sqrt{\frac{1}{10-1} ((995-1000)^2 + (1001-1000)^2 + ... + (997-1000)^2)} \ &= 5.13 \ \Omega \end{aligned}

Where:

:math:\sigma is the standard deviation

:math:n is the number of measurements

:math:x_i is the i-th measurement

:math:\bar{x} is the mean of the measurements

The standard deviation of 5.13 Ω indicates the range of values that the true resistance may fall within with a given level of confidence.


Conclusion
-----------------------------
Measuring physical quantities comes with inherent uncertainty, which is affected by various factors. By understanding and minimizing the sources of uncertainty, we can increase the accuracy of our measurements.


Written by Andraž Pirc

This teaching material was created by `Red Pitaya <https://www.redpitaya.com/>`_ & `Zavod 404 <https://404.si/>`_ in the scope of the `Smart4All <https://smart4all.fundingbox.com/>`_ innovation project.
