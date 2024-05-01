<p align="center">
    <img width="100%" src="./documentation/Banner_white-mode.png#gh-light-mode-only" alt="Dokument Header">
    <img width="100%" src="./documentation/Banner_dark-mode.png#gh-dark-mode-only" alt="Dokument Header">
</p>


![Programmiersprache Scratch](https://img.shields.io/badge/Language-Scratch-%23855cd6?link=https://scratch.mit.edu/)
![Schulprojekt](https://img.shields.io/badge/Schulprojekt-green?link=gymnasium-warstein.de)
![Note](https://img.shields.io/badge/Note-nicht_erteilt-orange)
![Mitwirkende](https://img.shields.io/badge/Mitwirkende-3-blue)
![Letzter Commit](https://img.shields.io/github/last-commit/RedLion8399/EV3_rubiks_cube-solver.svg)
![Lizens](https://img.shields.io/github/license/RedLion8399/EV3_rubiks_cube-solver.svg)
![Veröffentlichung](https://img.shields.io/github/release/RedLion8399/EV3_rubiks_cube-solver.svg)


## :page_facing_up: Inhaltsverzeichnis
- :book: [Einleitung](#Einleitung)
- :computer: [Hard-/Softwarevorraussetzungen](#Hard-/Softwarevorraussetzungen)
- :hammer_and_wrench:[Installation](#Installation)
- :arrow_forward: [Anwendung](#Anwendung)
- :books:[Weiterführende Dokumenation](#Weiterführende_Dokumenation)
- :clap:[Danksagung](#Danksagung)


## :book: Einleitung
DAs EV3 Rubiks Cube Solver berechnet den Lösungsweg eines Zauberwürfels mithilfe eines [Algorythmus](https://github.com/RedLion8399/EV3_rubiks_cube-solver/wiki/Algorithmen). Dazu muss der Nutzer den Würfel manuell einscannen. Gelöst wird der Würfel mit zwei Motoren, die ihn aus Sicht des Roboters, um die x-Achse und die y-Achse rotierem, woraus sich alle weiteren Bewegungsmuster ergeben.


## :computer: Hard-/Softwarevorraussetzungen
- EV3 Clasroom als Entwicklungsumgebung
> [Download for Windows](https://education.lego.com/_/downloads/EV3_Classroom_Windows_1.5.3_Global.msi) oder im [Microsoft Store](ms-windows-store://pdp?launch=true&mode=full&hl=de-de&gl=de&ocid=bingwebsearch&productid=9p8sjvzm63sz&referrer=storeforweb&source=https%3A%2F%2Fwww.bing.com%2F)  
> [Download für MacOS](https://education.lego.com/_/downloads/EV3_1.50_Global.dmg) oder im [App Store](https://apps.apple.com/us/app/ev3-classroom-lego-education/id1502412247)

- LEGO Mindstorms EV3 Stein  
    - Zwei Motoren
    - Einen Farbsensor
    - Zwei Tastsensoren

<div name="Anschlussbelegung">Die Belegung der Anschlüsse erflgt folgendermaßen:</div>

Port | Belegung
---|---
A|Motor zum Drehen des Würfels
B|Motor zum Kippen des Würfels
C|-
D|-
-|
1|Farbsensor
2|-
3|Tastsensor zum Wiederrufen der eingabe
4|Tastsensor zum Bestätigen der Eingsbe

- Motor-A so konfigurriert sein, dass durch eine Drehung um 90°, der Würfel um eine Seite entlang der y-Achse rotiert wird.  
- Motor-B muss so konfigurruert sein, dass durch eine Drehung um 180° im Uhrzeigersinn aus der Ausgangsposition der Würfel antlang der x-Achse gekippt wird. 


> [!IMPORTANT]
> Wenn ihr Roboter eine andere Übersetzung verwendet, kann es erforderlich sein, die Orginalwerte anzupassen. Was sie anpassen müssen, erfahren sie [hier](https://github.com/RedLion8399/EV3_rubiks_cube-solver/wiki/Funktionsweise/motor-functions).


## :hammer_and_wrench: Installation
Es gibt mehrere Optionen, um das Programm zu erhalten und auszuführen.

- Dierekter [Download](https://github.com/RedLion8399/EV3_rubiks_cube-solver/archive/refs/heads/main.zip) des Repositories
- Klonen des Repositories (setzt die Installation von git vorraus)

  ```bash
  cd{gewünschter-Pfad}
  ```

  ```bash
  git clone https://github.com/RedLion8399/EV3_rubiks_cube-solver.git
  ```

- Herrunterladen des Programms auf den EV3 Stein
  - Ablegen der Projekt-Datei über den Datei Explorer - setzt Verbindung per Kabel vorraus
  - Download über die EV3 [Clasroom App](#Hard-softwarevorraussetzungen)


## :arrow_forward: Anwendung
1. Starten des Programms
2. Einscannen des Zauberwürfels gemäß der Anweisungen auf dem Display
   1. Ausrichten des Würfels
   2. positionieren des Farbsensors über der Kachel
   3. Betätigen des [Tastsensors zum Bestätigen](#Anschlussbelegung)
   4. Bwginnend in der hinteren linken Ecke, nach rechts fortfahren. Danach die jewails daruntergelegene reihe einscannen.
   5. Die einzelnen Seiten in der vorgegebenen Reiehnfolge einscannen
3. Stellen des Zauberwürfels auf den Drehteller. Aus der Perspektive des Steins befindet sich der rote Mittelpunkt vorne und der weiße Mittelpunkt oben. Betätigen des [Tastsensors zum Bestätigen](#Anschlussbelegung)
4. Auf die Lösung des Würfels warten


## :books: Weiterführende Dokumenation
Falls sie weitergehende Informationen zu diesem Projekt haben möchten, empfielt es sich, das [Wiki](https://github.com/RedLion8399/EV3_rubiks_cube-solver/wiki) dieses Repositories aufzusuchen.

Aufgrund der Komplexität des Programms ist es nicht möglich, den gesamten Funktionsumfang hier abzubilden. Dazu existiert ein Eintrag im [Wiki](https://github.com/RedLion8399/EV3_rubiks_cube-solver/wiki/Funktionsweise).

Bei der Ausführung des Programms können Fehler auftreten. Einige davon sind auf irritierende Scratch Mechaniken zurückzuführen. diese sind [hier](https://github.com/RedLion8399/EV3_rubiks_cube-solver/wiki/Bugs-and-Problems) dokumentiert.

Der Algorythmus zur Lösung dieses Projekts ist nicht optimal und sehr zeitaufwendig, jedoch nicht möglich, anders umzusetzen (siehe [Bugs- und Probleme](https://github.com/RedLion8399/EV3_rubiks_cube-solver/wiki/Bugs-and-Problems) dokumentiert.)  
[Dieser und weitere Algorythmen](https://github.com/RedLion8399/EV3_rubiks_cube-solver/wiki/Algorithmen) sind ebenfalls im Wiki zu finden.


## :clap: Danksagung
Vielen Dank an das Team, als das wir dieses Projekt entgegen aller Hürden umgesetzt haben.

Vielen Dank Lena für die große Unterstützung bei der Entwicklung des Codes, das einbringen deines Wissens, ohne welches das Projekt nicht möglich gewesen wäre, über das Lösen des zauberwürfels und das Fertigstellen der Hardware.

Danke Eric für die initiale Idee zum Projekt und das anfertigen des ersten Prototypen, der die Grundlage für das heutige Endresultat gelegt haben.

---

Wir möchten uns außerdem bei unserer Informatik Lehrerin Frau Sina bedanken, die uns bei der Umsetzung sehr unterstützt hat und für die zahllosen [Prbleme](https://github.com/RedLion8399/EV3_rubiks_cube-solver/wiki/Bugs-and-Problems) stets versucht hat eine Lösung zu finden.

---

Einige Teile der Hardware stammen nicht initial von uns, sondern sind von einem fertigen Projekt inspirriert oder daraus übernommen. Der [MindCub3r](https://www.mindcuber.com/mindcub3r/mindcub3r.html) ist eine großartige Vorlage, die zudem besser funktioniert, als usere Version, was teils darauf zurückuführen ist, dass uns weiniger Bauteile zur Verfügung stehen und wir eine andere Programmiersprache verwendet haben.

Die Programmierung ist jedoch vollkommen eigenständig.