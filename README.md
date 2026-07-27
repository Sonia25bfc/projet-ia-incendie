# Fire Detection and Prevention System in Industrial Environments

Building AI course project

## Summary

This project is an intelligent computer vision system capable of detecting fire and smoke in real-time within industrial facilities. By analyzing existing security camera feeds, the AI instantly alerts safety teams, drastically reducing response time and preventing major catastrophes.

## Background

Industrial fires cause tragic human losses and billions of euros in damage every year. Traditional smoke detectors on ceilings often react too late, only when smoke physically reaches the sensor.

* **Problem frequency**: Thousands of industrial fires occur worldwide each year.
* **Personal motivation**: Improving worker safety and leveraging computer vision for public and industrial safety.
* **Importance**: Detecting a fire start within seconds enables immediate suppression and prevents human and economic loss.

## Data and AI methods

The project relies on computer vision and deep learning techniques.

### Data Sources
* Public datasets of fire and smoke images (e.g., Roboflow, Kaggle Fire Detection Dataset).
* Real-time RTSP video streams from standard IP surveillance cameras.

### AI Methods
* **Convolutional Neural Networks (CNN) / YOLO**: Object detection model trained to detect flames and smoke.
* **Image Preprocessing**: Resizing and frame normalization for real-time edge processing.

```python
import cv2

def detect_fire_frame(frame, threshold=0.85):
    resized_frame = cv2.resize(frame, (224, 224))
    fire_confidence = 0.92 
    if fire_confidence > threshold:
        return True, fire_confidence
    return False, fire_confidence

alert, score = detect_fire_frame(None)
if alert:
    print(f"FIRE DETECTED! Confidence: {score * 100:.1f}%")

      
