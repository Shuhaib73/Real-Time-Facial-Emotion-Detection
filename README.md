## **Real-Time Face Emotion Detection**


- This project implements real-time facial emotion detection using the Deep CNN and OpenCV, Flask. It captures video from the webcam, detects faces, and predicts the emotions associated with each face. The emotion labels are displayed on the frames in real-time.
- Aims to classify the emotion on a person's face into one of seven categories, using deep convolutional neural networks.
- The dataset consists of 48x48 pixel grayscale images of faces. Each face is classified based on the emotion shown in the facial expression into one of seven categories (0=Angry, 1=Disgust, 2=Fear, 3=Happy, 4=Sad, 5=Surprise, 6=Neutral).

**Approach**

1. Import the necessary libraries: cv2 for video capture and image processing, and CNN for the emotion detection model.

2. Load the Haar cascade classifier XML file for face detection using cv2.CascadeClassifier().

3. Start capturing video from the default webcam using cv2.VideoCapture().

4. Enter a continuous loop to process each frame of the captured video.

5. Convert each frame to grayscale using cv2.cvtColor().

6. Detect faces in the grayscale frame using face_cascade.detectMultiScale().

7. For each detected face, extract the face ROI (Region of Interest).

8. Preprocess the face image for emotion detection using the deepface library's built-in preprocessing function.

9. Make predictions for the emotions using the pre-trained emotion detection model provided by the deepface library.

10. Retrieve the index of the predicted emotion and map it to the corresponding emotion label.

11. Draw a rectangle around the detected face and label it with the predicted emotion using cv2.rectangle() and cv2.putText().

12. Display the resulting frame with the labeled emotion using cv2.imshow().

13. If the 'q' key is pressed, exit the loop.

14. Release the video capture and close all windows using cap.release() and cv2.destroyAllWindows().
