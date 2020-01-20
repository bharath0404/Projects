# Projects

## 1.Gesture Recognition using OpenCV and Image processing techniques.

### OBJECTIVE:

To control the Mouse cursor operations using Static Hand Gesture Recognition. 

#### LIBRARIES USED: OpenCV, Tensorflow, Pyautogui.
#### LINK TO CODE: https://github.com/bharath0404/Projects/blob/master/Gesture_Recognition1.py

### BRIEF SUMMARY:

The project aims to recognize the hand gestures and displays the number that the hand is showing using the webcam of laptop. The process of recognition and mouse control is divided up into following parts:

  1. Record the video using webcam from laptop and break it into frames for image processing.
  2. Firstly, the frames are converted into grey scale images. Then, a Gaussian filter is used to remove the noise from the image.
  3. Next, thresholding is done to separate the hand from the background, thus converting the frame into binary image – Background Subtraction.
  4. Now, the contours of the hand are found and the maximum area contour is calculated. Next, a rectangle bounding the contour is created.
  5. A convex null is deduced later and the contours for the fingers are drawn. To detect the gesture, the convexity defects are found applying cosine rule to find angle for all defects.  
  6. If angle < 90, the fingers are detected. If not, they are ignored.
  7. A line is drawn from start to end i.e.., the convex points (finger tips). Based on the number of convexity defects, the gestures are classified into 5 classes of numbers from 1 to 5.
  8. Next, the mouse cursor is mapped to particular gesture using pyautogui library.

