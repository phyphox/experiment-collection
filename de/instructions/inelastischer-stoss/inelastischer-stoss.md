--- 
translationKey: "Inelastic Collision Instruction"
title: "(In)elastischer Stoß"
date: 2024-12-17T11:42:40+01:00
draft: false
author: 
  - Sebastian Staacks
CreativeCommons: ['BY']
categories:
  - 'Mechanics'
sensors:
  - 'Microphone'
levels: ['2a', '2b', '3', '6']  # see doc for explanation. Remove everything else
video: ['Localized']
materials:
  - 'Household items'
tags: # All Tags start upper-case expect for 'phyphox'. This list can be expanded!
  - 'Ball'
  - 'Inelastischer Stoß'
  - 'Elastischer Stoß'
  - 'Energieerhaltung'
  - 'Freier Fall'
  - 'Akustische Stoppuhr'
summary: 'Bestimme die Anfangshöhe und die Energiebilanz eines springenden Balls anhand der Zeiten seiner Stoßgeräusche.'
version: '0.1.0'

---

{{< youtube sqCEo4tj3e4 >}}

## Überblick

In diesem Experiment lässt du einen Ball in der Nähe des Mikrofons deines Smartphones auf eine harte Oberfläche (z.B. einen Tisch) fallen. Phyphox erfasst die Geräusche bei jedem Aufprall des Balls auf der Oberfläche und verwendet deren Zeitpunkte, um die Fallhöhe des Balls zu bestimmen. Es zeigt die Maxima der Flugparabel zwischen den Aufprallen sowie die nach jedem Aufprall verbleibende kinetische Energie (relativ zur anfänglichen Energie).

### Abgedeckte Themen

Dieses Experiment kann verwendet werden, um den Energieerhaltungssatz und insbesondere die potenzielle und kinetische Energie zu besprechen. Es eignet sich auch zur Diskussion und Untersuchung von elastischen, plastischen und inelastischen Stößen. Da eine parabolische Flugbahn angenommen wird, kann es außerdem im Kontext eines einfachen parabelförmigen freien Falls verwendet werden, indem man die geschätzten Maximalhöhen zwischen den Aufprallen betrachtet. Um die von phyphox präsentierten Daten vollständig zu verstehen, sind jedoch ein Verständnis der Energie notwendig.

### Benötigte Materialien

- Smartphone oder Tablet mit phyphox
- Ball (kleiner Metallball, Golfball, …)
- Harte Oberfläche (z.B. Tisch) 
- Maßband oder Ähnliches wenn die phyphox-Ergebnisse geprüft werden sollen

### Zeitaufwand

Der Aufbau des Experiments dauert weniger als eine Minute. Abhängig vom Geräuschpegel in der Umgebung kann es jedoch einige Versuche erfordern, die Schwelle des Triggers (siehe „Probleme und Lösungen“) richtig einzustellen.

## Aufbau

Platziere dein Smartphone auf der Oberfläche oder auf einem Stativ in der Nähe der Oberfläche. Da das Geräusch des Ballaufpralls auf der Oberfläche erfasst werden soll, wird dringend empfohlen, so nah wie möglich am Aufprallpunkt zu sein, damit das Geräusch sich von Hintergrundgeräuschen im Raum abhebt.

Wähle in phyphox die Konfiguration „(In)elastic collision“ aus dem Hauptmenü. Starte die Messung, indem du auf das Dreieck in der oberen rechten Ecke drückst.

Je nach Geräuschpegel in deinem Raum, der Wahl des Balls und der Oberfläche sowie dem Smartphone-Modell musst du möglicherweise die „Schwelle“-Einstellung im Reiter „Einstellungen“ anpassen. Diese bestimmt, bei welcher Lautstärke (auf einer Skala von 0 bis 1) ein Geräusch als Ereignis gewertet wird.  Wenn Messwerte ohne hüpfenden Ball erscheinen, erhöhe die Schwelle von seinem Standard-Wert von 0,1. Wenn keine Messwerte erkannt werden, senke die Schwelle.

Der Parameter „Mindestvertzögerung“ verhindert Mehrfachzählungen einzelner Aufpralle, z.B. aufgrund von Nachhall. Der Standardwert von 0,1s ist in den meisten Fällen ausreichend.

## Durchführung

Stelle sicher, dass die Messung in phyphox läuft (Pause-Symbol wird in der oberen rechten Ecke angezeigt statt des dreieckigen Startsymbols). Setze die Messwerte über die „Reset“-Taste im Reiter „Höhen“ oder „Energie“ zurück. Lass den Ball neben dem Mikrofon des Smartphones fallen. Optional kannst du ein Maßband daneben halten um eine Referenzhöhe zu bestimmen.

