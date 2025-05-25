# Autoencoders
Repository for showcasing autoencoder architecture in computer vision and its applications in denoising, domain adaption, anomaly detection and image colorization.

### Basic Implementation
An autoencoder is used to compress an input image using an encoder and then recontruct it using a decoder. The file [Autoencoder_basic.ipynb](./Autoencoder_basic.ipynb) is an implementation for image-to-image reconstruction using tensorflow library. The image [monalisa.jpg](./data/monalisa.jpg) is reconstructed as [monalisa_output.png](./data/monalisa_output.png) after training the autoencoder for 500 epochs.
Below is the comparision: <br> 
| INPUT | RECONSTRUCTED |
|--------|-------|
| <img src="https://github.com/Parth-D3/Autoencoders/blob/main/data/monalisa.jpg" width="250" height = "250"/> | <img src="https://github.com/Parth-D3/Autoencoders/blob/main/data/monalisa_output.png" width="250" height = "250"/> |
<hr>

### Denoising MNIST Dataset
An autoencoder can also be used to denoise images. To do so, the noisy image is fed as input and the original image as the target image while training an autoencoder. In this program, the mnist dataset was loaded using `tensorflow.keras` library. The images were converted to noisy images with a noise_factor = 0.5. The model was trained for 100 epochs. Below is the output: <br>
<img src="https://github.com/Parth-D3/Autoencoders/blob/main/data/autoencoder_mnist.png" />
<hr>
