# **Information-Geometric Hyperscanning for Inter-Brain Networks**

<p align="center">
<img src="brainhack_figure.png" alt="Information-Geometric Hyperscanning Network Circular Graph" width="250">
</p>

## **BrainHack Warsaw 2026**  
Welcome to the HyPhi(Φ) project repository for BrainHack Warsaw\!  
HyPhi(Φ) is a scalable hyperscanning analysis pipeline that characterizes inter-brain coupling using discrete Ricci curvature and curvature entropy. Instead of treating inter-brain synchrony as a scalar quantity, we model time-resolved inter-brain networks as evolving geometric objects.

**Project coordinators** 
Nicolás Hinrichs
Nahid Torbati

**Contributors**  
Kacper Łyczak
Vinayak M. Kulkarni
Katarzyna Libera
Pola Kukiełka
Hanna Święcicka
Marta Lotka
Sylwia Adamus
Zuzanna Maruszewska

## **🗺️ Conceptual Map & Pipeline**

Our analysis workflow bridges established hyperscanning ecosystems with novel geometric measures. The pipeline follows these core steps:

1. [**HyPyP**](https://github.com/GHFC/HyPyP) Preprocess data and extract **adjacency matrices**.  
2. [**NetworkX**](https://networkx.org/) Construct **weighted connectivity** graphs from the matrices.  
3. [**HyPhi**](https://github.com/nicolashinrichs/HyPhi) Conduct **curvature analyses** on the resulting networks.

Mattermost handle:
[https://minervamessenger.mpdl.mpg.de/neural-ds-lab/channels/hyphi](https://minervamessenger.mpdl.mpg.de/neural-ds-lab/channels/hyphi)

## **🗓️ BrainHack Warsaw Schedule**

### **Day 1 (19:30 \- 22:00)**

**Focus:** Project kickoff and data preparation.

* **Who:** All participants  
* **Tasks:**  
  * How to organize and structure our work.  
  * Grant collaborator access to the main HyPhi repository.
  * Create dedicated branches for each team/feature.

### **Day 2**

**Focus:** Core analysis, geometric metrics, and statistical modeling.

* **Who:** Everyone
  * Preprocess the dataset using the HyPyP pipeline.
  * Create initial connectivity matrices using NetworkX.
 
* **Teams & Tasks:**  
  * **Team Red:** Focus on *Spectral Graph Analyses*.  
  * **Team Blue:** Focus on *Entropy* and/or *Wasserstein distance* (heat diffusion probabilities vs. random walking) and/or *Statistical Analyses*.  
  * **Team leaders:** Project coordination/guidance, core pipeline integration, and Flow module.

### **Day 3 (09:00 \- 13:00)**

**Focus:** Wrap-up, documentation, and interpretation.

* **Who:** Everyone  
* **Tasks:**  
  * Repository setup, code commenting, and finalizing README files.  
  * Adding interpretations and conceptual explanations to the findings.

## **🚀 Possible Contributions & Future Directions**

We welcome contributions from coders and non-coders alike\! Potential areas for contribution during the Hackathon and beyond include:

* **Spectral Graph Analyses:** Deeper dives into the spectral properties of inter-brain networks.  
* **Advanced Metrics:** Implementing Wasserstein distance from heat diffusion probabilities vs. random walking.  
* **Tooling:** Developing a Graphic User Interface (GUI) with straightforward options for modality, task, and measure selection.  
* **Conceptualization:** Modeling and interpreting existing synchrony metrics against our geometric ones.

## **🤝 Collaboration & Outputs**

* Code commenting, finalizing README files, and submitting Pull Requests from our dedicated branches.
* Drafting a structural outline for our joint publication to organize our asynchronous work after the event.
* Adding interpretations and conceptual explanations to the findings.
* **Other project participants?** We are actively looking for cognitive neuroscientists, physicists/applied mathematicians, and science visualization specialists to join the effort.


## **📚 Literature**

1. https://www.frontiersin.org/journals/aging-neuroscience/articles/10.3389/fnagi.2023.1120846/full
2. https://www.nature.com/articles/s41598-018-27001-3
3. https://www.nature.com/articles/s41598-020-67474-9
4. https://www.nature.com/articles/s41598-019-46380-9
5. https://www.sciencedirect.com/science/article/abs/pii/S0378437122005179
6. https://math.oit.edu/~hammondd/publications/hammond_gur_johnson_ieee_globalsip_2013.pdf