Im Reiter „Höhen“ erscheinen bis zu fünf Zeitintervalle, die zu sechs Aufprallen gehören.

## Datenanalyse

Die Zeiten im Reiter „Höhen“ entsprechen den Zeitdifferenzen zwischen zwei Aufprallen auf der Oberfläche. Die Höhen 1 bis 5 entsprechen der maximalen Höhe, die der Ball im jeweiligen Zeitintervall erreicht hat. Höhe 0 ist die anfängliche Höhe **vor** dem ersten Aufprall, extrapoliert aus den Aufprallen 1 bis 3 (siehe Abschnitt „Physikalischer Hintergrund und Analysedetails“).

Der Reiter „Energie“ zeigt die zu den berechneten Höhen gehörenden Energiedaten an. Da die absolute Energie nicht bestimmt werden kann, wird die Energie der Höhe 1 auf 100% gesetzt. Das bedeutet, dass alle Energien als Bruchteil der potenziellen Energie der Höhe 1 aus dem Reiter „Höhen“ dargestellt werden. Folglich entsprechen die Energien 2 bis 5 der potenziellen Energie der Höhen 2 bis 5 und damit dem Verhältnis der Höhen 2 bis 5 zu Höhe 1. Die kleinere Angabe „Bei Stoß behalten“ ist das Verhältnis der potenziellen Energie des aktuellen Zeitintervalls zur potentiellen Energie des vorherigen Intervalls und stellt somit den Anteil der kinetischen Energie dar, der nach dem letzten Aufprall erhalten geblieben ist.

---

## Physikalischer Hintergrund und Analysedetails

Phyphox zeichnet Audiodaten des Smartphone-Mikrofons auf und analysiert sie sequentiell (wie in der Konfiguration „akustische Stoppuhr“). Die Samples werden auf einen Bereich von -1 bis 1 normalisiert, wobei die genaue Bedeutung dieser Amplitude je nach Aufnahmehardware des Smartphones variieren kann. Wenn ein Sample die vom Benutzer eingestellte Trigger-Schwelle überschreitet, wird dies als Ereignis gezählt und die Zeit vermerkt. Die Zeit basiert auf der Abtastrate, die typischerweise 48 kHz (oder in einigen Fällen 44,1 kHz) beträgt. Das ergibt eine theoretische zeitliche Auflösung von \(21\,\mathrm{\mu s}\) (bzw. \(23\,\mathrm{\mu s}\)). In der Praxis ist diese Auflösung jedoch durch Unterschiede in den Geräuschen verschiedener Aufpralle, Dispersion und die Form der Schallwelle begrenzt. Während phyphox intern exakte Werte nutzt, werden daher nur drei Dezimalstellen (1 ms) angezeigt.

Nach einem Ereignis werden die folgenden Audiosamples verworfen, bis die im unter „Mindestverzögerung“ eingestellte Zeit verstrichen ist. Danach wird das nächste Sample oberhalb der Schwelle als nächstes Ereignis erfasst. Die Zeitdifferenzen zwischen den aufeinanderfolgenden Ereignissen werden als „Zeit 1“, „Zeit 2“ usw. angezeigt.

Phyphox nimmt eine perfekte parabolische Flugbahn zwischen den Ereignissen an. Die Höhen „Höhe 1“ bis „Höhe 5“ werden nach folgender Formel berechnet:

\[
h_i = \frac{1}{8} g \Delta t_i^2
\]

mit \( \Delta t_i \) als zugehörigem „Zeit i“ und \( g \) als Erdbeschleunigung (\( 9,81 \, m/s^2 \)). Dies basiert auf der Formel für die Strecke eines Körpers unter konstanter Beschleunigung \( a \) aus dem Ruhezustand:

\[
d = \frac{1}{2}a t^2
\]

In diesem Experiment gilt \( a = g \) und \( \Delta t_i = 2t \), da das Zeitintervall sowohl den Aufstieg zur maximalen Höhe als auch den symmetrischen Abstieg umfasst.

Die Energien werden als potenzielle Energie an den höchsten Punkten der Flugbahn berechnet. Mit konstanter Masse und Erdbeschleunigung kann die potenzielle Energie \( E_i = m g h_i \) an jedem Maximum einfach als Bruchteil von \( E_1 \) ausgedrückt werden, nämlich als das Verhältnis der Höhen \( E_i / E_1 = h_i / h_1 \).

Die anfängliche Höhe \( h_0 \) wird extrapoliert, indem angenommen wird, dass das Verhältnis der potenziellen Energie vor und nach dem ersten Aufprall dem vor und nach dem zweiten Aufprall entspricht:

