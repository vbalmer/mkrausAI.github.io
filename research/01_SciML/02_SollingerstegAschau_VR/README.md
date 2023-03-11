<!--https://mkrausai.github.io/research/01_SciML/01_BH_PedestrianBridge_XAI/-->
<script src='https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.4/MathJax.js?config=default'></script>


# Virtual Reality (VR) Explainable AI for Conceptual Generative Design of a Pedestrian Bridge

<!-- A repository of structural information on the design of pedestrian bridges
============================== -->

*   [Motivation und Hintergrund](#description)
*   [Projektübersicht](#objectives)
*   [Schlussfolgerungen](#content)
*   [Beteiligte](#contributors)

<!-- -->
<!-- *   [Citation](#citation)-->

## <a name="description"></a>Project Description

Das Potenzial von Augmented Reality (AR) für den Hoch- und Ingenieurbau ist groß, jedoch bleiben derzeitige Anwendungen in der Praxis eher Prototypen. Gerade die konzeptionelle Entwurfsphase eines Bauprojektes bedingt die Einbindung der Interessen und Bedürfnisse diverser beteiligter Personen und Gruppen, für welche die technische Sprache der Planenden sowie die Form der Entwurfskommunikation in Planabstraktionen, statischen Modellen oder Prinzipskizzen eine Verständnishürde darstellt. Dabei ist aber das Erzielen einer Paretooptimalität aufgrund des gegenseitigen Verständnisses in dieser ersten Phase eines Bauwerks essenziell um die spätere Akzeptanz und Zufriedenheit in der Breite der betroffenen und beteiligten Personen zu garantieren. Bei öffentlichen Bauprojekten steht dabei die frühzeitige Demokratisierung der Entscheidungsfindung über diverse Formen der Bürgerinformation und -beteiligung immer stärker im Fokus. Daher hat sich im Rahmen dieses Projekts ein Team aus Bauherrenschaft, Planung und Forschung zusammengeschlossen, um die technischen und organisatorischen Herausforderungen dafür zu erarbeiten und eine effiziente und ansprechende Lösung mithilfe von Virtual Reality (VR) zu entwickeln.

<img src="https://mkrausai.github.io/research/01_SciML/02_SollingerstegAschau_VR/figs/Snapshot.PNG" width="50%" alt="Snap_1" /><br />
[![Totalansicht im VR Modell "Sollingersteg Variante 2"](https://youtu.be/g3Hgu1M1gj8/0.jpg)](https://www.youtube.com/watch?v=qbr8kGF8zXU&t=1s "VR Rundgang mit den drei Brückenvarianten des "Sollingersteg Aschau im Chiemgau"")



Diese Forschungsarbeit bietet einen leistungsgesteuerten Rahmen für die Designexploration, um den menschlichen Designer durch eine Variante des Conditional Variational Autoencoders (CVAE) zu unterstützen, der sowohl als Vorwärts-Performance-Prädiktor für gegebene Design-Merkmale (Vorwärts-Designprozess) als auch als Prädiktor für Design-Merkmale unter Berücksichtigung einer Reihe von Leistungsanforderungen (Invers-Designprozess) dient. Das CVAE wird auf synthetisch generierten Leistungsdaten für den Entwurf einer Fußgängerbrücke "Brücke über den Graben" in St. Gallen in der Schweiz trainiert. Um die Interpretierbarkeit des Modells zu verbessern, machen wir von der Sensitivitätsanalyse Gebrauch und zeigen, dass das Modell nicht nur Einblicke in die Beziehungen zwischen den Merkmalen gibt, sondern auch als Hilfsmittel dient, um den Konstrukteuren Hinweise zu geben, wie sie die Konstruktionen im Hinblick auf bestimmte vordefinierte Ziele verbessern können. Eine Nutzerstudie hat gezeigt, dass unser Rahmenwerk intuitiv, zuverlässig und sehr genau ist und das Potenzial hat, als Co-Pilot für konzeptionelle Designstudien im AEC-Bereich über Fußgängerbrücken hinaus zu dienen.



## <a name="objectives"></a>Objectives
The objective of this research is to 
*   develop a synthetic dataset generation pipeline for quantifyable (structural) design performances
*   implement, train and evaluate a suitable design meta-model for the forward and inverse design setting
*   create a demonstrator application of an explainable and intuitive co-pilot for conceptual design. 

We demonstrate the applicability of this approach in the forward as well as inverse design setting for the generic example of a bridge st engineers or project managers with limited expertise in ML or AI and fosters wide-spread use of such tools in practice.


## <a name="content"></a> Project Details
The pedestrian bridge "Brücke über den Graben" provides a pedestrian crossing from an exit of a building next to a parking garage (start point / SP), over a busy cantonal street and then through the St. Mangen park, to terminate next to a church (end point / EP). The currently existing surroundings of the bridge project as well as the corresponding coordinate system is given as a scanned point cloud within a BIM model in Autodesk Revit, cf. the videos below. 

**Project site**<br />
<img src="https://mkrausai.github.io/research/01_SciML/01_BH_PedestrianBridge_XAI/figs/ProjectSite.png" width="30%" alt="project_site" /><br />
 M 1:750, Basler&Hoffmann 2022<br />

<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d474.0242073607348!2d12.323151332711353!3d47.7720359900404!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47761522c08e627d%3A0xd3961beed124bacf!2s83229%20Aschau%20im%20Chiemgau!5e0!3m2!1sen!2sde!4v1678525783377!5m2!1sen!2sde" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe> <br />
 M 1:750, Basler&Hoffmann 2022<br />



This study develops AI-based meta models for both design situations, forward and inverse design setting, together with respective interaction interfaces, which are described below.


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

## <a name="sec:Results"></a> Results and Discussion
We sampled 18'000 instances of the pedestrian bridges together with their performances within the generative design as described before to form the dataset for subsequent CVAE training. While the Latin-Hypercube-Sampling of the Design space was conducted in a few seconds, obtaining performances of a batch of 600 design instances via FEA took on average around 55 minutes.

Below we show the prototype of a user interface for the inverse design situation developed within Revit Dynamo. It provides the user with sliders and check-boxes, allowing to set desired performance metrics such as ranges for costs or the maximum structural utilisation in the ultimate as well as serviceability limit state. More fine grained requests for different objectives, as well as an additional visualisation of the latent space and the mapping of the objectives, is also possible, yet has been omitted for the sake of clearness. The right hand side of the user interface displays the sensitivity plots as well as a scatter plot for finding the Pareto front. Finally, a rendering of the generated bridge is shown, which can be inspected either on the screen in 2D, or in 3D through virtual reality on smartphones or dedicated devices.

We demonstrated our developments to a selected group of researchers and practitioners (15 persons) within a hands-on session. The collected feedback towards ergonomics, efficiency and quality prove our framework to be intuitive, efficient, reliable and to bear a great potential for applications in practice.

<img src="https://mkrausai.github.io/research/01_SciML/01_BH_PedestrianBridge_XAI/figs/XAI_Overview.PNG" width="80%" alt="XAI_Overview" /><br />
[![Explainable AI Interface for Forward and Inverse Pedestrian Bridge Design](https://youtu.be/6pVvFye_5ko/0.jpg)](https://youtu.be/GbXYkEoFv9Q "Explainable AI Interface for Forward and Inverse Pedestrian Bridge Design")

## <a name="sec:Conclusions"></a> Conclusions
Our proposed framework for design subspace learning establishes a new paradigm for performance-conditioned exploration of design spaces, which is neither an optimisation setting nor a random process. Rather, it provides an intuitive and efficient cartography of the vastness of these design spaces. Instead of replacing human intuition with predefined, deterministic, quantitative rules, the AI acts as a design collaborator/co-pilot that augments the human designer's intuition on the problem at hand.

This research provides a variation of CVAEs tailored to forward and inverse design situations. We showed the potential of our CVAE in meta-modelling (i) the forward problem by providing a surrogate to estimate more efficiently and quickly design performances given design features, (ii) compression of complex design spaces into continuous, smooth, low-dimensional design subspaces. With a forward pass through our CVAE being extremely efficient, it can provide performance conditioned designs in quasi real-time and thus augment human designers by providing instant feedback and proposals during the iterative prototyping phase. Furthermore, with analytical derivatives inherently provided in neural networks, we demonstrated that the sensitivity analysis serves as powerful tool for both design optimisation as well as model interpretability. The latter is crucial for building trust and achieving wide acceptance of this kind of design augmentation tools in the AEC domain. The collected user responses prove our framework possesses the potential to find wide application in industry and research as a co-pilot for conceptual design studies in the AEC domain beyond pedestrian bridges.



<img src="https://mkrausai.github.io/research/01_SciML/02_SollingerstegAschau_VR/figs/koeppl_portrait.jpg" width="20%" alt="Johannes" /><br />
**M.Eng. Johannes Köppl**<br />
Prokurist und Gesellschafter der Köppl Ingenieure GmbH Rosenheim <br />

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

