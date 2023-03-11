<!--https://mkrausai.github.io/research/01_SciML/01_BH_PedestrianBridge_XAI/-->
<script src='https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.4/MathJax.js?config=default'></script>


# Virtual Reality (VR) Explainable AI for Conceptual Generative Design of a Pedestrian Bridge

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

The objective of this research is to 
*   develop a synthetic dataset generation pipeline for quantifyable (structural) design performances
*   implement, train and evaluate a suitable design meta-model for the forward and inverse design setting
*   create a demonstrator application of an explainable and intuitive co-pilot for conceptual design. 

We demonstrate the applicability of this approach in the forward as well as inverse design setting for the generic example of a bridge st engineers or project managers with limited expertise in ML or AI and fosters wide-spread use of such tools in practice.


## <a name="content"></a> Projektbeschreibung "Sollingersteg" in Aschau im Chiemgau
Aschau im Chiemgau ist eine Gemeinde im oberbayerischen Landkreis Rosenheim mit den beiden Hauptorten Aschau und Sachrang. Die Gemeinde ist inmitten des Prientals gelegen und was dazu führt, dass der Ort durch Fluss Prien sprichwörtlich geteilt wird. Aus diesem Grund besitzt die Gemeinde Aschau viele Brückenbauwerke, die neben den Hauptverkehrswegen für den Luftkurort einen wichtigen Faktor in der vorherrschenden Infrastruktur, vor allem für Fußgänger und Radfahrer darstellen. Diese Bauwerke müssen regelmäßig gewartet bzw. saniert werden. 

Bei der letzten Bauwerksprüfung des Sollingerstegs, eine Fußgängerbrücke im Ortskern direkt neben dem Rathaus gelegen wurde festgestellt, dass die Stahlkonstruktion der 21 m weit gespannten Fußgängerbrücke über die Prien so stark korrodiert ist und dass eine Sa-nierung, auch aufgrund der einbetonierten Haupttragelemente in die Widerlager nicht wirt-schaftlich durchzuführen ist. Diese Brücke ist einer der wichtigsten Hauptverkehrswege für Fußgänger und Radfahrer in der Gemeinde und ist mit seiner aktuellen lichten Breite von ca. 1,80 m für einen hochfrequentierten Fußweg nicht mehr zeitgemäß. Bei der vorliegen-den Stahlkonstruktion handelt es sich um zwei Längsträger aus IPE – Profilen, die am Un-tergurt durch einen Längsverband aus Winkelprofilen ausgesteift sind. Die beiden Längs-träger sind schließlich am Widerlager biegesteif eingebunden. 

<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d474.0242073607348!2d12.323151332711353!3d47.7720359900404!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47761522c08e627d%3A0xd3961beed124bacf!2s83229%20Aschau%20im%20Chiemgau!5e0!3m2!1sen!2sde!4v1678525783377!5m2!1sen!2sde" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
 <br />
Lage des Sollingerstegs in Aschau im Chiemgau, visualisiert via Google Maps (2023)<br />


Der Gemeinderat beschloss darauf hin, dass ein Ersatzneubau errichtet werden soll. Das Ingenieurbüro Köppl-Ingenieure Rosenheim wurde beauftragt mögliche Varianten für den Ersatzneubau auszuarbeiten. Die vorgestellten Varianten waren folgende – Stahlbal-kenbrücke, Holzbalkenbrücke, Holzfachwerkbrücke mit Überdachung, Holzbogenbrücke und eine Stahlfachwerkbrücke mit Rundrohrprofilen. Der Gemeinderat beschloss, dass die über-dachte Holzfachwerkbrücke weiter ausgearbeitet werden soll. Dabei gab es den Auftrag des Gemeinderats, trotz der überdachten Variante, eine möglichst filigrane Konstruktion zu entwickeln, die sich gut in die umliegende Bebauung eingliedert und keine unnötige Stör-kontur auf die Umgebung darstellt. Diese Varianten werden in einer weiteren Gemeinde-ratssitzung vorgestellt und diskutiert. Bei den Fachwerkbrücken wurde eine reine Variante in Holz und eine mit Stahlrundstäben als Zugglieder ausgearbeitet. Die Holz- und Stahl-fachwerkbrücke stellt somit den Kompromiss zwischen nachhaltiger- und filigraner Bauwei-se dar und ist im Gegensatz zur reinen Holzvariante weniger massiv. 


