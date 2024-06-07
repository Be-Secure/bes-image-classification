# bes_image_classification

This repository contains the **bes_image_classification** model and target file which can be used with the CounterFit tool for Dynamic Application Security Testing (DAST).

## Usage Instructions

Follow these steps to use the bes_image_classification model with CounterFit:

1. **Clone the Repository**

   Clone the current repository to your local machine using the following command:
   ```sh
   git clone https://github.com/Be-Secure/bes_image_classification.git

2. **Prepare the CounterFit Tool**

   Start the **CounterFit** by following the setup instructions provided in its [documentation](https://github.com/Be-Secure/counterfit). Once the tool is running, execute the following command within CounterFit to create the necessary environment for the **bes_image_classification** model:
   ```sh
   new -n bes_image_classification -d image

4. **Copy Files to CounterFit**
   
    Navigate to the `bes_image_classification/counterfit` folder inside the cloned repository and copy all its contents. This folder includes another `bes_image_classification` folder and a `bes_image_classification.py file`. You need to paste these contents into the `targets` folder of the CounterFit tool where it is running, replacing the existing `bes_image_classification.py` file. The typical path for the `targets` folder in CounterFit is `counterfit/counterfit/targets`.

After copying the files, you can use the **bes_image_classification** model with CounterFit DAST as per the tool's usage guidelines.

## Additional Information

For more details on how to configure and run the CounterFit, refer to the [CounterFit documentation](https://github.com/Be-Secure/counterfit).

## License
This project is licensed under the terms of the [Apache-2.0 license](https://github.com/Be-Secure/bes_image_classification/blob/main/LICENSE).
