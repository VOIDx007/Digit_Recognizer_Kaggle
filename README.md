# Digit_Recognizer_Kaggle
This repository contains the zip file "digit-recognizer.zip" (which must be extracted in the same directory as that of the open Jupyter notebook), the notebook containing the code "Digit_recognizer.ipynb" and the screenshot of achieved accuracy in Kaggle compete, where the competition is hosted.

The aim of the competition is to train a model using the images of digits in the train dataset and use it to predict the digits from the images in test dataset.

The steps in the code are-->
1. Read the train and test sets
2. Define the target set Y having the column "label" from the train set and drop that column from the train set
3. Normalize the values of the pixels in test and train sets by dividing them with 255.0
4. Reshape the dataframes (test and train) into 28x28x1 images so that we can use them in a CNN
5. Define a Callback function and make it so that training stops when an accuracy of 100% is reached
6. Define the model, with the required Conv2D, MaxPooling2D, Flatten and Dense layers while making sure the output layer has 10 neurons for each classification of digits
7. Compile the model using an 'adam' optimizer, loss calculated of 'sparse_categorical_crossentropy' and with a metrics of 'accuracy' (required for our callback)
8. Fit the train and target data into the model with the required callback as defined and high enough epochs (GPU should be preferred over CPU to save time)
9. Predict the results using the test data and create "submission.csv" and the "sample-submission.csv" in the dataset file

Uploading the submission result in kaggle compete, a score of **99.142%** accuracy was achieved.
![Digit Recognizer](https://user-images.githubusercontent.com/49501411/124384849-cb89ce80-dcf0-11eb-9b05-3c0b6521b2a5.png)
