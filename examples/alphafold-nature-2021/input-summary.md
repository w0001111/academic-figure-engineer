# Input Summary

AlphaFold predicts protein structure from an amino acid sequence using evolutionary and structural information.

Publicly described high-level components include:

- amino acid sequence input;
- multiple sequence alignment (MSA) information;
- structural template information when available;
- learned sequence/MSA and pair representations;
- Evoformer representation learning with information exchange between MSA and pair representations;
- recycling / iterative refinement of representations and structure;
- a structure module that predicts 3D atomic coordinates;
- confidence estimates such as predicted local distance difference test and aligned error measures.

The central contribution represented in this example is an end-to-end architecture that reasons over sequence, evolutionary, template, and pairwise geometric information to generate accurate protein structures.

This summary is intentionally high-level. It does not reproduce the original Nature figure layout or styling.
