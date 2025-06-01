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
An autoencoder can also be used to denoise images. To do so, the noisy image is fed as input and the original image as the target image while training an autoencoder. In this program, the mnist dataset was loaded using `tensorflow.keras` library. The images were converted to noisy images with a noise_factor = 0.5. The model was trained for 100 epochs. Find the program  [Autoencoder_denoising_mnist.ipynb](./Autoencoder_denoising_mnist.ipynb). file Below is the output: <br>
<img src="https://github.com/Parth-D3/Autoencoders/blob/main/data/autoencoder_mnist.png" />
<hr>

### Anomaly Detection
Dataset: [https://data.lhncbc.nlm.nih.gov/public/Malaria/cell_images.zip](https://data.lhncbc.nlm.nih.gov/public/Malaria/cell_images.zip)  <br>
An autoencoder can also detect anomalies in all types of data. The model is trained with 'normal' or 'non-anomaly' images. Learning takes place and the autoencoder is able to reconsturct the same type of images as that of training ones. If any other image with major changes is presented to the model, it is not able to recreate it accurately. Thus, the error for the anomalous image is higher than a set threshold and thus image is flagged as anomaly. Find the program in [Autoencoder_anomaly_Detection.ipynb](./Autoencoder_anomaly_Detection.ipynb).<br>
The given dataset contains the following two types of images. The model was trained on around 16 out of 100 epochs due to early stopping. Mean Squared error was used to measure the difference between the input image and the reconstructed image. 
<img src="https://github.com/Parth-D3/Autoencoders/blob/main/data/malaria.png" />
<hr>

### Image Colorisation
An autoencoder can also be utilized to convert gray scale images to colored images through image colorisation. Colored images (RGB) and their grayscale equivalents are provided as X,Y during training. New unseen grayscale images similar to those used in training can then be fed to the autoencoder model to get RGB conversion. For the demonstration purposes, 60 random images were used which can be found in [data/images](./data/images). The model was initially trained on 300 epochs and retrained for an additional 300 epochs. due to no improvement in validation accuracy, the training was concluded. Find the program files here [Autoencoder_image_colorisation](./Autoencoder_image_colorisation.ipynb).
