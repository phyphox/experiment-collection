--- 
title: "(In)elastic Collision"
date: 2024-12-17T11:42:40+01:00
translationKey: "Inelastic Collision Instruction"
draft: false
author: 
  - Sebastian Staacks
CreativeCommons: ['BY']
categories:
  - 'Mechanics'
sensors:
  - 'Microphone'
levels: ['2a', '2b', '3', '6']  # see doc for explanation. Remove everything else
video: ['English']
materials:
  - 'Household items'
tags: # All Tags start upper-case expect for 'phyphox'. This list can be expanded!
  - 'Ball'
  - 'Inelastic Collision'
  - 'Elastic Collision'
  - 'Conservation of Energy'
  - 'Free Fall'
  - 'Acoustic Stopwatch'
summary: 'Determine the initial height and loss of energy of a bouncing ball from the timing of its impact sounds'
version: '0.1.0'
---

{{< youtube ikvtPDwV1FE >}}

## Overview

In this experiment, you drop a ball near the microphone of your phone onto a hard surface (i.e. a table). Phyphox will detect the sounds of each impact of the ball on the surface and use their timing to determine the drop height of the ball. It will show the maxima of its free fall parabola between each impact as well as the kinetic energy retained after each impact (relative to the initial energy).

### Topics covered

This experiment can be used to discuss conservation of energy and in particular potential and kinetic energy. It can also be used as a tool to discuss and explore elastic/plastic/inelastic collisions. Finally, since a parabolic trajectory is assumed, it can also be used in context of a simple parabolic free fall by looking at the maximum estimate between each impact. However, understanding the entire data presented by phyphox requires some understanding of energy.

### Required Materials

* Smartphone or tablet with phyphox
* Ball (small metal ball, golf ball, …)
* Hard surface (table)
* Tape measure or similar if you want to verify phyphox results

### Time effort

The experiment can be set up within a minute. However, depending on the noise level of the surroundings, it can take a few tries to fine tune the threshold (sensitivity) of the trigger (see problems and solutions below).

## Setup

Place your phone on the surface or a stand close to the surface. As you want to detect the sound from the ball's impact on the surface, it is highly recommended to be as close to the impact point as possible, so the sound stands out from background noises in the room.

In phyphox select the configuration "(In)elastic collision" from the main menu. Press the triangle in the top-right corner to start the measurement.

Depending on the noise in your room, your choice of ball and surface and your phone model, you might have to adjust the "threshold" setting in the "Settings" tab. This determines at which volume (on a scale from zero to one) noise is considered as an event in the experiment. If measurements are coming in on the "Heights" or "Energy" tab immediately without a bouncing ball, you want to increase the threshold from its default value of 0.1. If you do not get any measurements when the ball is bouncing, you might want to decrease it.

Minimum delay determines how long phyphox will wait after an event before considering sound above the threshold as a new event. This can be increased if a single impact is counted multiple times due to reverbaration, but the first measure should be to increase the threshold. For most experiments, the default of 0.1s should be fine.

## Execution

Make sure phyphox is running (top-right corner shows a pause symbol instead of the triangular start button). Reset your measurements by pressing the "reset" button the "heights" or "energy" tab. Drop the ball next to the phones microphone. Optionally you can hold a tape measure next to the dropping ball for reference.

The Heights tab will show up to five time intervals that correspond to six impacts on your surface.

## Data analysis

The times shown in the "heights" tab correspond to the time difference between two impacts on the table. The heights 1 to 5 correspond to the maximum height that the ball reached during the corresponding time interval. Height 0 is the initial height **before** the first impact, extrapolated from impacts 1 to 3 (see Physics background and analysis details).

The energy tab shows energy data corresponding to the heights that have actually been derived from time intervals. As there is no means to determine the absolute energy the energy of height 1 is set to 100%, meaning that all energy is expressed as a fraction of the potential energy of height 1 from the "heights" tab. Consequentially, Energy 2 to 5 correspond to the potential energy of height 2 to 5 and therefore the ratio of height 2 to 5 and height 1. The smaller entries "Retained on collision" is just the ratio of the potential enery of the current time interval divided by the potential enery of the previous interval, thereby representing the fraction of energy that was retained as kinetic energy after the last bounce.

## Physics background and analysis details

Phyphox records audio samples from the phone's microphone and considers them sequentially (like the "acoustic stopwatch" configuration). The samples are normalized to a range of -1 to 1, although the exact meaning can differ from phone to phone due to different recording hardware and processing. If a sample is above the trigger threshold set by the user, this is counted as an event and its time is noted. The time is based on the sampling rate of the recording, which is typically 48kHz (or in some cases 44.1kHz), resulting in a theoretical temporal resolution of \(21\,\mathrm{\mu s}\) (or \(23\,\mathrm{\mu s}\)). Note that in practice this resolution is severely limited by differences between the sounds from different bounces as well as dispersion and the shape of the waveform itself and phyphox only displays three decimals (1ms) while using the exact value internally.

