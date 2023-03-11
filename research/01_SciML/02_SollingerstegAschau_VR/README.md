<!--https://mkrausai.github.io/research/01_SciML/01_BH_PedestrianBridge_XAI/-->
<script src='https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.4/MathJax.js?config=default'></script>


# Die Zukunft der Entscheidungsfindung bei Bauprojekten mit Virtual Reality (VR) am Beispiel der Fußgängerbrücke "Sollingersteg" in Aschau im Chiemgau

<!-- A repository of structural information on the design of pedestrian bridges
============================== -->

*   [Motivation und Zielsetzung](#description)
*   [Projektbeschreibung "Sollingersteg" in Aschau im Chiemgau](#content)
*   [Virtual Reality Demonstrator](#VRDemonstrator)
*   [Resümee](#conclusions)
*   [Beteiligte](#contributors)

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

<iframe src="https://www.google.com/maps/embed?pb=!1m14!1m12!1m3!1d167.5928082780064!2d12.323317008203363!3d47.77204415067!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!5e0!3m2!1sen!2sde!4v1678528976927!5m2!1sen!2sde" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
 <br />
Lage des Sollingerstegs in Aschau im Chiemgau, visualisiert via Google Maps (2023)<br />

Nachdem die Schäden an der alten Brücke festgestellt wurden, beschloss der Gemeinderat, einen Ersatzneubau zu errichten und beauftragte das Ingenieurbüro Köppl-Ingenieure Rosenheim mit der Ausarbeitung möglicher Varianten. Zur Auswahl standen eine Stahlbalkenbrücke, eine Holzbalkenbrücke, eine Holzfachwerkbrücke mit Überdachung, eine Holzbogenbrücke sowie eine Stahlfachwerkbrücke mit Rundrohrprofilen. Der Gemeinderat entschied sich schließlich für eine überdachte Holzfachwerkbrücke, bei der jedoch eine möglichst filigrane Konstruktion entwickelt werden sollte, um sich gut in die umliegende Bebauung einzufügen. Zur weiteren Entscheidungsfindung unter insbesonderer Berücksichtigung der Wirkung der Fußgängerbrücke alleine und in Interaktion mit der einbettenden Umgebung wird ein Virtual Reality Simulationsmodell erstellt.

## <a name="sec:VRDemonstrator"></a> Virtual Reality Demonstrator

Für die Pistensanierung 10-28 am Flughafen Zürich erstellten wir ein BIM-Modell, welches nicht nur Pläne und Bauteillisten generiert, sondern auch Einblick in den zukünftigen Flughafenbetrieb bietet und so eine effiziente Bewirtschaftung der Anlagen für die Zukunft garantiert. Weiter wurden für den Bauherrn verschiedene dynamische Virtual Reality-Simulationen der Ausfallszenarien von Befeuerungselementen bei Start- und Landesituationen mit der Software Unity erstellt, um die Sichtbarkeit der Piste aus dem Cockpit in Notfällen wie beispielsweise starkem Nebel überprüfen zu können.

Für eine objektive Darstellung der drei Varianten und um alle Unklarheiten im Hinblick auf die umliegende Bebauung zu klären, wurde das Gelände mithilfe eines Laserscans aufge-nommen und die Brückenvarianten wurden dort implementiert. usw….   


Our proposed framework for design subspace learning establishes a new paradigm for performance-conditioned exploration of design spaces, which is neither an optimisation setting nor a random process. Rather, it provides an intuitive and efficient cartography of the vastness of these design spaces. Instead of replacing human intuition with predefined, deterministic, quantitative rules, the AI acts as a design collaborator/co-pilot that augments the human designer's intuition on the problem at hand.

This research provides a variation of CVAEs tailored to forward and inverse design situations. We showed the potential of our CVAE in meta-modelling (i) the forward problem by providing a surrogate to estimate more efficiently and quickly design performances given design features, (ii) compression of complex design spaces into continuous, smooth, low-dimensional design subspaces. With a forward pass through our CVAE being extremely efficient, it can provide performance conditioned designs in quasi real-time and thus augment human designers by providing instant feedback and proposals during the iterative prototyping phase. Furthermore, with analytical derivatives inherently provided in neural networks, we demonstrated that the sensitivity analysis serves as powerful tool for both design optimisation as well as model interpretability. The latter is crucial for building trust and achieving wide acceptance of this kind of design augmentation tools in the AEC domain. The collected user responses prove our framework possesses the potential to find wide application in industry and research as a co-pilot for conceptual design studies in the AEC domain beyond pedestrian bridges.







## <a name="sec:conclusions"></a> Resümee

In einer weiteren Gemeinderatssitzung wurden verschiedene Varianten der Fachwerkbrücke vorgestellt und diskutiert, darunter eine reine Holzvariante und eine Variante mit Stahlrundstäben als Zugglieder. Schließlich wurde die Holz- und Stahlfachwerkbrücke als Kompromiss zwischen Nachhaltigkeit und filigraner Bauweise ausgewählt, da sie im Gegensatz zur reinen Holzvariante weniger massiv ist.



Für eine objektive Darstellung der drei Varianten und um alle Unklarheiten im Hinblick auf die umliegende Bebauung zu klären, wurde das Gelände mithi
*   [Schlussfolgerungen](#conclusions)



## <a name="sec:contributors"></a> Beteiligte

<img src="https://mkrausai.github.io/research/01_SciML/02_SollingerstegAschau_VR/figs/koeppl_portrait.jpg" width="20%" alt="Johannes" /><br />
**M.Eng. Johannes Köppl**<br />
Prokurist und Gesellschafter der Köppl-Ingenieure GmbH Rosenheim <br />

<img src="https://mkrausai.github.io/research/01_SciML/02_SollingerstegAschau_VR/figs/max.jpg" width="20%" alt="Max" /><br />
**M.Sc. Maximilian Rietschel **<br />
Gründer und Inhaber "Romantic Technologies" Zürich<br />

<img src="https://mkrausai.github.io/research/01_SciML/02_SollingerstegAschau_VR/figs/Eder_portrait.png" width="20%" alt="Fritz" /><br />
**M.Eng. Friedrich Eder**<br />
OTH Regensburg <br />

<img src="https://mkrausai.github.io/img/persons/Michael6_3.jpg" width="20%" alt="Michael" /><br />
**Dr. Michael A. Kraus, M.Sc.(hons)**<br />
Oberassistent and Co-Leitung des Immersive Design Lab von Design++ an der ETH Zürich<br />




<head>
	<title>Beteiligte</title>
	<style>
		.img-container {
			display: flex; /* Flex-Container */
			flex-wrap: wrap; /* Zeilenumbruch, falls nötig */
		}
		.img-container img {
			flex: 1; /* Alle Bilder gleich groß */
			margin: 5px; /* Abstand zwischen den Bildern */
			max-width: 100%; /* Bilder auf Containergröße beschränken */
			height: auto; /* Höhe automatisch anpassen */
		}
	</style>
</head>
<body>
	<div class="img-container">
		<img src="https://mkrausai.github.io/research/01_SciML/02_SollingerstegAschau_VR/figs/koeppl_portrait.jpg" alt="Johannes">
		<img src="https://mkrausai.github.io/research/01_SciML/02_SollingerstegAschau_VR/figs/max.jpg" alt="Max">
		<img src="https://mkrausai.github.io/research/01_SciML/02_SollingerstegAschau_VR/figs/Eder_portrait.png" alt="Fritz">
		<img src="https://mkrausai.github.io/img/persons/Michael6_3.jpg" alt="Michael">
	</div>
</body>
</html>


<div style="display:flex">
  <div style="flex:1; margin-right:10px">
    <img src="https://mkrausai.github.io/research/01_SciML/02_SollingerstegAschau_VR/figs/koeppl_portrait.jpg" alt="Johannes" style="width:100%">
    <div style="text-align:center">**M.Eng. Johannes Köppl**<br />
Prokurist und Gesellschafter der Köppl-Ingenieure GmbH Rosenheim <br /></div>
  </div>
  <div style="flex:1; margin-right:10px">
    <img src="bild2.jpg" alt="Bild 2" style="width:100%">
    <div style="text-align:center">Bild 2: Beschreibung des Bildes</div>
  </div>
  <div style="flex:1; margin-right:10px">
    <img src="bild3.jpg" alt="Bild 3" style="width:100%">
    <div style="text-align:center">Bild 3: Beschreibung des Bildes</div>
  </div>
  <div style="flex:1">
    <img src="bild4.jpg" alt="Bild 4" style="width:100%">
    <div style="text-align:center">Bild 4: Beschreibung des Bildes</div>
  </div>
</div>















# Kontakt und Projektleitung
Dr. Michael A. Kraus, M.Sc.(hons)
Institut für Baustatik und Konstruktion (IBK)
ETH Zürich
kraus@ibk.baug.ethz.ch
https://kaufmann.ibk.ethz.ch/de/personen/mitarbeitende/dr-michael-anton-kraus.html


------------
Shield: [![CC BY 4.0][cc-by-shield]][cc-by]

This work is licensed under a
[Creative Commons Attribution 4.0 International License][cc-by].

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg

