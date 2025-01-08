---
translationKey: "Elevator Instruction"
title: "Aufzug"
date: 2025-01-07T14:21:17+01:00
draft: false
author: 
  - Sebastian Staacks
CreativeCommons: ['BY']
categories:
  - 'Mechanics'
sensors:
  - 'Pressure'
levels: ['2a', '2b', '3', '6']  # see doc for explanation. Remove everything else
video: ['Localized']
materials:
  - 'Smartphone only'
tags: # All Tags start upper-case expect for 'phyphox'. This list can be expanded!
  - 'Gleichförmige Bewegung'
  - 'Barometrische Höhenformel'
  - 'Luftdruck'
  - 'Kinematik'
summary: 'Bestimme die Geschwindigkeit eines Aufzugs und stelle seine Orts-, Geschwindigkeits- und Beschleunigungsfunktion dar.'
version: '0.1.0'

---

{{< youtube Jgzym7tplVU >}}

## Überblick

Der Luftdrucksensor kann genutzt werden um Höhendifferenzen zu erfassen. Dies kann insbesondere in Aufzügen sehr anschaulich genutzt werden, deren zurückgelegte Höhendifferenz sowie Geschwindigkeit ermittelt werden kann. So ist sowohl eine Diskussion der barometrischen Höhenformel als auch der Kinematik möglich. Die hier dargestellten Experimentideen lassen sich auch auf andere Situationen übertragen, in denen ein signifikanter Höhenunterschied erreicht wird (z.B. Treppensteigen, Fahrt auf einem Riesenrad, Seilzug über mehrere Etagen usw.)

### Abgedeckte Themen

In diesem Experiment wird der Luftdrucksensor genutzt um Höhenunterschiede eines sich bewegenden Objekts zu ermitteln, so dass es auf drei Arten eingesetzt werden kann:
- Es kann der Zusammenhang zwischen Luftdruck und Höhe, also die barometrische Höhenformel behandelt werden. In dem Fall bietet es sich an, nicht die in phyphox integrierte Konfiguration „Aufzug“ zu verwenden, sondern direkt über „Luftdruck“ die Rohdaten des Sensors aufzuzeichnen und den Lernenden die Umrechnung zu überlassen, bzw. die Werte mit einer Referenz (z.B. Messung mit Lot, Abzählen von Stockwerken, GPS-Messung (teuils sehr ungenau), bekannte Gebäudehöhe, usw.) zu vergleichen.
- Es kann die Kinematik, insbesondere s-t-, v-t- und a-t-Diagramme anhand eines alltäglichen Vorgangs veranschaulicht werden. Hierzu wird die in phyphox integrierte Konfiguration „Aufzug" genutzt, die die Umrechnung des Luftdrucks in eine Höhendifferenz übernimmt und in Verbindung mit dem Beschleunigungssensor als s-t-, v-t- und a-t-Diagramme visualisiert. Die Lernenden können mit dem Aufzug fahren und in Echtzeit sehen, wie die Graphen zur Bewegung des Fahrstuhls entstehen.
- Das Experiment kann als Werkzeug zur Höhenbestimmung in anderen Experimenten genutzt werden. Hier muss mit einer gewissen Drift gerechnet werden, aber insbesondere mit wiederholter Messung sind Genauigkeiten von etwa einem Meter erreichbar, was in der Regel genauer ist als die in der Vertikalen recht ungenaue GPS-Position und den Vorteil bietet, auch in Gebäuden und Fahrzeugen zu funktionieren.

### Benötigte Materialien

- Smartphone oder Tablet mit phyphox, welches über einen Luftdrucksensor verfügt. Dies ist bei allen Apple-Geräten der Fall und bei Android-Geräten typischerweise ab der „mittleren Preisklasse“ (vgl. [https://phyphox.org/sensordb](Sensordatenbank)).
- Je nach Experiment etwas, was zu einer Höhendifferenz führt (Aufzug, Rolltreppe, größerer Flaschenzug)

### Zeitaufwand

Die Messung kann alleine mit dem Smartphone jederzeit begonnen werden und dauert nur so lange wie der zu messende Vorgang. Sollen die Lerndenden die Berechnung der barometrischen Höhenformel selbst durch führen, ist hierfür Zeit einzuplanen.

## Aufbau

Bei Nutzung eines Aufzugs ist kein Aufbau notwendig. Bei Alternativen (Flaschenzug bzw. herablassen des Smartphones an einem Seil) sind entsprechende Vorbereitungen notwendig.

In phyphox muss lediglich die Konfiguration „Aufzug“ oder für Rohdaten „Luftdruck“ geöffnet werden. Auch hier sind keine weiteren Einstellungen notwendig.

## Durchführung

Öffne je nach Ziel des Versuchs die in phyphox integrierte Konfiguration „Aufzug“ (zur automatischen Berechnung von s-t-, v-t- und a-t-Diagrammen) oder „Luftdruck“ (um Rohdaten des Sensors aufzuzeichnen). Begib dich in den Aufzug un platziere das Smartphone auf dem Boden. Starte die Messung mit dem Dreieck-Symbol oben rechts und wähle im Aufzug eine Etage. Stoppe die Messung am Ende der Fahrt mit der Pause-Taste (parallele Linien).

## Datenanalyse

Je nach Beadrf und Aufgabenstellung.

---

## Physikalischer Hintergrund und Analysedetails

Die Konfiguration „Aufzug“ nutzt die „internationale Höhenformel“ um den Luftdruck \(p\) in eine Höhe \(h\) umzurechnen.

$$
h = \frac{288,15\,\mathrm{K}}{0,0065\,\mathrm{\frac{K}{m}}}\left(1-\left(\frac{p(h)}{1013,25\,\mathrm{hPa}}\right)^{\frac{1}{5,255}}\right)
$$

Da der Absolutwert unter anderem metereologischen Schwankungen unterliegt, wird der erste Messwert als Referenz genutzt und auf die Höhe Null gesetzt, so dass in Folge eine Höhendifferenz bestimmt wird. Zudem mittelt diese Konfiguration die Druckmessungen in Intervallen von 1s um das Rauschen zu reduzieren, auch wenn der verbaute Luftdrucksensor höhere Raten unterstützt.

Das a-t- Diagramm entspricht den Rohdaten der z-Achse (senkrecht zum Bildschirm) des Beschleunigungssensors.

## Probleme und Lösungen

* **Das a-t-Diagramm ist zu verrauscht**
  Das a-t-Diagramm entspricht der z-Achse des Beschleunigugnssensors, welche senkrecht zum Bildschirm liegt. Entsprechend muss das Smartphone flach liegen und darf nicht aufrecht gehalten werden. Zudem dominieren Vibrationen leicht die vergleichsweise geringe Beschleunigung eines Aufzugs. In diesen Fällen kann es helfen, das Smartphone nicht auf den Boden zu legen, sondern in der Hand zu halten, oder auf einen weichen, leicht dämpfenden Untergrund (Schaumstoff, Jacke,...) zu legen.
* **Der Luftdruck / Höhenverlauf ist unerwartet.**  
  Denke daran, dass die Messgröße Luftdruck auch anders beeinflusst werden kann. In Fahrzeugen werden Höhenunterschiede beispielsweise leicht durch Druckunterschiede in Tunneln oder den Staudruck über Lüftungen (vgl. Pitot-Rohr) überlagert. In sehr schnellen Aufzügen großer Gebäude sind teils Schächte zum Druckausgleich verbaut und das Lüftungssystem eines Gebäudes kann ebenso unerwartete Einflüsse haben. In größeren Passagierflugzeugen ist eine Höhenmessung unmöglich, dass der Kabinendruck künstlich reguliert wird.
* **Der Luftruck zeigt plötliche Schwankungen**
  Sollte es sich um ein wasserdichtes Smartphone handeln, kann der Druckausgleich zur Umgebung nur langsam erfolgen. Drückt man auch nur leicht auf das Gehäuse (schon beim Halten des Smartphones) kann eine kurzzeitige Druckänderung im Gerät entstehen, die die Messung überlagert.


## Variationen

Dieses Experiment erlaubt viele Variationen wie beispielsweise der Einsatz beim Treppensteigen, mit Seilzügen oder aber auch mit Smartphones, die an einer Drohne befestigt werden. Ebenso spannend sind Freizeitparkattraktionen wie Riesenräder oder Falltürme. Zu beachten ist, dass abhängig vom verwendeten Smartphone oder Tablet eine Auflösung von etwa einem Meter Höhenunterschied möglich ist und oft eine zeitliche Drift zu erkennen ist. Entsprechend sind Höhenunterschiede innerhalb eines Raumes meist nicht sinnvoll messbar, sondern man sollte Systeme suchen, die eine Beweugung über mehrere Etagen / mehrere Meter erzeugen.

## Arbeitsblätter / Material

Es sind derzeit keine Arbeitsblätter verfügbar. Eventuell findest du in anderen Sprachen dieser Seite Arbeitsblätter, die übersetzt werden können.

Wir freuen uns immer, wenn du Arbeitsblätter mit uns und anderen Nutzern teilst. Kontaktiere uns einfach unter contact@phyphox.org.

