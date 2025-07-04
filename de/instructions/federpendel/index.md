---
# Instructions are generic instructions for phyphox experiments.
# These should primarily address which materials are required, how to conduct the experiment, which results can be expected, which problems to expect and how to troubleshoot them.
# Additionally, variants can be discussed, in particular how the experiment can be used to cover different subjects and student levels.
# These instructions are not worksheets by themselves and while they can be used by students, they do not directly address students.
# Worksheets should be linked at the end of the instructions (compare with existing experiments).

title: "Federpendel"                       # Title of the experiment
translationKey: "Federpendel"  # This has to be the same across all translations of the same instructions and allows linking to different language versions despite them having different titles

author:                                 # One or more authors of this document (i.e. your name and anyone who contributed)
  - Alexander Pusch
  - Sebastian Staacks

CreativeCommons: ['BY']                 # License of this document and embedded materials (images). This should be a Creative Commons licence. Make this an array of the different CC modules that apply.
# Examples:
# CC-0        => ['0']
# CC-BY-SA    => ['BY', 'SA']
CC-BY-NC-SA # => ['BY', 'NC', 'SA']
# CC-BY-ND    => ['BY', 'ND']
# See https://creativecommons.org/share-your-work/ for details

categories:                             # Pick one or more of the following and remove the others. Do not translate them. Get in touch with the phyphox team before adding new categories or if an item is not automatically translated in the final document
  - 'Mechanics'

sensors:                                # Pick one or more of the following and remove the others. Do not translate them. Get in touch with the phyphox team before adding new sensor types or if an item is not automatically translated in the final document
  - 'Accelerometer'

# Bluetooth
# Frontmatter for Bluetooth devices has not yet been finalized. If the experiment uses Bluetooth, please get in touch with the phyphox team first.

levels: ['2a', '2b', '3', '6', '7']   # Education levels according to ISCED-2011
# This should indicate, for which levels there is an interesting variant of the experiment.
# 0 Early childhood education
# 1 Primary education
# 2 Lower secondary education (2a = with access to higher levels, 2b = without access to higher levels)
# 3 Upper secondary education
# 6 Bachelor's or equivalent
# 7 Master's or equivalent
# See https://en.wikipedia.org/wiki/International_Standard_Classification_of_Education or https://uis.unesco.org/en/topic/international-standard-classification-education-isced for details.
# Notes:
#- We distinguish between 2a and 2b for lower secondary education forms that either focus to prepare students to continue with upper secondary education (2a) or that emphasize a path to vocational training (2b)
#- Levels 4, 5 and 8 are currently not represented as they are rather specific. Let us know if you have a use case for this.

materials:  # Pick which material is required for this experiment and remove the others. Do not translate them.
  - 'Household items'
#  - 'Basic experiment material'
#  - 'Special equipment'
# Only select multiple if there are matching variants. For example: If an experiment requires a stand (basic experiment material) and a plastic bag (household items), only select "basic experiment material". However, if there is a variant that requires a stand and an independent variant that only requires a plastic bag, select both categories.

tags: # These are free tags that help finding the experiment and that can be used in cloud tags. In contrast to the other items you can freely define them and they should be in the language of the document!
  - 'Uniform motion' # Example 1
  - 'Atmospheric pressure'  # Example 2
  - 'Barometric formula'  # Example 3

summary: 'This is a short summary of the experiment, which is shown in listings with multiple experiments.'
---

## Overview

Ein Federpendel lässt sich einsetzen, um (harmonische) Oszillationen zu zeigen, die Periodendauer zu bestimmen oder auch um gedämpfte Schwingungen zu untersuchen. Der Aufbau erfolgt mit gängigem Stativmaterial und einer Schraubfeder. 

Aufbau:
- Das Smartphone wird an einer Schraubfeder an einer Stativstange aufgehangen.
- Es eignen sich Druckverschlussbeutel, Versandtaschen, Topflappen oder eine Papprolle um das Smartphone aufzunehmen.
- Alternativ: Anstelle der Schraubenfeder lässt sich auch ein dickeres Gummiband untersuchen. Dieses resultiert dann allerdings nicht in einer idealen harmonischen Oszillation. 

Durchführung
- Starten Sie das Experiment "Beschleunigung ohne g" und lenken das Pendel aus.
- In der ersten Ansicht in der App werden die Werte für die Beschleunigung der einzelnen Koordinatenachsen angezeigt.
- Auf den Graphen ist eine Oszillation erkennbar, die sich je nach Ausrichtung des Smartphones und Bewegungsrichtung in einer oder zwei Achsen besonders deutlich zeigt.
- Ein Schlingern des Smartphones beim Pendeln kann zu vom idealen Modell abweichenden Ergebnissen führen. 

Hinweise:
- Durch die Verwendung von unterschiedlich großen Pappscheiben, die waagerecht am unteren Ende der Feder befestigt werden, lassen sich verschieden starke Dämpfungen realisieren.
