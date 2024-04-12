**Mood Detection System using Computer Vision and Deep Learning**

**Overview:**
This project implements a real-time mood detection system using computer vision techniques for face detection and deep learning for emotion recognition. The system captures video input from a webcam, detects faces in each frame, and analyzes the facial expressions to determine the dominant emotion displayed by each individual.

**Libraries Used:**
- OpenCV: Utilized for face detection using a pre-trained Haar Cascade classifier.
- Keras: Used for deep learning tasks, specifically for preprocessing images and loading the pre-trained emotion recognition model.
- DeepFace: A deep learning library that provides an easy-to-use interface for facial analysis tasks, including emotion recognition.

**Face Detection:**
- The project begins by initializing a video capture object (`cv2.VideoCapture(0)`) to access the webcam feed.
- It employs a pre-trained Haar Cascade classifier (`haarcascade_frontalface_default.xml`) to detect faces in each frame of the video stream. 
- Detected faces are highlighted with rectangles drawn using `cv2.rectangle()` to provide visual feedback to the user.

**Emotion Recognition:**
- After detecting faces, the system extracts the region of interest (ROI) corresponding to each face detected.
- The ROI is preprocessed, resized, and converted into a format suitable for input to the emotion recognition model.
- Utilizing the DeepFace library, the preprocessed face ROI is analyzed to determine the dominant emotion displayed by the individual.
- Emotion labels such as 'Angry', 'Happy', 'Confused', 'Sad', 'Fear', and 'Neutral' are predefined to classify the detected emotions.
- The detected emotion is then displayed on the video frame using `cv2.putText()`.

**User Interaction:**
- The system continuously processes video frames until the user interrupts the process by pressing the spacebar key.
- Upon receiving the spacebar key press (`cv2.waitKey(1) & 0xFF == ord(" ")`), the processing loop breaks, and the resources are released.

**Conclusion:**
This mood detection system provides a simple yet effective means of analyzing facial expressions in real-time. It demonstrates the integration of computer vision and deep learning techniques to create an interactive application for emotion recognition. Future enhancements may include improving the accuracy of emotion detection, implementing user interfaces, and integrating the system into various applications such as virtual assistants, health monitoring systems, and interactive gaming platforms.
