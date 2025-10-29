# Sars-Cov2 Deep Mutational Modelling

This repo builds on the work done in https://pmc.ncbi.nlm.nih.gov/articles/PMC9428596/. Here the RBD of Sars-Cov2 was mutated and the the resulting proteins were screened for ACE2 and antibody binding. Their data contains a list of amino acid sequences and then if the resulting proteins could bind (binary value). 

Here we attempt to develop a model that can predict ACE2 binding and immune escape of new amino acid mutations. We attempt to add structural information into the model. 

First we test the performance of AlphaFold3 and AlphaFold multimer for ACE2-RBD interaction and structure prediction using known PDB structures. We do the same for the antibodies used in the paper. This also allows us to identify epitopes of known antibodies. 

AlphaFold3 additionally lets users specify `bondedAtomPairs` - we can supply the model with the list of known epitope binding sites and assess if this improves docking and structure prediction.
