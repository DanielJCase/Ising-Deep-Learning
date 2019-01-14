# Ising-Deep-Learning
In this repo I explore various deep learning algorithms as applied to the 2-dimensional Ising model. The Ising model can be viewed as a simplistic model of a magnet, inwhich a 2d array of particles with "spin" can orient to point in one of two directions: "up" or "down". At low temperatures the spins of each particle tends to align with the spin of its neighbors, as this is the lower energy state. At high temperature the spin of with particle may be randomly up or down. This model is interesting in physics because it displays a well understood phase transition at a critical temperature. An interesting question in AI is whether models can be developed to learn the phases of physical materials. To explore this questions, a good first step is to apply AI to this model, and see if the phase transition can be identified. 

First, I generate a dataset of Ising model configurations by performing Monte Carlo simulations at various temperatures.
These simulations are performed in ```Ising_genData.ipynb```.

In ```Ising_NN.ipynb```, I explore how a neural net with a single hidden layer, and a convolutional neural net are able to classify the high and low temperature phases of the Ising model. These ideas are based off the paper: J. Carrasquilla, R. Melko, Nat. Phys. (2017).

Next, In ```Ising_GAN.ipynb``` I create a GAN that generates configurations of the Ising model, trainging from the full temperature range sampled in the simulations.

Given that the GAN may generate a configuration corresponding to any temperature, it is more interesting the explore a conditional GAN (cGAN)

In ```Ising_cGAN.ipynb``` I develop a conditional deep convolutional GAN (cDCGAN) that takes as input to the generator and discriminator an embedding of the temperature label. Therefore the GAN can be used to generate configurations for specified temperatures. This model shows promising results but still requires tuning. An upcoming step is to compare the statistical properties 

These notebooks and documentation are an active project and will be updated daily.
