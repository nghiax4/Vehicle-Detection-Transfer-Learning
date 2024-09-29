# Vehicle Detection Transfer Learning
 Using Transfer Learning to predict vehicles

This is a team project for us to learn more about Transfer Learning in Keras. We used Transfer Learning to predict vehicles in images.

## Files
- image_classification_mobilenet_v2.ipynb: This notebook includes steps of loading libraries, dataset, model; adding layers to the original model, training it, and exporting the new model as a file; and running the model on the whole test set and saving the results in a csv file, ready for submission to Kaggle.
- test_run.ipynb: Run the exported file on a few custom images.
- image_classification_mobilenet_v2.h5: The new model created from the original MobileNetV2 with Transfer Learning.
- kagglesubmission.csv: Prediction results by the new model, can be submitted to the Kaggle competition

## Dataset
The dataset we used is from a Kaggle contest: https://www.kaggle.com/c/vehicle. It consists of 7.45gb of images seperated into a train set and a test set, and 17 classes (Ambulance, Boat, Cart, Limousine, Snowmobile, Truck, Barge, Bus, Caterpillar, Motorcycle, Tank, Van, Bicycle, Car, Helicopter, Segway, Taxi).

To make sure "image_classification_mobilenet_v2.ipynb" runs successfully, a dataset folder is needed. You can download the dataset from the Kaggle contest, and split them into the following folder structure:
```bash
kaggle_dataset
    └───vehicle
        ├───test
        │   └───testset
        └───train
            └───train
                ├───Ambulance
                ├───Barge
                ├───Bicycle
                ├───Boat
                ├───Bus
                ├───Car
                ├───Cart
                ├───Caterpillar
                ├───Helicopter
                ├───Limousine
                ├───Motorcycle
                ├───Segway
                ├───Snowmobile
                ├───Tank
                ├───Taxi
                ├───Truck
                └───Van
```
, where the "testset" folder is the test set, and "train" is the train set.

(This is equivalent to unzipping the downloaded dataset file from Kaggle to a new folder called "kaggle_dataset")

Make sure the "kaggle_dataset" folder is in the same folder as "image_classification_mobilenet_v2.ipynb".

## Model
We loaded the MobileNetV2 model given in Keras, froze its parameters, and added a few layers to make it output the final probabilities in 17 nodes, corresponding to 17 classes. The specific additions can be found in the file "image_classification_mobilenet_v2.ipynb".

## Accuracy
After running the model through each image in the test set and submitting to Kaggle, we got 80% accuracy.
![image](https://github.com/user-attachments/assets/aab26162-7507-49d3-976d-1ae02ff4eef8)

## Credits
- Guide to Transfer Learning with Keras: https://keras.io/guides/transfer_learning/
- Kaggle's vehicle classification contest: https://www.kaggle.com/c/vehicle
- Project was forked from https://github.com/trekhleb/machine-learning-experiments/blob/master/experiments/image_classification_mobilenet_v2/image_classification_mobilenet_v2.ipynb
- Teammates: Bui Quoc Minh Nhat, Nguyen Pham Quoc An
