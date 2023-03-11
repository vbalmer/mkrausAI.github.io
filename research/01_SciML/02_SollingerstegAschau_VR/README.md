<script src='https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.4/MathJax.js?config=default'></script>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

# Die Zukunft der Entscheidungsfindung bei Bauprojekten mit Virtual Reality (VR) am Beispiel der Fußgängerbrücke "Sollingersteg" in Aschau im Chiemgau

<!-- A repository of structural information on the design of pedestrian bridges
============================== -->

*   [Motivation und Zielsetzung](#description)
*   [Projektbeschreibung "Sollingersteg" in Aschau im Chiemgau](#content)
*   [Virtual Reality Demonstrator](#VRDemonstrator)
*   [Resümee](#conclusions)
*   [Team und Kontakt](#contributors)

<!-- -->
<!-- *   [Citation](#citation)-->

## <a name="description"></a>Motivation und Zielsetzung

Das Potenzial von Augmented Reality (AR) für den Hoch- und Ingenieurbau ist groß, jedoch bleiben derzeitige Anwendungen in der Praxis eher Prototypen. Gerade die konzeptionelle Entwurfsphase eines Bauprojektes bedingt die Einbindung der Interessen und Bedürfnisse diverser beteiligter Personen und Gruppen, für welche die technische Sprache der Planenden sowie die Form der Entwurfskommunikation in Planabstraktionen, statischen Modellen oder Prinzipskizzen eine Verständnishürde darstellt. Dabei ist aber das Erzielen einer Paretooptimalität aufgrund des gegenseitigen Verständnisses in dieser ersten Phase eines Bauwerks essenziell um die spätere Akzeptanz und Zufriedenheit in der Breite der betroffenen und beteiligten Personen zu garantieren. Bei öffentlichen Bauprojekten steht dabei die frühzeitige Demokratisierung der Entscheidungsfindung über diverse Formen der Bürgerinformation und -beteiligung immer stärker im Fokus. Daher hat sich im Rahmen dieses Projekts ein Team aus Bauherrenschaft, Planung und Forschung zusammengeschlossen, um die technischen und organisatorischen Herausforderungen dafür zu erarbeiten und eine effiziente und ansprechende Lösung mithilfe von Virtual Reality (VR) zu entwickeln.

Mit der Entwicklung im Rahmen dieses Projekts werden folgende Ziele verfolgt: 
* Entwicklung eines Ansatzes zur Datenintegration von GIS und BIM Modellen in eine VR Entwicklungsumgebung
* Herleitung der notwendigen Komponenten zur Ausgestaltung der VR Simulation (Informationen, Steuerung, Detailtiefe) 
* Umsetzung mehrerer Entwurfsvarianten in der VR Umgebung
* Durchführung und Evaluation von Demonstrationsanwendungen mit dem Entwicklerteam und der Bauherrenschaft
* Durchführung und Evaluation der analogen und online Bürgerbeteiligung

Im Rahmen dieses Projektes konnten wir die erfolgreiche technische und organisatorische Anwendbarkeit unseres Ansatzes demonstrieren, sodass künftig weitere Bauprojekte in der konzeptionellen Entwurfsphase begleitet werden können. Damit fördern wir die weitere Verbreitung und den Einsatz solcher Werkzeuge in der Praxis und bauen Schranken für die Bürgerbeteiligung ab.


## <a name="content"></a> Projektbeschreibung "Sollingersteg" in Aschau im Chiemgau
Aschau im Chiemgau ist eine Gemeinde im oberbayerischen Landkreis Rosenheim, die sich inmitten des malerischen Prientals befindet. Die Gemeinde besteht aus den beiden Hauptorten Aschau und Sachrang und wird durch den Fluss Prien buchstäblich geteilt. Aufgrund dieser Lage gibt es in der Gemeinde zahlreiche Brücken, die eine wichtige Rolle in der Infrastruktur spielen, insbesondere für Fußgänger und Radfahrer. Neben den Hauptverkehrswegen für den Luftkurort müssen diese Brücken regelmäßig gewartet und instand gehalten werden.

Die letzte Bauwerksprüfung des Sollingerstegs, einer 21 Meter weit gespannten Fußgängerbrücke im Ortskern neben dem Rathaus gelegen, hat ergeben, dass die Stahlkonstruktion durch starke Korrosion stark geschädigt ist. Eine Sanierung ist aufgrund der einbetonierten Haupttragelemente in den Widerlagern nicht wirtschaftlich durchführbar. Der Sollingersteg ist einer der wichtigsten Verkehrswege für Fußgänger und Radfahrer in der Gemeinde, aber mit seiner aktuellen lichten Breite von ca. 1,80 m nicht mehr zeitgemäß für einen hochfrequentierten Fußweg. Die Stahlkonstruktion besteht aus zwei Längsträgern aus IPE-Profilen, die durch einen Längsverband aus Winkelprofilen am Untergurt verstärkt sind. Die beiden Längsträger sind schließlich am Widerlager biegesteif eingebunden.

<div style="text-align:center;">
<iframe src="https://www.google.com/maps/embed?pb=!1m14!1m12!1m3!1d167.5928082780064!2d12.323317008203363!3d47.77204415067!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!5e0!3m2!1sen!2sde!4v1678528976927!5m2!1sen!2sde" width="500" height="400" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
<p style="font-weight:bold; color:blue;"> Abbildung 1: Lage des Sollingerstegs in Aschau im Chiemgau, visualisiert via Google Maps (2023)</p>
</div>

Nachdem die Schäden an der alten Brücke festgestellt wurden, beschloss der Gemeinderat, einen Ersatzneubau zu errichten und beauftragte das Ingenieurbüro Köppl-Ingenieure Rosenheim mit der Ausarbeitung möglicher Varianten. Zur Auswahl standen eine Stahlbalkenbrücke, eine Holzbalkenbrücke, eine Holzfachwerkbrücke mit Überdachung, eine Holzbogenbrücke sowie eine Stahlfachwerkbrücke mit Rundrohrprofilen. Der Gemeinderat entschied sich schließlich für eine überdachte Holzfachwerkbrücke, bei der jedoch eine möglichst filigrane Konstruktion entwickelt werden sollte, um sich gut in die umliegende Bebauung einzufügen. Zur weiteren Entscheidungsfindung unter insbesonderer Berücksichtigung der Wirkung der Fußgängerbrücke alleine und in Interaktion mit der einbettenden Umgebung wird ein Virtual Reality Simulationsmodell erstellt.


## <a name="sec:VRDemonstrator"></a> Virtual Reality Demonstrator
Im Zuge der weiteren Planung sollen nun zwei Entwurfsalternativen mit Bedachung sowie eine Konstruktion ohne Dach gegenübergestellt werden. Zur besseren und barrierefreieren Kommunikation der technischen Planung mit allen Beteiligten und der Öffentlichkeit wird dies anhand eines VR-Demonstrators vorgenommen.

Das VR Modell ist dabei als interaktives 3D-Modell der Umgebung (Ausschnitt 1 km x 1 km) des Ortes Aschau im Chiemgau, der lokalen Bebauung (im LOD200) sowie der drei Brückenvarianten im LOD 300. Die Interaktion zwischen App und Nutzenden findet einerseits über ein Textfeld auf dem Tablet und andererseits über die Controllertasten statt. Benutzende können sich mit Hilfe der Controllertasten oder eines Teleportationsstrahls frei bewegen (vgl. Abbildung 2a). In der VR Umgebung können Benutzende die drei Brückenvarianten (vgl. Abbildung 2a) aus verschiedenen Blickwinkeln betrachten. Hierbei kann einerseits auf fünf vordefinierte Betrachtungsstandorte (gelbe Markierungen in Abbildung 2a) zurückgegriffen werden. Andererseits erlauben die beiden Hand-Controller die Drehung des Modells oder einen Ortswechsel mittels Teleportation oder Translation. Eine beispielhafter Ausschnitt aus der VR Simulation ist als Ansicht des Portals der Brückenvariante 2 in Abbildung 2b dargestellt.

<div style="display: flex; justify-content: center;">
  <div style="display: flex; flex-direction: row;">
    <div style="margin: 10px;">
      <img src="https://mkrausai.github.io/research/01_SciML/02_SollingerstegAschau_VR/figs/Snapshot_3.PNG" alt="Bild 1" style="height: 350px;">
      <p style="text-align: center; font-weight: bold;"> (a)</p>
    </div>
    <div style="margin: 10px;">
      <img src="https://mkrausai.github.io/research/01_SciML/02_SollingerstegAschau_VR/figs/Snapshot_2.PNG" alt="Bild 2" style="height: 350px;">
      <p style="text-align: center; font-weight: bold;">(b)</p>
    </div>
  </div>
  <br>
  <p style="font-weight:bold; color:blue;"> Abbildung 2: a) Bedienfeld; b) Ansicht des Portals der Brückenvariante 2</p>
</div>

Da wir davon ausgehen, dass die allermeisten Projektteilnehmer aber auch Bürgerinnen und Bürger mit VR nicht vertraut sind, wird vor der Benutzung ein einführendes Tutorial angeboten, welches die wichtigsten Funktionen erklärt. Die anschließende Erkundungsphase zur Exploration der Umgebung und der drei Brückenvarianten ist dann personenzentriert und erfolgt ohne weitere Anleitung. Dabei können die beschriebenen Funktionalitäten genutzt werden.

<div style="text-align:center;">
  <iframe width="896" height="504" src="https://www.youtube.com/embed/qbr8kGF8zXU" title="VR Walk Aschau" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<p style="font-weight:bold; color:blue;"> Abbildung 3: VR Rundgang über die Brückenvarianten "Sollingersteg Aschau im Chiemgau"</p> </div>

Die Umsetzung im Rahmen dieses Projektes erfolgte mit Unity auf einer Oculus Quest 2. 



Für eine realistische Darstellung der drei Varianten und um alle Unklarheiten im Hinblick auf die umliegende Bebauung zu klären, wurde das Gelände maßstabsgetreu als GIS Modell in Unity 

mithilfe eines Laserscans aufgenommen und die Brückenvarianten wurden dort implementiert.   

Für die Pistensanierung 10-28 am Flughafen Zürich erstellten wir ein BIM-Modell, welches nicht nur Pläne und Bauteillisten generiert, sondern auch Einblick in den zukünftigen Flughafenbetrieb bietet und so eine effiziente Bewirtschaftung der Anlagen für die Zukunft garantiert. Weiter wurden für den Bauherrn verschiedene dynamische Virtual Reality-Simulationen der Ausfallszenarien von Befeuerungselementen bei Start- und Landesituationen mit der Software Unity erstellt, um die Sichtbarkeit der Piste aus dem Cockpit in Notfällen wie beispielsweise starkem Nebel überprüfen zu können.





<img class="centered-image" src="https://mkrausai.github.io/research/01_SciML/02_SollingerstegAschau_VR/figs/Snapshot.PNG" width="50%" alt="VR_Walk" /><br />
[![Abbildung 2: VR Rundgang über die Brückenvarianten beim "Sollingersteg Aschau im Chiemgau"]()](https://www.youtube.com/watch?v=qbr8kGF8zXU&t=1s "VR Rundgang über die Brückenvarianten beim "Sollingersteg Aschau im Chiemgau"")



## <a name="sec:conclusions"></a> Resümee

In einer weiteren Gemeinderatssitzung wurden verschiedene Varianten der Fachwerkbrücke vorgestellt und diskutiert, darunter eine reine Holzvariante und eine Variante mit Stahlrundstäben als Zugglieder. Schließlich wurde die Holz- und Stahlfachwerkbrücke als Kompromiss zwischen Nachhaltigkeit und filigraner Bauweise ausgewählt, da sie im Gegensatz zur reinen Holzvariante weniger massiv ist.



Für eine objektive Darstellung der drei Varianten und um alle Unklarheiten im Hinblick auf die umliegende Bebauung zu klären, wurde das Gelände mithi


## <a name="sec:contributors"></a> Team und Kontakt

Diese Arbeit wurde von der Gemeinde Aschau im Chiemgau beauftragt und von den im Folgenden benannten Personen bearbeitet und umgesetzt.

### Projektleitung und Kontakt 

<h5>Bauherrenschaft</h5>
<p>Erster Bürgermeister Simon Frank</p>
<p>Gemeinde Aschau im Chiemgau</p>
<p>Webseite: <a href="https://www.gemeinde-aschau.de/">https://www.gemeinde-aschau.de/</a></p>

<h5>Entwurf und Tragwerksplanung</h5>
<p>M.Eng. Johannes Köppl</p>
<p>Köppl-Ingenieure GmbH Rosenheim</p>
<p>Email: kraus@ibk.baug.ethz.ch</p>
<p>Webseite: <a href="https://www.koeppl-ingenieure.de/">https://www.koeppl-ingenieure.de/</a></p>

<h5>Virtual Reality</h5>
<p>Dr. Michael A. Kraus, M.Sc.(hons)</p>
<p>Institut für Baustatik und Konstruktion (IBK)</p>
<p>ETH Zürich</p>
<p>Email: kraus@ibk.baug.ethz.ch</p>
<p>Webseite: <a href="https://kaufmann.ibk.ethz.ch/de/personen/mitarbeitende/dr-michael-anton-kraus.html">https://kaufmann.ibk.ethz.ch/de/personen/mitarbeitende/dr-michael-anton-kraus.html</a></p>


### <a name="sec:contributors"></a> Beteiligte

<div style="display:flex">
  <div style="flex:1; margin-right:10px">
    <img src="https://mkrausai.github.io/img/persons/Michael6_3.jpg" alt="Michael" style="width:100%">
    <div style="text-align:center"> Dr. Michael A. Kraus, M.Sc.(hons) <br />
Oberassistent and Co-Leitung des Immersive Design Lab von Design++ an der ETH Zürich <br /></div>
  </div>
  <div style="flex:1; margin-right:10px">
    <img src="https://mkrausai.github.io/research/01_SciML/02_SollingerstegAschau_VR/figs/koeppl_portrait.jpg" alt="Bild 2" style="width:100%">
    <div style="text-align:center">M.Eng. Johannes Köppl<br />
Prokurist und Gesellschafter der Köppl-Ingenieure GmbH Rosenheim <br /></div>
  </div>
  <div style="flex:1; margin-right:10px">
    <img src="https://mkrausai.github.io/research/01_SciML/02_SollingerstegAschau_VR/figs/max.jpg" alt="Max" style="width:100%">
    <div style="text-align:center">M.Sc. Maximilian Rietschel <br /> Gründer und Inhaber "Romantic Technologies" Zürich</div>
  </div>
  <div style="flex:1">
    <img src="https://mkrausai.github.io/research/01_SciML/02_SollingerstegAschau_VR/figs/Eder_portrait.png" alt="Fritz" style="width:95%">
    <div style="text-align:center"> M.Eng. Friedrich Eder <br /> Consultant für Softwareentwicklung und BIM </div>
  </div>
</div>

------------
Shield: [![CC BY 4.0][cc-by-shield]][cc-by]

This work is licensed under a
[Creative Commons Attribution 4.0 International License][cc-by].

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg

