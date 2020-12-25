# Projects

## 1.Gesture Recognition 

### OBJECTIVE:

To control the Mouse cursor operations using Static Hand Gesture Recognition. 

#### LIBRARIES USED: OpenCV, Tensorflow, Pyautogui.

#### LINKS TO CODE: 
* https://github.com/bharath0404/Projects/blob/master/Gesture_Recognition1.py
* https://github.com/bharath0404/Projects/blob/master/Gesture_Recog_AI.py 


### BRIEF SUMMARY:

The project aims to recognize the hand gestures and displays the number that the hand is showing using the webcam of laptop. This project is accomplished by two different approaches:

1. Using simple Image Processing techniques using OpenCV
2. Using Deep learning based classification using Keras

**Using Image processing with OpenCV:**

The part of the project aims to recognize the hand gestures and displays the number that the hand is showing using the webcam of laptop. The process of recognition and mouse control is divided up into following parts:

1. Record the video using webcam from laptop and break it into frames for image processing.
2. Firstly, the frames are converted into grey scale images. Then, a Gaussian filter is used to remove the noise from the image.
3. Next, thresholding is done to separate the hand from the background, thus converting the frame into binary image – Background Subtraction.
4. Now, the contours of the hand are found and the maximum area contour is calculated. Next, a rectangle bounding the contour is created.
5. A convex null is deduced later and the contours for the fingers are drawn. To detect the gesture, the convexity defects are found applying cosine rule to find angle for all defects.
6. If angle < 90, the fingers are detected. If not, they are ignored.
7. A line is drawn from start to end i.e.., the convex points (finger tips). Based on the number of convexity defects, the gestures are classified into 5 classes of numbers from 1 to 5.
8. Next, the mouse cursor is mapped to particular gesture using pyautogui library.

**Using Deep Learning with Keras**

This part of the project deals with recognizing the hand gestures after a CNN is trained on a grouped lists of each gesture as a class after which the prediction happens based on the probability results from CNN.

    
## 2. A Perceptron NN for Sonar signal classification

### OBECTIVE:

To classify a Sonar based signal in submarines processed by computing systems into ‘MINE’ or ‘ROCK’ by Perceptron Neural Network built from scratch.

#### LINK TO CODE: 
* https://github.com/bharath0404/Projects/blob/master/Perceptron_From_Scratch.py 

#### BRIEF SUMMARY:

The project is broken down into 3 parts:

1. Making Predictions.
2. Training Network Weights.
3. Modeling the Sonar Dataset.

1. The dataset is first loaded, the string values converted to numeric and the output column is converted from strings to the integer values of 0 to 1. This is achieved with helper functions load_csv(), str_column_to_float() and str_column_to_int() to load and prepare the dataset.

2. We will use k-fold cross validation to estimate the performance of the learned model on unseen data. This means that we will construct and evaluate k models and estimate the performance as the mean model error. Classification accuracy will be used to evaluate each model. These behaviors are provided in the cross_validation_split(), accuracy_metric() and evaluate_algorithm() helper functions.

3. We will use the predict() and train_weights() functions created above to train the model and a new perceptron() function to tie them together. A k value of 3 was used for cross-validation, giving each fold 208/3 = 69.3 or just under 70 records to be evaluated upon each iteration. A learning rate of 0.1 and 500 training epochs were chosen with a little experimentation. Running this example prints the scores for each of the 3 cross-validation folds then prints the mean classification accuracy.