The next sound samples will be discarded until a minimum time interval set by "Minimum Delay" has passed. After this time the next sample above the threshold is noted as the next event and the time difference between subsequent events is shown as "Time 1", "Time 2", etc.

Phyphox assumes a perfect parabolic trajectory between each event. Therefore, "Height 1" to "Height 5" are simply calculated as

$$
h_i = \frac{1}{8} g \Delta t_i^2
$$

with \(\Delta t_i\) being the corresponding "Time i" and \(g\) Earth's acceleration, assumed to be \(9.81\,m/s^2\). This is based on the distance travelled by a body under constant acceleration \(a\) from rest:

$$
d = \frac{1}{2}a t^2
$$

In this experiment \(a = g\) and \(\Delta t_i = 2 t\) as the time interval encompasses the rise of the ball to the highest point and then symmetrically the drop from zero vertical velocity.

Energies are simply considered from potential energy at the highest point at the trajectory. With constant mass and Earth's acceleration, the potential energy \(E_i = mgh_i\) at each maximum can simply be expressed as a fraction of energy \(E_1\) as the ratio of the heights \(E_i/E_1 = h_i/h_1\).

Finally, the initial height \(h_0\) is extrapolated by assuming that the ratio of potential energy before and after the first impact is the same as before and after the second impact:
\begin{align*}
 \frac{E_0}{E_1} &= \frac{h_0}{h_1} = \frac{h_1}{h_2} = \frac{t_1^2}{t_2^2}\\\\
\Rightarrow h_0 &= h_1\frac{t_1^2}{t_2^2} = \frac{1}{8}g\frac{t_1^4}{t_2^2}
\end{align*}

Note, that in practice, this usually underestimates the initial height because the amount of energy transformed into heat on impact typical increases with higher impact velocities. Therefore, the first impact with the highest impact velocity usually has a higher "energy loss" than the second, so by assuming it to be the same on both impacts means that the energy before the first impact is typically underestimated.
 
## Problems and Solutions

* **Phyphox misses some or all impacts.**
  If the measurement reacts to some impacts or loud noises like clapping, but misses some impacts, the trigger threshold is set too high. Decrease the threshold to match the volume of your impact sounds or increase the volume of these sounds by picking a different ball/surface combination. You can check also have a look at the volume of the sounds in the phyphox configuration "Audio Scope", which dislays noise in the same zero to one range as the trigger setting.
* **Events are registered even if the ball is not bouncing**
  In this case the threshold is set too low and/or the background noise is too loud. Increase the threshold until the measurement is not triggered by background noises. Make sure that the bouncing sound is louder than the background noise in the room.
* **Some bounces are counted as multiple events**
  This can be a consequence of a too low trigger threshold as the reverberation of the sound is still above the threshold. Try increasing the threshold first. If this is not an option because you are missing the quieter later boucnes or because your surroundings are too loud, you can try to increase the setting "Minimum delay", which prevents fast events. Be aware though, that this might also lead to missed events when the later bounces occur more rapidly.
* **The energy readings do not make any sense / Some energy readings are larger than 100%**
  Check the time intervals shown on the heights tab. These probably are not correct and you might have a very short interval in there from a bounce that was counted twice. Check the solutions for missed collisions or collisions that have been counted multiple times.

## Variations

In principle, this experiment should work on various scales, from marbles to basket balls and from centimeters to several meters. Just keep in mind that air resistance might play a role and that vastly different sound volumes or timing intervals can be a challenge.

Also, this experiment can be used in many different ways. It can be used as a show-case for these calculations before and/or after discussing the underlying calculations with students. It can also be used to discuss collisions with varying elasticities. For this, different combinations of balls and surfaces can be used to determine the coefficient of restitution for each combination.

For a more systematic variation of the coefficient of restitution, a well-bouncing ball (golf ball or steel ball) can be used on a hard surface. Then the coefficient of restitution can be gradually lowered by inserting an increasing number of sheets of paper between the ball and the surface.

## Weitere Videos

{{< youtube Zm_tAkWmZPo >}}
{{< youtube MOHCmhbkjek >}}

## Worksheets / material

No worksheets are available yet. You can check this page in other languages to see if there is material available for translation.

We are always happy to receive and share your worksheets. Get in touch with us at contact@phyphox.org

