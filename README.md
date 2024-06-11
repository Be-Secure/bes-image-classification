# bes-image-classification

## Overview
This image classification model is designed to classify grayscale images of handwritten digits (0-9). The model has been trained using the popular MNIST dataset and can predict the class of an input image, returning a probability distribution over the 10 possible digit classes.

## Model Architecture
The model architecture is a simple Convolutional Neural Network (CNN) designed with the following layers:
1. **Input Layer**: Accepts 28x28 grayscale images.
2. **Convolutional Layer 1**: 32 filters, 3x3 kernel size, ReLU activation.
3. **MaxPooling Layer 1**: 2x2 pool size.
4. **Convolutional Layer 2**: 64 filters, 3x3 kernel size, ReLU activation.
5. **MaxPooling Layer 2**: 2x2 pool size.
6. **Flatten Layer**: Converts the 2D matrix to a 1D vector.
7. **Dense Layer 1**: 128 neurons, ReLU activation.
8. **Output Layer**: 10 neurons (one for each digit), softmax activation.

## Training
The model is trained on the MNIST dataset, which consists of 60,000 training images and 10,000 testing images. Each image is a 28x28 pixel grayscale image of handwritten digits. The training process includes:
1. **Loss Function**: Sparse Categorical Crossentropy
2. **Optimizer**: Adam
3. **Metrics**: Accuracy
4. **Epochs**: 10
5. **Batch Size**: 32

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
   bes-image-classification/                  counterfit/
   ├── bes-image-classification.h5   ------>  ├── targets/
   ├── counterfit/                            │   ├── bes_image_classification.py
   │   ├── bes_image_classification.py  ----> │   ├── bes_image_classification/
   │   ├── bes_image_classification.npz  ---->│       ├── bes-image-classification.h5
                                              │       ├── bes_image_classification.npz

After copying the files, you can use the **bes_image_classification** model with CounterFit DAST as per the tool's usage guidelines.

## Additional Information

For more details on how to configure and run the CounterFit, refer to the [CounterFit documentation](https://github.com/Be-Secure/counterfit).

## License
This project is licensed under the terms of the [Apache-2.0 license](https://github.com/Be-Secure/bes_image_classification/blob/main/LICENSE).
