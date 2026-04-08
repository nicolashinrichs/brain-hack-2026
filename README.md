# **Information-Geometric Hyperscanning for Inter-Brain Networks**

**@ BrainHack Warsaw**  
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
  * Preprocess the dataset using the HyPyP pipeline.  
  * Create initial connectivity matrices using NetworkX.

### **Day 2**

**Focus:** Core analysis, geometric metrics, and statistical modeling.

* **Who:** Sub-teams  
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

* **Branching:** Please create a branch in the HyPhi repo for your specific features or analyses, and submit Pull Requests to the main branch.  
* **Publications:** We are aiming to turn the new toolkit modules and our findings into a **joint publication**. All active participants who meaningfully contribute will be included\!  
* **Other project participants?** We are actively looking for cognitive neuroscientists, physicists/applied mathematicians, and science visualization specialists to join the effort.

## **📋 Pre-Hackathon To-Do List (Maintainers)**

* \[ \] Prepare the dataset.  
* \[ \] Prepare a project one-pager for distribution.  
* \[ \] Finalize the conceptual map visual.
