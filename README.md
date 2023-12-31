**Real-time Driver Drowsiness Detection System using Computer Vision and Deep learning**


This Python script is a real-time driver drowsiness detection system that employs computer vision and deep learning techniques. Here's a breakdown of its main components and functionality:

1. **Libraries and Modules:**
   - The script starts by importing necessary libraries, including OpenCV (`cv2`), operating system (`os`), Keras (`load_model`), NumPy (`np`), and Pygame (`mixer`).

2. **Initialization:**
   - Pygame is initialized for audio alerts, and an alarm sound (`alarm.wav`) is loaded.

3. **Cascade Classifiers:**
   - Haar cascade classifiers are utilized for detecting facial features, specifically the face, left eye, and right eye.

4. **Model Loading:**
   - A pre-trained Convolutional Neural Network (CNN) model (`cnncat2.h5`) is loaded using Keras. This model is likely trained to classify whether eyes are open or closed.

5. **Video Capture:**
   - The script opens a video capture stream from the default camera (index 0).

6. **Main Loop:**
   - Inside the main loop, the video frames are continuously captured.

7. **Face and Eye Detection:**
   - Haar cascade classifiers are applied to detect faces, left eyes, and right eyes in the captured frame.

8. **Eye Classification:**
   - For both left and right eyes, the corresponding regions are extracted and preprocessed.
   - These regions are fed into the pre-trained CNN model to predict whether the eyes are open or closed.

9. **Scoring:**
   - A scoring system is implemented based on the predictions. If both eyes are closed, the score is incremented; otherwise, the score is decremented.

10. **Display:**
    - The frame is annotated with rectangles around detected faces and eyes, along with text indicating whether the eyes are open or closed.
    - The score is displayed on the frame.

11. **Drowsiness Alert:**
    - If the score surpasses a certain threshold (15 in this case), indicating potential drowsiness, an alarm sound is played, and a red rectangle is drawn around the frame.

12. **User Interaction:**
    - The application can be terminated by pressing 'q'.

13. **Cleanup:**
    - After exiting the main loop, the video capture is released, and OpenCV windows are destroyed.

**Overall Description:**
This project is designed to actively monitor a driver's alertness in real-time by analyzing facial features and eye states. It utilizes computer vision for face and eye detection and a pre-trained deep learning model for eye state classification. The system provides visual feedback on the frame, including a real-time score, and triggers an alarm if signs of drowsiness are detected, aiming to enhance road safety.


**Screenshots**

<img width="490" alt="Screenshot 2023-12-31 135455" src="https://github.com/KRISHNAVAMSI599/Real-time_Driver_Drowsiness_Detection_System_using_Computer_Vision_and_Deep_learning/assets/138597505/4a88c7f1-ae7f-4da3-9428-209d88cf1891">
![Screenshot (430)](https://github.com/KRISHNAVAMSI599/Real-time_Driver_Drowsiness_Detection_System_using_Computer_Vision_and_Deep_learning/assets/138597505/ec857d4e-0042-4b3f-b100-e92f382744bc)
![Screenshot (419)](https://github.com/KRISHNAVAMSI599/Real-time_Driver_Drowsiness_Detection_System_using_Computer_Vision_and_Deep_learning/assets/138597505/129983af-106d-4a73-a297-799a3f6fcec3)
