# Cas9_Files
This repo contains the data from: 
EVCouplings, 
DynaMut2, 
MDM-TASK,
MD simulation.

# MD Simulation:
**For PBC correction (1 Protein and 0 System)**

echo 1, 0 |gmx trjconv -s md.tpr -f md.xtc -o md_corr.xtc -center -ur compact -pbc mol


****Visualization in VMD****

**PBC Correction:**

vmd step3_input.psf md_corr.xtc

**Protein Alignment:**

VMD Main > Extension > Analysis > RMSD Trajectory Tool > Align (using protein) > RMSD

VMD Main > Graphics > Representations > index 0 to 26513 (in Selection Atoms Panel) > Enter

**Save Protein-Nucleic Acid Complex in .dcd format:**

VMD Main > File > Save Coordinates > Selected Atoms: index 0 to 26513 > File Type: dcd > Save > Protein_NA_complex.dcd

VMD Main > File > Save Coordinates > Selected Atoms: index 0 to 26513 > File Type: pdb > Frames: First 0, Last 0, Stride, 1 > Save > Protein_NA_complex.pdb

**Visualizing Protein-Nucleic Acid Complex:**

vmd Protein_NA_complex.pdb Protein_NA_complex.dcd


