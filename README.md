# Computer-Vision
This project presents a real time system for detecting and analyzing crowd behavior using 3D Convolutional Neural Networks (3D CNNs). The system is designed to monitor public spaces and identify abnormal behaviors such as panic, aggression, or unusual movement patterns to enhance safety and situational awareness.

# Objective
1. To design a flexible and dependable system incorporating a camera and machine learning to effectively monitor and manage crowds in tracking behavioral patterns;
      a) The system can display 85-90% accuracy in different crowd dynamics (100, 500, and 1000 crowd sizes), and different environments such as in a       School Cafeteria and a school-based Event (Flag Ceremony).
   
      b) A system able to monitor and manage the crowd with uptime from Monday to Saturday:
      I. 7 am to 9 am in the Flag Ceremony; and
      II. 11 am – 1 pm in the School Cafeteria;
      
      c) The system output will be compared to the real-world observation of the behavioral pattern, including the following:
      I. Violence and Brawl;
      II. Seizure and Fainting; and
      III. Behavioral Panic.
      
      d) The system should have a latency of less than 2 seconds between collected data from the camera and the corresponding alert or notification         displayed or updated on the user interface.

2. To utilize video processing and machine learning algorithms that can quickly spot crowd behaviors, and potential threats such as brawl and running in multiple directions, and potential health threats such as seizure and fainting as they happen;
   
3. To implement the system in different settings, like in School grounds, such as in School cafeterias, and during School events, like Flag ceremonies, so that it can give real-time support to event organizers, school officials, law enforcement, and health services for better crowd management and public safety; and,

4. 4. To evaluate the performance of the real-time crowd behavior control and monitoring system in various environments, focusing on its accuracy in detecting crowd behaviors and potential threats. Using ISO/IEC-25010 in terms of:
   
      a) Accuracy;
      
      b) Reliability;
      
      c) Functionality; and
      
      d) Performance Efficiency.

# Technologies Used
      - Python
      - TensorFlow / Pytorch
      - OpenCV
      - 3D CNN (Convolution Neural Network)
      - Jetson Nano J1010
      - Webcam
      - CUDA
      - Flask

# Dataset
We used a combination of publicly available and custom video datasets to train and test our real-time crowd behavior monitoring system. The data was collected from Kaggle, YouTube, and original recordings.


| Behavior Type | Number of Clips    |
| ------------- | ------------------ |
| Normal        | 1,239              |
| Brawl         | 520                |
| Panic         | 130                |
| Fainting      | 400                |


Source: Kaggle, YouTube, and custom-recorded videos

Clip Duration: Each video was segmented into clips ranging from 1 to 5 seconds

Preprocessing:

      Videos reduced to 1-second clips and cropped
      
      From each clip, 16 frames were extracted
      
      Frames resized to 112×112 pixels
      
      Normalized pixel values
      
      Converted to uniform frame rate
      
      Label encoding for classification
      

# Results
The system achieved the following classification accuracy across behavior types:

| Behavior Type | Accuracy |
| ------------- | -------- |
| Brawl         | 91.67%   |
| Fainting      | 85.00%   |
| Panic         | 85.00%   |
| Normal        | 91.67%   |

Overall Accuracy: 88.33%

# Future Work

1. Improve Model Accuracy and Adaptability
Further enhancement of the 3D-CNN algorithm is recommended to increase the system’s precision in detecting complex behaviors. This includes expanding the dataset and training it with more diverse and context-rich scenarios.

2. Multimodal Integration
Future versions of the system could integrate sound detection to recognize auditory cues such as shouting, cries, or distress calls. This would improve responsiveness and provide more reliable early warnings.

3. Wider Behavior Coverage
The current system focuses on detecting brawl, panic, fainting, and normal behavior. Future iterations should include a broader spectrum of crowd behaviors (e.g., loitering, stampede, group formation, etc.) for comprehensive public safety monitoring.
