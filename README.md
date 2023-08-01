# BMI Predictor using Facial Images

This project aims to build a BMI (Body Mass Index) predictor using facial images of individuals. The dataset used is the "iDoc Mugshots" dataset. We are interested in the "front" folder, which contains frontal mugshot images of individuals.

## Dataset

- **Dataset Source**: [iDoc Mugshots Dataset](https://www.kaggle.com/datasets/elliotp/idoc-mugshots)
- **Dataset Description**: The dataset contains mugshot images of individuals, We will be using the "front" folder, which contains frontal mugshot images.
- **Dataset Usage**: Only the images from the "front" folder are used for training and evaluating the BMI predictor model. A new CSV file named "label.csv" is created to provide corresponding labels (BMI values) for each facial image. It is stored in BMI folder.

## Project Structure

```
project_root/
│   README.md
│   bmi_predictor.ipynb
└───bmi/
│   └───front/
│   │   └───front/
│   │   │   │   M47396.jpg
│   │   │   │   ...
│   │   label.csv
│   │   model.tflite

```

- **README.md**: This file, is providing an overview of the project and instructions on usage.
- **bmi_predictor.ipynb**: The main script to execute the training and evaluation of the BMI predictor model.
- **bmi/front/**: A folder that should contain the front folder of mugshot images downloaded from the "front" folder of the iDoc Mugshots dataset. Other folders and csv files are deleted
- **bmi/label.csv**: A CSV file containing the BMI labels corresponding to the images in the "front" folder.
- **bmi/model.tflite**: The trained BMI predictor model in TFLite format.

## Instructions

1. Download the dataset and take only the front folder from the iDoc Mugshots dataset source using the provided link.
2. Create a new folder named "bmi" inside the project root.
3. Inside the "bmi" folder, create a new folder named "front".
4. Place the downloaded "front" folder (containing frontal mugshot images) inside the "bmi/front" folder.
5. Create a new CSV file named "label.csv" inside the "bmi" folder and enter the corresponding BMI labels for each facial image in the "front" folder. The CSV file is uploaded in the BMI folder


6. Ensure that you have the required Python packages installed. You can install them using `pip`, You can add ! to access the terminal inside Jupyter Notebook:

```
!pip install numpy pandas tensorflow opencv-python
```

7. Run the `bmi_predictor.ipynb` script to train the BMI predictor model and generate the TFLite model file.
8. Once the training is complete, you can use the generated `model.tflite` file to make predictions on new facial images.

That's it! You have now successfully trained a BMI predictor model using facial images and can use it to predict BMI values based on new facial images.

