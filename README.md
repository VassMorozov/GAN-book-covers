# Exploring Generative Adversarial Networks (GAN)

A GAN is a deep learning framework that can be used to generate images or text. It consists of two competing models: a generator and a discriminator. The discriminator aims to classify whether an output is real or not while the generator aims to create an output that can trick the discriminator into believing the output is real. These models are trained in parallel with each iteration resulting in better predictions and generated outputs. The end result is a generator capable of producing realistic outputs.

For this project, a GAN framework is explored to generate images. Specifically, these images are children's book covers. The source data can be found using the following link:

https://www.kaggle.com/datasets/thomaskonstantin/6000-children-and-teen-book-covers

The project is divided into the following high level tasks:

* Image visualisation and cleaning
* Development of bespoke GAN
* Exploration of GAN with pre-trained discriminator

Visualising the image revealed that the majority of them have large text on the cover. I did not set out to build a text and image generator and wanted to focus on the images. The presence of text will only create noise in the GAN. As such, the first task involved using a pre-trained text extractor from Keras to remove the text from each book cover. An example of the result can be seen below:

![image](https://github.com/VassMorozov/GAN_book_covers/assets/28609388/aacc0fa4-b0e5-4a00-8311-fb1f466c6955)

Training a bespoke GAN proved tricky (and exceptionally computationaly expensive even with Google Colab GPUs!). I explored several architectures with improving results each time as I built both the generator and discriminator up, however did not find the training balance required for a GAN with the computational resources I had available. 

As a last effort to try and get some meaningful results, I tried to use my existing best generator combined with a pre-trained image classification model (VG16 from Keras: https://arxiv.org/abs/1409.1556). I was not sure this would work given the balance that needs to be struck between generator and discriminator in training, and using a base discriminator that was incredibly strong may not work. However the generator using a pre-trained discriminator yielded results that resembled some sort of character / animal that could arguably be a book cover!

![image](https://github.com/VassMorozov/GAN_book_covers/assets/28609388/3ebdb30d-1d21-489e-8bff-29d7455b10a2)

This was an output after 350 epochs of training, so with additional fine-tuning of the architecture and training hyperparameters, the results can be improved further.


