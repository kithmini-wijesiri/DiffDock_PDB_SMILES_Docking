**DiffDock Overview**

DiffDock is a diffusion generative model for drug discovery in molecular blind docking. DiffDock consists of two models: the **Score** and **Confidence models**.
The Score model is a 3-dimensional equivariant graph neural network that has three layers: embedding, interaction layer with 6 graph convolution layers, and output layer.It is used to generate a series of potential poses for protein-ligand binding by running the reverse diffusion process.

The **Confidence model** has a similar architecture as the Score model but with 5 graph convolution layers in the interaction layer. It is used to rank the generated ligand poses from the Score model. 

*Model Architecture* 
Architecture Type: Score-Based Diffusion Model (SBDM)
Network Architecture: Graph Convolution Neural Network (GCNN)

Input Type(s): Text (PDB, SDF, MOL2, SMILES)
Input Format(s): Protein Data Bank (PDB) Structure files for proteins, Structural Data Files (SDF), Tripos molecule structure format (MOL2) Structure files and Simplified molecular-input line-entry system (SMILES) strings for ligands
Other Properties Related to Input: Pre-Processing Needed

*Ref:  Corso, Gabriele, Hannes Stärk, Bowen Jing, Regina Barzilay, and Tommi Jaakkola. “Diffdock: Diffusion steps, twists, and turns for molecular docking.” arXiv preprint arXiv:2210.01776 (2022)*
