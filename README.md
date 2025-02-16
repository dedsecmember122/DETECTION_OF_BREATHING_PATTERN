# DETECTION_OF_BREATHING_PATTERN
Summary of Thermal Breath Detection Using YOLOv11
1. Introduction This project focuses on detecting breathing patterns using thermal imaging. The primary goal was to distinguish between inhaling and exhaling by analyzing thermal images of the nose region. The project leveraged a dataset of thermal facial images and trained a YOLOv11 model to classify breathing states based on heat variations in the nasal area.
2. Data Collection & Preprocessing
•	Thermal facial images were sourced from "Panetta's Vision and Sensing System Lab."
•	Observed pattern: During exhaling, the nose area appeared darker due to heat emission, while during inhaling, it remained lighter.
•	Gathered around 500 images and uploaded them to Roboflow.
•	Images were manually labeled into two classes: 
o	Exhaling (1): Nose appears dark due to heat release.
o	Inhaling (2): Nose remains light as less heat is emitted.
•	Roboflow's preprocessing tools were used to enhance the dataset quality.
3. Model Training
•	Trained a YOLOv11 model using 30 epochs on the preprocessed dataset.
•	Dataset configuration was defined in data.yaml.
•	Training parameters: 
o	Image size: 84x84
o	Batch size: 8
o	Model used: yolo11l.pt
•	Training duration: Approximately 3 hours for 30 epochs.
4. Real-Time Detection Using OpenCV
•	Implemented a real-time detection system using OpenCV.
•	The system processes live thermal images via a webcam.
•	Bounding boxes are drawn around the nose region, with color-coded labels: 
o	Red (Exhaling)
o	Green (Inhaling)
o	White (No detection)
•	The system provides real-time feedback on breathing patterns.
5. Results & Observations
•	The model successfully detected breathing states in thermal images.
•	Real-time inference showed accurate classification of inhaling and exhaling.
•	The approach demonstrates the potential for medical applications, such as respiratory monitoring.
7. Conclusion This project highlights the effectiveness of YOLOv11 in detecting nasal thermal variations for breath classification. By leveraging AI and thermal imaging, this method can be extended to various applications, including healthcare and biometric security.
