# Image Super-Resolution using Efficient Sub-Pixel CNN (ESPCN)

This project implements image super-resolution using the Efficient Sub-Pixel Convolutional Neural Network (ESPCN).

## Overview

Super-resolution (SR) is the process of recovering high-resolution (HR) images from their low-resolution (LR) counterparts.

* High-resolution images offer a higher pixel density, providing more detail about the original scene.
* The need for higher resolution is common in computer vision applications to enhance performance in tasks like pattern recognition and image analysis.
* Super-resolution has numerous real-world applications.
* In recent years, deep neural network-based models have achieved significant success in both computational performance and the accuracy of reconstructed super-resolution images.

**NOTE:** This project specifically utilizes the **Efficient Sub-Pixel Convolutional Neural Network (ESPCN)**

## Understanding Sub-pixels

In digital imaging systems, captured image data is discretized. Due to sensor limitations, images have a native pixel resolution, where each pixel represents a small area of color from the real world. While we see pixels connected side-by-side in a digital image, at a microscopic level, there exist numerous "tiny pixels" between these physical pixels. These are referred to as **sub-pixels**. ESPCN leverages operations at the sub-pixel level for efficient upscaling.

## Algorithm: ESPCN

The process flow using the ESPCN model is as follows:

1.  **Input:** A low-resolution (LR) image.
2.  **Data Preprocessing:**
    * Normalizing pixel values
    * cropping and resizing the image as needed for the network input.
3.  **Efficient Sub-Pixel CNN (ESPCN)**
   - Several convolutional layers (`Conv2D`) are used:
     - Conv2D
     - Conv2D
     - Conv2D
     - Conv2D
   - Activation layers:
     - Tanh activation layer
     - Sigmoid activation layer
4.  **Output:** The reconstructed high-resolution (HR) image.

## Loss Function

To train the network, we need to measure the difference between the generated super-resolution (SR) image and the original high-resolution (HR) image (ground truth). The **Mean Squared Error (MSE)** is commonly used for this purpose.

## Peak Signal-to-Noise Ratio (PSNR)
PSNR is the primary metric used to evaluate super-resolution performance:

- Measures the signal-to-noise ratio between two images.
- Compares the original high-resolution image with the predicted reconstructed image.
- Higher PSNR values indicate better image quality.
- Achieved a PSNR of 31 dB
