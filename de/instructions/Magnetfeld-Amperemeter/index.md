---
# Instructions are generic instructions for phyphox experiments.
# These should primarily address which materials are required, how to conduct the experiment, which results can be expected, which problems to expect and how to troubleshoot them.
# Additionally, variants can be discussed, in particular how the experiment can be used to cover different subjects and student levels.
# These instructions are not worksheets by themselves and while they can be used by students, they do not directly address students.
# Worksheets should be linked at the end of the instructions (compare with existing experiments).

title: "Magnetfeld Amperemeter"                       # Title of the experiment
translationKey: "Magnetfeld Amperemeter"  # This has to be the same across all translations of the same instructions and allows linking to different language versions despite them having different titles

author:                                 # One or more authors of this document (i.e. your name and anyone who contributed)
  - Alexander Pusch

CreativeCommons: ['BY']                 # License of this document and embedded materials (images). This should be a Creative Commons licence. Make this an array of the different CC modules that apply.
# Examples:
# CC-0        => ['0']
# CC-BY-SA    => ['BY', 'SA']
CC-BY-NC-SA => ['BY', 'NC', 'SA']
# CC-BY-ND    => ['BY', 'ND']
# See https://creativecommons.org/share-your-work/ for details

categories:                             # Pick one or more of the following and remove the others. Do not translate them. Get in touch with the phyphox team before adding new categories or if an item is not automatically translated in the final document
  - 'Electricity and Magnetism'


sensors:                                # Pick one or more of the following and remove the others. Do not translate them. Get in touch with the phyphox team before adding new sensor types or if an item is not automatically translated in the final document
  - 'Magnetometer'

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
  - 'Basic experiment material'
  - 'optional 3D-Prints'
# Only select multiple if there are matching variants. For example: If an experiment requires a stand (basic experiment material) and a plastic bag (household items), only select "basic experiment material". However, if there is a variant that requires a stand and an independent variant that only requires a plastic bag, select both categories.

tags: # These are free tags that help finding the experiment and that can be used in cloud tags. In contrast to the other items you can freely define them and they should be in the language of the document!
  - 'Amperemeter' # Example 1
  - 'Spule'  # Example 2
  - 'Stromstärke'  # Example 3
  - 'Permeabilitätszahl'  # Example 3


summary: 'This is a short summary of the experiment, which is shown in listings with multiple experiments.'
In diesem Experiment wird der Magnetfeldsensor verwendet um indirekt über die magnetische Wirkung die Stromstärke zu ermitteln. Darüber hinaus können anhand einer Referenzmessung (z.B. mit bekannter Permeabilitätszahl von Luft) die Permeabilitätszahlen unterschiedlicher Spulenkern eermittelt und verglichen werden .
Um die Praktikabilität und Reproduzierbarkeit im Experiment zu erhöhen, kann eine einfache Halterung aus dem 3D-Drucker verwendet werden, um die Spule am Smartphone zu fixieren. Alternativ funktioniert auch Klebeband.

## Overview

Theoretischer Hintergrund:
In einer schmalen Spule der Länge l mit N Windungen ist der Zusammenhang zwischen dem Betrag der magnetischen Feldstärke B entlang der Spulenrichtung und angelegter Stromstärke I in guter Näherung gegeben durch:

B = µ_0 * µ_r * I * N / l 

Es kann daher Näherungsweise ein proportionaler Zusammenhang zwischen B und I angenommen werden.


Bestimmung der Stromstärke:
1. Eine kleine Spule wird gewickelt (z.B. 30 Windungen, um eine Stativstange) und über dem Magnetometer platziert (austesten mit einem kleinen Probemagneten). (vgl. Abb.1)
2. Das Experiment wird zu phyphox hinzugefügt: phyphox://phyphox.org/wiki/images/6/65/Amperemeter-Clip_Phyphox_App.phyphox und gestartet
3. Eine Kalibrierung wird im Phyphox experiment durchgeführt. Hierzu sind zwei Wertepaare erforderlich. Ein Wertepaar kann 0A und die gemessene Magnetische Feldstärke sein. Das zweite Wertepaar wird anhand einer bekannten angelegten Stromstärke aufgenommen. (vgl. Abb. 2 und 3)
4. Wenn das Experiment auf die gewickelte Spule kalibriert wurde, können verschiedene Stromstärken mit Phyphox bestimmt werden. 

Abbildung 1: gewickelte Spule auf Smartphone mit optionalem 3D-Druckteil.

Hinweise zur Spule:
- Die Spule muss möglichst exakt und nah am Sensor positioniert werden.
- Der Innenwiderstand der Spule muss durch ausreichende Dimensionierung des Drahts vernachlässigbar klein sein.
- Die Position der Spule zum Smartphone und die des Smartphones zum Erdmagnetfeld dürfen beim Experimentieren nicht verändert werden.
- Mit einer Spule von ca. 30 Windungen können ohne Eisenkern Stromstärken bis etwa 20 mA zuverlässig gemessen werden.
- Die gemessenen Magnetfelder befinden sich je nach Stromstärke bei bis zu 3-facher Größe des Erdmagnetfeldes.
- Bei Nutzung eines Eisenkerns können die Größe des erzeugen Magnetfeldes und somit die Messgenauigkeit um ein Vielfaches erhöht werden.


Abbildung 2: Kalibrierung mittels zweier Wertepaare.
Abbildung 3: Nutzung des Experiments zur Anzeige der Stromstärke.


Weiterführende Informationen zu dem Experiment, eine optionale 3D-Datei und Ideen für weitere Möglichkeiten (z.B. Permeabilitätszahl bestimmen) finden sich hier: 
- Download STL-Datei: https://physikkommunizieren.de/3d-druck/spulenclip/
- Amperemeter-Experiment im Phyphox-Wiki: http://www.phyphox.org/wiki/index.php?title=Smartphones_as_ammeters
- Holz, C., & Pusch, A. (2022). Stromstärken mir einem Spulenclip messen. In Wilhelm, T., & Kuhn, J. (Hrsg.), Für alles eine App (S. 237–242). Springer VDI Verlag. doi: 10.1007/978-3-662-63901-6.
- Holz, C., Pusch, A., Wilhelm, T., & Kuhn, J. (2020). Smarte Physik. Stromstärken mit dem Handy messen. Physik in unserer Zeit, 2020 (02), 96–97. doi: 10.1002/piuz.202070212.
- Holz, C., & Pusch, A. (2019). Stromstärke und Permeabilitätszahl mit dem Smartphone messen. Ein Spulenclip aus dem 3D-Drucker für Phyphox-Experimente. Naturwissenschaften im Unterricht Physik, 169, 46–47.