\begin{align*}
\frac{E_0}{E_1} &= \frac{h_0}{h_1} = \frac{h_1}{h_2} = \frac{t_1^2}{t_2^2} \\
\Rightarrow h_0 &= h_1 \frac{t_1^2}{t_2^2} = \frac{1}{8}g\frac{t_1^4}{t_2^2}
\end{align*}

In der Praxis wird die anfängliche Höhe häufig unterschätzt, da bei höheren Aufprallgeschwindigkeiten mehr Energie in Wärme umgewandelt wird. Der erste Aufprall hat typischerweise die höchste Geschwindigkeit und verliert damit einen höheren Anteil seiner Energie. Die Annahme eines gleichen Verlustfaktors führt somit zu einer Unterschätzung der potentiellen Energie vor dem ersten Aufprall und damit zu einer Unterschätzung der Anfangshöhe.


## Probleme und Lösungen

* **Phyphox erfasst nicht alle Aufpralle.**  
  Wenn die Messung auf einige Aufpralle oder laute Geräusche wie Klatschen reagiert, aber manche Aufpralle verpasst, ist die Triggerschwelle zu hoch eingestellt. Verringere die Schwelle, um sie an die Lautstärke der Aufprallgeräusche anzupassen, oder erhöhe die Lautstärke dieser Geräusche, indem du eine andere Ball-/Oberflächenkombination wählst. Du kannst dir auch die Lautstärke der Geräusche in der phyphox-Konfiguration „Audio Scope“ ansehen, welche Geräusche im gleichen Bereich von null bis eins wie die Triggerschwelle anzeigt.
* **Ereignisse werden registriert, obwohl der Ball nicht springt.**  
  In diesem Fall ist die Triggerschwelle zu niedrig eingestellt und/oder die Hintergrundgeräusche sind zu laut. Erhöhe die Schwelle so lange, bis die Messung nicht mehr durch Hintergrundgeräusche ausgelöst wird. Stelle sicher, dass das Aufprallgeräusch lauter ist als die Hintergrundgeräusche im Raum.
* **Einzelne Aufpralle werden mehrfach gezählt.**  
  Dies kann eine Folge einer zu niedrig eingestellten Triggerschwelle sein, da der Nachhall des Geräuschs noch über der Schwelle liegt. Versuche zunächst, die Schwelle zu erhöhen. Wenn dies keine Option ist, weil leisere spätere Aufpralle nicht erfasst werden oder die Umgebungsgeräusche zu laut sind, kannst du versuchen, die Einstellung „Mindestverzögerung“ zu erhöhen, um schnelle Ereignisse zu verhindern. Beachte jedoch, dass dies dazu führen kann, dass spätere, schneller aufeinanderfolgende Aufpralle nicht erfasst werden.
* **Die Energieanzeigen sind unplausibel (z.B. größer als 100 %).**  
  Überprüfe die Zeitintervalle im Reiter „Höhen“. Diese sind wahrscheinlich nicht korrekt, und es könnte ein sehr kurzes Intervall vorhanden sein, das durch einen doppelt gezählten Aufprall entstanden ist. Sieh dir die Lösungen für verpasste Aufpralle oder mehrfach gezählte Aufpralle an um korrekte Zeiten zu erhalten.


## Variationen

Dieses Experiment funktioniert auf verschiedenen Skalen, von Murmeln bis zu Basketbällen und von Zentimetern bis zu mehreren Metern. Beachte jedoch, dass Luftwiderstand eine Rolle spielen könnte und stark unterschiedliche Geräuschpegel eine Herausforderung sein können.

Das Experiment kann als Demonstration vor oder nach der Besprechung der zugrundeliegenden Berechnungen dienen. Es kann auch verwendet werden, um Stöße mit unterschiedlicher Elastizität zu untersuchen, z.B. durch Variieren der Ball-Oberflächen-Kombinationen.

Für eine systematische Untersuchung des Rückstoßkoeffizienten kann ein gut springender Ball (z.B. Golfball oder Stahlkugel) verwendet werden. Hier lässt sich die Elastizität des Stoßes schrittweise durch das Einfügen von Papierbögen zwischen Ball und Oberfläche reduzieren.

## Weitere Videos

{{< youtube 8Dd8Vi9GuzE >}}
{{< youtube _2K9aYdkt6Y >}}


## Arbeitsblätter / Material

Es sind derzeit keine Arbeitsblätter verfügbar. Eventuell findest du in anderen Sprachen dieser Seite Arbeitsblätter, die übersetzt werden können.

Wir freuen uns immer, wenn du Arbeitsblätter mit uns und anderen Nutzern teilst. Kontaktiere uns einfach unter contact@phyphox.org.

