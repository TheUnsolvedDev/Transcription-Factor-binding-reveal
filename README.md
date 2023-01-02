# Base-resolution models of transcription-factor binding reveal soft motif syntax

## Cell Culture:

## ChIP-nexus, PATCH-CAP, and ChIP-seq experiments:

## Mutation of binding motifs using CRISPR/Cas9 Technology:

## ChIP-nexus data processing pipeline:

## BPNet Architecture:

One-hot encoded sequence for base pairs:

A : [1,0,0,0] Adenine \
C : [0,1,0,0] Cytosine \
G : [0,0,1,0] Guanine \
T : [0,0,0,1] Thymine 

Body of BPNet consists of:

	- Sequence of convolutional layers with skip connections
	- Filter quantity is 64 length of filter is 25 base pairs
	- Filter quantity is 9 dilated convolution

## BPNet Loss function:

Notation:
- $k^{obs}$ vector of length $L$ for a particular strand.
- $p^{pred}$ vector of length $L$ of probabilities with sequence.
- Now, $\Sigma p_i = 1$ and $n^{obs} = \Sigma k^{obs}_{i}$
