---
title: "EXPERIMENT NAME"
topics:
  - "Waves and Sound and Optics"
  - "Mechanics"
sensors:
  - "Gyroscope"
  - "Proximity"
# bluethooth:
#   - "phyphox-Sensorbox"
levels:
  - 1
  - 2
# competencies:
#   - "E3"
materials:
  - "Smartphone only"
tags:
  - "phyphox"
  - "Smartphone"
  - "Experiment"
  - "Gyroscope"
  - "Coil"
---

# EXPERIMENT NAME
This file is the template for all experiments. It contains all information needed for a full description of the expertiments. All experiments should use the structure of this template document. It also contains explanations of the tags and some examples for structuring the experiment.

The experiment should contain the following sections:
1. *The name of the experiment*
2. Materials
3. Setup
4. Measurement
5. Analysis
6. Supplementary material (optional)
7. Examples (optional)
8. Experiment variants (optional)
9. Troubleshooting / problems and resolutions (optional)
10. Literature and sources

The content of the section with the name of the experiment (this section) should contain a brief summary of the experiment.

The contents shold be written in markdown as defined by the [CommonMark](https://spec.commonmark.org/) standard, where a extensive documentation can be found. Some examples are also given here.

### Tagging
Tags are given in the following categories (given as an array and separated by comma):

**Topic**: Select one or more from `[Mechanics, Waves and Sound and Optics, Electricity and Magnetism, Thermal and Statistical, Astronomy, Quantum]`. The topic tags are inspired by [physport](https://www.physport.org/).

**Sensor**: Select one or more from `[Gyroscope, Accelerometer, Magnetometer, Light, Location, Pressure, Temperature, Humidity, Proximity, Voltage, Current, Speaker]`. External sensors are to listed yet, but need to be implemented (**TODO**). Since the external sensors can be the same type of sensor as the internal sensors, doubling should be avoided here.

**Bluetooth**: Select **zero or more** from `[phyphox-Sensorbox, External device]`. This category works only together with the sensor category, since the sensor is not explicitly defined here. An external device is a device which uses the BLE library for phyphox (like an ESP32). **TODO** still a discussion, especially if supported special external devices should be mentioned here.

**Level**: Select one or more from `[0, 1, 2a, 2b, 3, 6, 7]`. This refers to the ISCED-2011 Level. `0` is pre-school (Vorschule in Germany), `1` is primary school (Grundschule), `2` is lower secondary education but we distinguish in the German Orientierungsstufe (`2a`, class level 5 and 6) and Sekundarstufe I (`2b`, class level 7, 8, 9 and 10). `3` is upper secondary education (Oberstufe), `6` is Bachelor level and `7` is Master level. Inspired by the German [Bildungsministerium](https://www.datenportal.bmbf.de/portal/de/G293.html).

**Competencies**: Only for German education, this is a **TODO** (which one do we use here?, the ones from the KMK?).

**Material**: The level of additional material, select **one** from `[Smartphone only, Household items required, Basic experiment material required, Special equipment required]`.

**Tags**: This is not used at the moment, but good for search engine optimization. The tags can be chose more or less free, but should be consistent.

**It is important to write all tags correctly, else the tagging system will fail.**

## Material
A short description of the used material.

## Setup
The setup of the experiemt, best visualized with some images. The phyphox code of the experiment belongs here. The phyphox file has to be linked as `[Dowload Name](/path/to/file.phyphox)`.

First, we have an images, which goes over the whole page. All images should be clickable, so they can be shown in a new tab in fullscreen. This is achieved by the snytax `[![Alternative Text](image path to show when clicked)][image path]`

[![This is big test image](/images/testbild.png)](/images/testbild.png)

<img style="float: right;" src="/images/testbild.png" width="400">

Now there comes a lot of text to check floating images. This is some text and some more and some more and some more words. I like long words like supercalifragilistc (by the way, to you know Mary Poppins?). And we have to write a bit more to test this correctly.

the first display option is no problem, the second one locks the width of the image, which reduces responsiveness. But in general it works quite good, even on small screens. It is important to either choose a relatively small width or use the first display option. A width of *400px* seems to be a good value, but the text floating will never be perfect. One could use some css in the configuration of the static site generator for better responsiveness.

## Measurement
The measurement data.

## Analysis
Further analysis of the data. 

## Supplementary material
Additional material, for example working sheets. They can be dowloaded with `[Name](/path/to/file.pdf)`. The correct path can depend on the static site generator is still a **TODO**.

## Examples
Some example measurements with their analysis.

## Experiment variants
If the experiemts has some variants, for example different variables are measured, they go here.[^1]

## Troubleshooting / problems and resolutions
If problems can occur, the resolutions are noted here.[^2]

## Literature and sources
The source of the experiment and some additional literature if existing. This has to be the last chapter, since the foonotes in the text are offset by a small line.

[^1]: As you can see in the sections above, there are two citations. The citation style is specified below.
[^2]: Author (year), *title*, Publisher/Journal Name (doi: XXX)
