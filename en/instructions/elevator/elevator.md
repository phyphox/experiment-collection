--- 
title: "Elevator"
date: 2025-01-07T14:21:17+01:00
translationKey: "Elevator Instruction"
draft: false
author: 
  - Sebastian Staacks
CreativeCommons: ['BY']
categories:
  - 'Mechanics'
sensors:
  - 'Pressure'
levels: ['2a', '2b', '3', '6']  # see doc for explanation. Remove everything else
video: ['English']
materials:
  - 'Smartphone only'
tags: # All Tags start upper-case expect for 'phyphox'. This list can be expanded!
  - 'Uniform motion'
  - 'Atmospheric pressure'
  - 'Barometric formula'
  - 'Kinematics'
summary: 'Measure the speed of an elevator and visualize its position, velocity and acceleration.'
version: '0.1.0'
---

{{< youtube y-goBtfuXAM >}}

## Overview

The pressure sensor can be used to measure height differences. This is particularly illustrative in elevators, where the height difference traveled and the speed can be determined. This allows for a discussion of both the barometric formula and kinematics. The experimental ideas presented here can also be applied to other situations involving significant height differences (e.g., climbing stairs, riding a Ferris wheel, using a pulley over multiple floors, etc.).


### Topics covered

In this experiment, the air pressure sensor is used to measure the height differences of a moving object. So the experiment can be employed in three different ways:
- The relationship between air pressure and height, i.e., the barometric formula, can be explored. In this case, it is advisable not to use the "Elevator" configuration integrated into phyphox but to record the sensor's raw data directly via "Pressure" and let learners do the conversion or compare the values with a reference (e.g., measurement with a plumb line, counting floors, GPS measurement (sometimes very inaccurate), known building height, etc.).
- Kinematics, especially s-t, v-t, and a-t diagrams, can be illustrated using an everyday process. The "Elevator" configuration integrated into phyphox is used here, which converts air pressure into a height difference and visualizes it as x-t, v-t, and a-t diagrams in conjunction with the acceleration sensor. Learners can ride the elevator and see the graphs of the elevator's movement in real-time.
- The experiment can be used as a tool for height determination in other experiments. Some drift must be expected here, but with repeated measurements, accuracies of about one meter can be achieved, which is generally more accurate than the relatively imprecise vertical GPS position and has the advantage of working indoors and in vehicles.


### Required Materials

- Smartphone or tablet with phyphox, equipped with a pressure sensor. This is the case for all Apple devices and typically for Android devices from the "mid-range" category (see [https://phyphox.org/sensordb](Sensor Database)).
- Depending on the experiment, something that leads to a height difference (elevator, escalator, larger pulley)


### Time effort

The measurement can be started at any time with just the smartphone and lasts only as long as the process to be measured. If learners are to perform the calculation of the barometric formula themselves, time must be allocated for this.


## Setup

No setup is necessary when using an elevator. For alternatives (pulley or lowering the smartphone on a rope), corresponding preparations are necessary.

In phyphox, only the "Elevator" or for raw data "Pressure" configuration needs to be opened. No further settings are necessary.


## Execution

Depending on the experiment's goal, open the "Elevator" (for automatic calculation of x-t, v-t, and a-t diagrams) or "Pressure" (to record raw sensor data) configuration integrated into phyphox. Enter the elevator and place the smartphone on the floor. Start the measurement with the triangle symbol at the top right and select a floor in the elevator. Stop the measurement at the end of the ride with the pause button (parallel lines).


## Data analysis

Depending on the requirements and task.


## Physics background and analysis details

The "Elevator" configuration uses the "international barometric formula" to convert air pressure \(p\) into height \(h\).

$$
h = \frac{288.15\,\mathrm{K}}{0.0065\,\mathrm{\frac{K}{m}}}\left(1-\left(\frac{p(h)}{1013.25\,\mathrm{hPa}}\right)^{\frac{1}{5.255}}\right)
$$

Since the absolute value is subject to meteorological fluctuations, the first measurement value is used as a reference and set to zero height, so a height difference can be determined subsequently. Additionally, this configuration averages the pressure measurements in 1-second intervals to reduce noise, even if the built-in air pressure sensor supports higher rates.

The a-t diagram corresponds to the raw data of the z-axis (perpendicular to the screen) of the acceleration sensor.

 
## Problems and Solutions

* **The a-t diagram is too noisy**
  The a-t diagram corresponds to the z-axis of the acceleration sensor, which is perpendicular to the screen. Thus, the smartphone must lie flat and should not be held upright. Additionally, vibrations can easily dominate the relatively low acceleration of an elevator. In such cases, it may help to hold the smartphone in hand or place it on a soft, slightly damping surface (foam, jacket, etc.).

* **The air pressure/height profile is unexpected.**
  Remember that air pressure as a measurement can be influenced by other factors. For example, in vehicles, height differences can be slightly overlaid by pressure differences in tunnels or the dynamic pressure over vents (cf. Pitot tube). In very fast elevators of large buildings, shafts for pressure equalization are sometimes installed, and the building's ventilation system can also have unexpected influences. In larger passenger aircraft, height measurement is impossible because the cabin pressure is artificially regulated.

* **The air pressure shows sudden fluctuations**
  If it is a waterproof smartphone, pressure equalization with the surroundings may occur slowly. Even lightly pressing on the housing (just when holding the smartphone) can cause a brief pressure change inside the device, overlaying the measurement.


## Variations

This experiment allows for many variations, such as using it while climbing stairs, with pulleys, or even with smartphones attached to a drone. Amusement park attractions like Ferris wheels or drop towers are also interesting subjects. Note that depending on the smartphone or tablet used, a resolution of about one meter height difference is possible, and a temporal drift is often noticeable. Therefore, height differences within a room are usually not measurable, and one should look for systems that involve movement over several floors/several meters.



## Worksheets / material

* Worksheet by Solmaz Khodaeifaal (Simon Fraser University): [docx](../files/elevator_khodaeifaal.docx), [pdf](../files/elevator_khodaeifaal.pdf)

We are always happy to receive and share your worksheets. Get in touch with us at contact@phyphox.org

