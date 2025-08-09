In this project, we implemented a Conditional Variational Autoencoder (CVAE) for MNIST digit generation and demonstrated machine unlearning.
The model learns structured representations of digits by:
- Conditional encoding: Mapping input images and class labels to latent distributions
- Stochastic sampling: Using reparameterization trick to generate latent vectors
- Class-conditional decoding: Reconstructing images from latent vectors and target labels

After training for 200 epochs on MNIST, we analyzed the latent space geometry by computing class-specific mean vectors and covariance matrices, and quantifying each digit's spread via determinant of covariance.
For unlearning, we developed the method used in [Selective Amnesia: A Continual Learning Approach for Forgetting in Deep Generative Models](https://arxiv.org/abs/2305.13990) paper.

The unlearning process after 10000 steps successfully removed knowledge of the target digit (in our case, digit 5) while maintaining reconstruction quality for other classes.
