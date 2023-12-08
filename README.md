# Exploring Generative Adversarial Networks (GAN)

A GAN is a deep learning framework that can be used to generate images or text. It consists of two competing models: a generator and a discriminator. The discriminator aims to classify whether an output is real or not while the generator aims to create an output that can trick the discriminator into believing the output is real. These models are trained in parallel with each iteration resulting in better predictions and generated outputs. The end result is a generator capable of producing realistic outputs.

For this project, a GAN framework is explored to generate images. Specifically, these images are children's book covers. The source data can be found using the following link:

https://www.kaggle.com/datasets/thomaskonstantin/6000-children-and-teen-book-covers

The project is divided into the following high level tasks:

* Image visualisation and cleaning
* Development of bespoke GAN
* Exploration of GAN with pre-trained discriminator

Training a GAN proved tricky (and exceptionally computationaly expensive!), however the generator using a pre-trained discriminator yielded results that resembled some sort of character / animal.
![image](https://github.com/VassMorozov/GAN_book_covers/assets/28609388/3ebdb30d-1d21-489e-8bff-29d7455b10a2)

This was an output after 350 epochs of training, so with additional fine-tuning of the architecture and training hyperparameters, the results can be improved further.


