# Garbage Container Dirtiness Detection via Drone 
The goal is to detect waste (garbage and trash) in drone-captured images of streets and alert teams to clean areas with heavy waste accumulation.

## Components:
Drone for Image Capture: A camera-equipped drone will be used to fly over streets, capturing real-time images of areas.
Image Processing using OpenCV: The captured images will be processed using the OpenCV library to detect garbage based on a pre-trained machine learning model.
YoloV3 Model for Garbage Detection: A YOLOv3 model has been trained using a custom dataset containing images of streets with garbage. The model identifies areas where trash is present.
Alerting and Response: When the model detects areas with concentrated waste, the system sends an alert to a response unit to clean those areas.

## Model Training:
A dataset consisting of both clean streets and streets with garbage has been collected from images either taken manually or sourced from the internet.
The YOLOv3 model is trained on this dataset to differentiate between clean areas and those with garbage.
The model's output will identify bounding boxes around detected garbage in the images.

## How it Works:
Drone Image Capture: The drone flies over the targeted streets, taking images at regular intervals.
Image Processing: These images are sent to a PC where the YOLOv3 model is executed using OpenCV.
Garbage Detection: The trained model processes each image, identifying the presence of garbage and drawing bounding boxes around detected trash.
Result Evaluation: If the model detects significant garbage in certain areas, it alerts the team, providing the exact location (from drone GPS data) and possibly visual proof.
Team Deployment: Based on the detected areas, a cleaning team is dispatched to the locations with the highest concentration of trash.

## Video Reference:
The project leverages the methodology shown in this video: Video Reference, where YOLOv3 is used in conjunction with OpenCV for object detection.
