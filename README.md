# MPT_SS23_Gr.2_VR-Fencing
 
This Unity project uses the version `2022.3.4f1`<br>
It is build for the Oculus Quest VR-headset with controllers<br>

Das Projekt "MPT_SS23_Gr.2_VR-Fencing" wird im Rahmen des Angewandte Informatik Studiums in der Vertiefunsgrichtung "Medieninformatik" im Modul "Medienprojekt" entwickelt.

Diese VR-Anwendung soll dem Nutzer die Möglichkeit bieten, die Grundlagen des Fechtens spielerisch in einer virtuellen Umgebung zu erlernen. Die Grundlagen umfassen hierbei das Blocken sowie Angreifen.
Trainiert wird mittels eines Fecht-Trainers, welcher gegnen den Nutzer antritt. Die Trainingseinheiten sind  unterteilt in "Blocken", "Angreifen", und "Freier Modus".

1. [Spielablauf](#spielablauf)
2. [Verwendete Technologien](#verwendete-technologien)
3. [Verwendete Plugins](#verwendete-plugins)
6. [Probleme bei der Entwicklung](#probleme-bei-der-entwicklung)
7. [Zu den Entwicklern](#zu-den-entwicklern)

## Spielablauf
Zunächst wählt der Nutzer einen Spiel-Modi. Zu Verfügung stehen "Blocken", "Angreifen", und "Freier Modus". Danach geht es in die jeweilige Trainingseinheit. Die unterschiedlichen Trainingseinheiten sind zusätzlich in je 3 Schwierigkeitsgrade unterteilt:

#### "Blocken"-Trainingseinheit
In der ersten Phase des Tranings wird der Trainer dem Nutzer zeigen, wie dieser den Degen führen muss, um bestimmte Angriffe abzublocken. Hierfür nimmt der Trainer die Position des Nutzers ein, und zeigt diesem durch seine eigene Schwertführung, wie der Nutzer die Bewegung richtig ausführt. Hat der Nutzer dies gemeistert, geht es zur zweiten Phase über. 
In der zweiten Phase stellt sich der Trainer gegenüber des Nutzers und sagt an, wohin er den Nutzer angreifen wird; bswp. "links unten". Der Spieler muss daraufhin innerhalb einer festgelegten Geschwindigkeit den Degen in die Abwehrposition bringen. Hat er dies gut gemeistert, gibt es Pukte für die richtig ausgeführte Bewegung. Ist die Bewegung hingegen nicht zufriednstellend ausgeführt, wird der Trainer erneut in Phase 1 übergehen und dem Nutzer nochmals zeigen, wie die Bewegung richtig ausgeführt wird.

#### "Angreifen"-Trainingseinheit
In der ersten Phase des Tranings wird der Trainer dem Nutzer zeigen, wie dieser den Degen führen muss, um bestimmte Angriffe auszuführen. Hierfür nimmt der Trainer die Position des Nutzers ein, und zeigt diesem durch seine eigene Schwertführung, wie der Nutzer die Bewegung richtig ausführt. Hat der Nutzer dies gemeistert, geht es zur zweiten Phase über. 
In der zweiten Phase stellt sich der Trainer gegenüber des Nutzers und sagt an, wohin der Nutzer angreifen soll; bswp. "rechts oben". Der Spieler muss daraufhin innerhalb einer festgelegten Geschwindigkeit mit den Degen die entsprechnde Angriffsbewegung ausführen. Hat er dies gut gemeistert, gibt es Pukte für die richtig ausgeführte Bewegung. Ist die Bewegung hingegen nicht zufriednstellend ausgeführt, wird der Trainer erneut in Phase 1 übergehen und dem Nutzer nochmals zeigen, wie die Bewegung richtig ausgeführt wird.
Dieser Modus wurde aus Zeitgründen noch nicht implementiert.

#### "Freier Modus"-Trainingseinheit
Im freien Modus wird alles erlernte vom Spieler gefordert in zufälliger Reihenfolge; sprich Blocken und Angreifen abwechselnd.
Dieser Modus wurde aus Zeitgründen noch nicht implementiert.


## Verwendete Technologien
Zur Erstellung des Fecht-Simulators wurde die Unity Game Engine in der Version 2021.3.12f1 verwendet und später dann in der Version 2022.3.4f1. Für die Erstellung der Animationen des Fecht-Trainers wurde Blender benutzt. Zum Erproben der Anwendung und Testen wurde das Oculus Quest VR-Headset mit Controllern verwendet. 


## Verwendete Plugins
Folgende Plugins wurden dem Projekt hinzugefügt: -offen- <br>
Des Weiteren wurde zunächst das PDollar Point-Cloud Gesture Recognizer Plugin und auch das MiVRy Plugin verwendet. Diese wurden jedoch im Laufe der Entwicklung verworfen, da beide Probleme mit sich brachten, welche wir in der vorgegebenen Zeit nicht beheben konnten. Mehr dazu bei Punkt "Probleme bei der Entwicklung".<br>


## Probleme bei der Entwicklung

#### Allgemein
Als allgemeine Schwierigkeit bei der Entwicklung lässt sich vor Allem der momentane Stand der VR-Spieleentwicklung nennen. Es gibt zwar so einige Tutorials, welche einem den Einstieg etwas erleichtern, jedoch anders als bei der Entwicklung anderer Projekte (zB. Webseiten, Apps, etc) gibt es selten Tutorials, welche spezifische Lösungsansätze für die aufkommenden, spezifischen Probleme bieten. Das hat die Entwicklung ungemein erschwert und auch teilweise recht langsam vorangehen lassen, da man sich erst ausgiebigst mit einem spezifischen Problem auseinandersetzen musste und eigene Lösungen dafür herausfinden bzw Alternativen, welche nicht immer zum Erfolg geführt haben. Dadurch hat man natürlich auf der einen Seite ein ganz anderes Verständnis für den Code und die GameObjects welche man schreibt und benutzt; auf der anderen Seite jedoch war die Zeit für dieses Projekt eben sehr knapp bemessen und dadurch hat man einige Features des Spiels leider nicht mehr umsetzen können. <br>

#### Probleme bezüglich der Plugins PDollar & MiVRy
Beide Plugins sollten ursprünglich zur Erkennung der Gesten, welcher der Nutzer ausführen muss um die Angriffe korrekt auszuführen bzw. zu blocken, benutzt werden. Das PDollar Plugin wurde recht schnell verworfen als mögliche Umsetzung der Gesten-Erkennung, da der PDollar-Algorithmus, auf welchen das Plugin basiert, in jetzigem Stand des Plugins nur in 2D 
Gesten erkennen kann. In Anbetracht dessen, dass wir dreidimensionale Gesten erkennen müssen, um ein realistisches Fecht-Gefühl zu vermitteln, bietet sich das Pdollar Plugin also nur begrenzt an. <br>
Auf der Suche nach besser geeigneten Plugins, welche die Gestenerkennung in VR ermöglichen, sind wir auf das MiVRy Plugin von dem Entwickler-Team MARUI gestoßen. Dieses Plugin ermöglicht es, Gesten in 3D aufzunehmen und zu erkennen. Alles in Allem war dieses Plugin perfekt für unser Vorhaben und auch das Aufnehmen und Abfragen der erforderlichen Gesten hat ausgezeichnet funktioniert. Jedoch gab es bei der Integrierung der erforderlichen Scripte in unseren eigenen Szenen erhebliche Probleme seitens der Controllererkennung. Diese Probleme konnten leider bis zum Schluss nicht behoben werden und so sahen wir uns gezwungen, unsere Gesten-Erkennung nochmals neu zu überlegen.


## Zu den Entwicklern
Die Entwickler dieses studentischen Projektes sind<br>
[Lucas Hengelhaupt](https://github.com/Diafreak),<br>
[Henning Venhorst](https://github.com/HenningCV),<br>
[Eric Kruse](https://github.com/EricKruse)<br>
und [Saskia Wohlers](https://github.com/schnoernja).