# <a name="sec:DesignRepresentation"></a> Design {Representation, Features, and Performances}
This research adopts the propositions of SIA 112 for chosing the bridge design features, which specifies a level of development (LOD) 300 for the task at hand. The design features define the girder height $$h_{girder}$$ and thickness $$t_{girder}$$, the amount $$n_{p}$$ and dimensions $$h_{p}$$ of the piers as well as parameters $$w,i$$ of the NURBS curve for defining the bridge alignment. For the set of performance metrics $$y = \mathcal{P}(\mathbf{x})$$ we employ structural safety and serviceability (resistances, utilisations, internal actions and displacements) criteria next to structural dynamics aspects (eigenfrequencies), costs (computed via the weight and volume) and the boundary conditions for SP, EP and the trees. The structural performance objectives together with the load definitions for the pedestrian bridge (such as loads due to dead weight, pedestrians, wind, snow and temperature) are derived from currently applicable design standards in Switzerland by SIA 261 and 262. 

# <a name="sec:data"></a> Synthetic Data Generation Pipeline and Dataset
The training of the deep latent generative model is collected in a two-stage approach: a central Latin Hypercube Sampling of the design space is launched at first. At second, the sampled design features $$\mathbf{x}$$ are handed to performance simulators to obtain the performance metrics $$\mathcal{P}(\mathbf{x})$$ as defined before, where analytical formoluae as well as the Finite-Element-Analysis software "Sofistik" is utilised. A parametric template for the FEA-based structural analysis was developed and connected to Revit via zero-touch nodes inside Dynamo for the FEA performance simulator to be able to evaluate the vast amounts of parameter samples in a standardised way.

# <a name="sec:MLmodel"></a> Machine Learning Model
The ML model used in this study is a variation of Conditional Variational Autoencoders (CVAE) \cite{cvae_sohn}. In light of having to solve both a forward as well as an inverse problem, we forgo feeding the conditional $$\mathbf{y}$$ to the encoder and instead let it predict the performance metrics together with a latent vector in two separate heads as shown below.

**cVAE Model**<br />
<img src="https://mkrausai.github.io/research/01_SciML/01_BH_PedestrianBridge_XAI/figs/cvae.JPG" width="50%" alt="cVAE_Model" /><br />
 Architecture of our CVAE network acting both as surrogate as well as generative model<br />


# <a name="sec:sensitivity"></a> Explainability through Design Sensitivity Analysis
This research adopts the idea of Sensitivity Analysis (SA), which is well-known in Finite-Element-Analysis by taking the derivative of the performance metrics w.r.t. the design variables Computing these derivatives in established solvers such as the FEM is expensive, while deep learning models, such as the proposed CVAE of this project, deliver these very efficiently through Automatic Differentiation (AD). When inspecting the sensitivity of a performance metric $$\frac{\partial \mathbf{\hat{y}_i}}{\partial \mathbf{x}}$$ for a certain design $$\mathbf{x}$$, the designer receives information in which direction the design variables should be changed in order to improve the particular performance attribute. Furthermore, the distribution of sensitivities over a large set of designs yields information about the network's decision-making. An expert designer with prior knowledge in the design, analysis and construction of bridges can therefore, to a certain extent, estimate the model's reliability based on the relations it found between the features.
%


## <a name="sec:VRDemonstrator"></a> Virtual Reality Demonstrator

Für eine objektive Darstellung der drei Varianten und um alle Unklarheiten im Hinblick auf die umliegende Bebauung zu klären, wurde das Gelände mithilfe eines Laserscans aufge-nommen und die Brückenvarianten wurden dort implementiert. usw….   


Our proposed framework for design subspace learning establishes a new paradigm for performance-conditioned exploration of design spaces, which is neither an optimisation setting nor a random process. Rather, it provides an intuitive and efficient cartography of the vastness of these design spaces. Instead of replacing human intuition with predefined, deterministic, quantitative rules, the AI acts as a design collaborator/co-pilot that augments the human designer's intuition on the problem at hand.

This research provides a variation of CVAEs tailored to forward and inverse design situations. We showed the potential of our CVAE in meta-modelling (i) the forward problem by providing a surrogate to estimate more efficiently and quickly design performances given design features, (ii) compression of complex design spaces into continuous, smooth, low-dimensional design subspaces. With a forward pass through our CVAE being extremely efficient, it can provide performance conditioned designs in quasi real-time and thus augment human designers by providing instant feedback and proposals during the iterative prototyping phase. Furthermore, with analytical derivatives inherently provided in neural networks, we demonstrated that the sensitivity analysis serves as powerful tool for both design optimisation as well as model interpretability. The latter is crucial for building trust and achieving wide acceptance of this kind of design augmentation tools in the AEC domain. The collected user responses prove our framework possesses the potential to find wide application in industry and research as a co-pilot for conceptual design studies in the AEC domain beyond pedestrian bridges.


## <a name="sec:conclusions"></a> Resümee

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

