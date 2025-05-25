# Autoencoders
Repository for showcasing autoencoder architecture in computer vision and its applications in denoising, domain adaption, anomaly detection and image colorization.

### Basic Implementation
An autoencoder is used to compress an input image using an encoder and then recontruct it using a decoder. The file `Autoencoder_basic.ipynb` is an implementation for image-to-image reconstruction using tensorflow library. The image `monalisa.jpg` is reconstructed as `monalisa_output.png` after training the autoencoder for 500 epochs.
Below is the comparision: <br> 
| INPUT | RECONSTRUCTED |
|--------|-------|
| <img src="https://example.com/image1.png" width="200"/> | <img src="https://example.com/image2.png" width="200"/> |
