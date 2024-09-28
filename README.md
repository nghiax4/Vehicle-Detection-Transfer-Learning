# Vehicle Detection Transfer Learning
 Using Transfer Learning to predict vehicles

This is a team project for us to learn more about Transfer Learning in Keras. We used Transfer Learning to predict vehicles in images.

## Dataset
The dataset we used is from a Kaggle competition: https://www.kaggle.com/c/vehicle. It consists of 7.45gb of images seperated into a train set and a test set, and 17 classes (Ambulance, Boat, Cart, Limousine, Snowmobile, Truck, Barge, Bus, Caterpillar, Motorcycle, Tank, Van, Bicycle, Car, Helicopter, Segway, Taxi)

## Model
We loaded the MobileNetV2 model given in Keras, froze its parameters, and added a few layers to make it output the final probabilities in 17 nodes, corresponding to 17 classes

## Accuracy
After running the model through each image in the test set and submitting to Kaggle, we got 80% accuracy.

## Credits
- https://keras.io/guides/transfer_learning/
- https://www.kaggle.com/c/vehicle
- Teammates: Bui Quoc Minh Nhat, Nguyen Pham Quoc An