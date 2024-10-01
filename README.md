# Image Generator GAN

This is a Generative Adversarial Network (GAN) model designed to generate images, trained on the FashionMNIST dataset. The GAN consists of two neural networks, a **Generator** and a **Discriminator**, which compete against each other to improve the model's performance. The generator creates images, while the discriminator classifies them as real or fake, pushing both networks to improve over time.

## Table of Contents
- [Overview](#overview)
- [Modules Used](#modules-used)
- [Dataset](#dataset)
- [How It Works](#how-it-works)
- [Training](#training)
- [Results](#results)
- [How to Use](#how-to-use)
- [License](#license)

## Overview
Generative Adversarial Networks (GANs) are a type of deep learning model in which two neural networks, a generator, and a discriminator, contest with each other in a zero-sum game framework. The generator creates data (in this case, images), and the discriminator evaluates the data as either real or fake.

In this project, the GAN model is trained on the **FashionMNIST** dataset, which consists of images of various clothing items like shoes, shirts, and bags. The objective of the model is to train the generator to produce realistic clothing images that the discriminator cannot distinguish from the real images in the dataset.

## Modules Used
- **PyTorch**: The deep learning framework used to build and train the neural networks.
- **NumPy**: Used for handling arrays and mathematical operations.
- **Matplotlib**: Used for plotting and visualizing results.

## Dataset
The **FashionMNIST** dataset is a collection of grayscale images of size 28x28, containing 10 different clothing categories, including T-shirts, shoes, bags, and more. The dataset contains 60,000 training images and 10,000 testing images.

## How It Works

- **Generator**: Takes a random noise vector as input and generates fake images. Its goal is to generate images so realistic that the discriminator is fooled into classifying them as real.
  
- **Discriminator**: Takes both real images (from the FashionMNIST dataset) and fake images (from the generator) as input and classifies them as either real or fake. Its goal is to correctly identify whether the input image is real or generated.

The **objective** of the generator is to generate images that are so realistic that the discriminator cannot distinguish them from real images, while the discriminator tries to improve its accuracy in identifying real vs. fake images. This creates competition, which helps both networks improve.

## Training

The training process consists of alternating between the generator and discriminator:
1. **Train the discriminator**: The discriminator is trained to maximize its ability to correctly classify real and fake images.
2. **Train the generator**: The generator is trained to minimize the discriminator's ability to distinguish between real and fake images.

During each training iteration, the generator tries to fool the discriminator, and the discriminator tries to catch the generator's fakes, leading to better performance for both models.

## Results

After training for a sufficient number of epochs, the generator is able to create images that look very similar to those in the FashionMNIST dataset. The competition between the generator and discriminator ensures that the quality of the generated images improves over time.

### Example Generated Images
![Screenshot from 2024-10-01 23-44-27](https://github.com/user-attachments/assets/301c2ca1-941f-45bd-8999-c890842bc75c)

## How to Use

1. **Clone the repository:**

   ```bash
   git clone https://github.com/your-username/Image-Generator-GAN.git
   ```
2. **Run on Google Colab if possible or it will also run on the device but can consume a lot of CPU computing.**
