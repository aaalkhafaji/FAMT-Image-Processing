# FAMT-Image-Processing
Python implementation of the Framed Algebraic-Morphological Transform (FAMT) for structure-preserving image denoising.
# Framed Algebraic-Morphological Transform (FAMT)

This repository contains a Python implementation of the **Framed Algebraic-Morphological Transform (FAMT)**, a novel, fully invertible image processing transform derived from combinatorial Hopf algebras. 

Unlike the Fast Fourier Transform (FFT) which relies on global sinusoidal harmonics and suffers from the Gibbs phenomenon, the FAMT projects image data onto a graded basis of localized topological primitives. 

## Theoretical Mapping
This code serves as the computational implementation of the theoretical framework developed in our research:
1. **Forward Transform (`forward_transform`):** Implements the subset-splitting coproduct $\Delta$. It decomposes the image into distinct topological features using the $0$-th Betti number (connected components).
2. **Spectral Filtering (`apply_filter`):** Implements the dual filter $\Phi \in \mathcal{H}^*$. It annihilates noise by filtering tensor components based on their topological rank (cardinality) while perfectly preserving their spatial phase.
3. **Inverse Transform (`inverse_transform`):** Implements the exact combinatorial inversion via the Hopf antipode $S$. It reconstructs the spatial boundaries exactly, ensuring zero ringing artifacts or boundary discontinuities.

## Usage
Ensure you have `opencv-python`, `numpy`, and `matplotlib` installed. 

```bash
pip install opencv-python numpy matplotlib
