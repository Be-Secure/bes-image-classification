# bes-image-classification

## Overview
This image classification model is designed to classify grayscale images of handwritten digits (0-9). The model has been trained using the popular MNIST dataset and can predict the class of an input image, returning a probability distribution over the 10 possible digit classes.

## Model Architecture
The model architecture is a simple Convolutional Neural Network (CNN) designed with the following layers:
* **Input Layer:** 28x28 grayscale images
* **Convolutional Layers:** Two layers with 32 and 64 filters, respectively, using ReLU activation
* **MaxPooling Layers:** Two layers with 2x2 pool size
* **Dense Layer:** 128 neurons with ReLU activation
* **Output Layer:** 10 neurons (one for each digit) with softmax activation


## Training
The model is trained on the MNIST dataset, which consists of 60,000 training images and 10,000 testing images. Each image is a 28x28 pixel grayscale image of handwritten digits. The training process includes:
* **Loss Function**: Sparse Categorical Crossentropy
* **Optimizer**: Adam
* **Metrics**: Accuracy


## Security Assessments
Be-Secure has conducted security assessments on this model using CounterFit and AIShield. Below are the detailed steps to perform these assessments.

### CounterFit Assessment
1. **Prepare the CounterFit Tool**
Start the CounterFit tool by following the setup instructions provided in its [documentation](https://github.com/Be-Secure/counterfit). Once the tool is running, execute the following command within CounterFit to create the necessary environment for the **bes-image-classification** model:
   ```sh
   new -n bes_image_classification -d image

2. **Clone bes-image-classification**
Clone the current repository to your local machine using the following command:
   ```sh
   git clone https://github.com/Be-Secure/bes_image_classification.git
   
3. **Copy Files to CounterFit tool**

   Inside the cloned `bes-image-classification` repository, navigate to the `counterfit` folder and copy `bes_image_classification.py`. Paste it inside the `targets` folder of the CounterFit tool where it is running.
   Additionally, from the cloned `bes-image-classification` repository, copy the `bes-image-classification.h5` file. Then, from the `bes-image-classification/counterfit` folder, copy the `bes_image_classification.npz` file. Paste both files into the `targets/bes_image_classification` folder of the CounterFit tool from where CounterFit is running.

   ```sh
   bes-image-classification/                           counterfit/
   ├── bes-image-classification.h5 ------------------>  ├── counterfit/
   ├── counterfit/                                      │   ├── targets/
   │   ├── bes_image_classification.py  ------------->  │       ├── bes_image_classification.py
   │   └── bes_image_classification.npz  ------------>  │       ├── bes_image_classification/
   │                                                    │           ├── bes-image-classification.h5
   │                                                    │           └── bes_image_classification.npz
   ```

After copying the files, you can use the **bes-image-classification** model with CounterFit DAST as per the tool's usage guidelines.
For more details on how to configure and run the CounterFit, refer to the [CounterFit documentation](https://github.com/Be-Secure/counterfit).

## License
This project is licensed under the terms of the [Apache-2.0 license](https://github.com/Be-Secure/bes_image_classification/blob/main/LICENSE).
