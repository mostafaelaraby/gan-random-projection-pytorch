# GAN Random Projection
In this repo an implementation of DCGAN and comparing its results when we use a single discriminator versus using a set of discriminator each one of them on a different projection of the data.

We use random filters fixed throughout the training, these filters are then applied to input images from the data distribution or data generated by the generator. These random projection are then sent to a set of discriminators each working on a specific filter.

The notebook is commented and contains already generated images. 


## Motivation
In GANs, non saturating discriminators can provide meaningful gradients to the generator.
Meaningful gradients will let us continue the adversarial training longer without having the discriminator beat the generator
We will get different gradients from each discriminator, each gradient will be in a different lower dimensional space depending on our initial filter which will help the training avoid mode collapse.

## References
<a id="1">[1]</a> 
Neyshabur, Behnam, Srinadh Bhojanapalli, and Ayan Chakrabarti.
"Stabilizing GAN training with multiple random projections." arXiv preprint arXiv:1705.07831 (2017).
