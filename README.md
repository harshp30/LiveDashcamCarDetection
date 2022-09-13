# Live Car Detection Model

#### Credits:

Some of the pipeline is dependent on Nicholas Renotte's tutorial (https://www.youtube.com/watch?v=yqkISICHH-U) and repo (https://github.com/nicknochnack/TFODCourse). The verification script is by him as well as a few coding blocks which take into account different operating systems.

For this project I took an existing set of TFrecords based on this roboflow dataset (https://universe.roboflow.com/gaurigodghase-gmail-com/vehicles-openimages-svzce/dataset/1)

## Demonstration

## Description:

This is a computer vision model which utilizes open-cv and tensorflow object-detection to make predicitions on images and a live video feed showing detected vehicles. The model can differeniate between 5 different vehicle types ('Ambulance', 'Bus', 'Car', 'Motorcycle', 'Truck').

## Use Case:

This can be used as...
    - a dashcam setup for object tracking purposes.
    - a object-detction software autonomous vechiles to help with collision avoidance algorithms
    
## Display

Here is the model performing on an image:

![image demo](https://github.com/harshp30/LiveDashcamCarDetection/blob/main/images/imagedemo.png)
    
## Performance
 
Using tensorboard I was able to get a few charts displaying training and evaluation metrics as shown below.

#### Evaluation Metrics:

![eval metrics](https://github.com/harshp30/LiveDashcamCarDetection/blob/main/images/evalboxprecision.png)
![eval metrics](https://github.com/harshp30/LiveDashcamCarDetection/blob/main/images/evalboxrecall.png)
 
#### Training Metrics:

![training metrics](https://github.com/harshp30/LiveDashcamCarDetection/blob/main/images/train1.png)

## Future Expantion
 
This project can be expanded to detect other objects on the road besides vehicles, such as people, traffic signs, and lane lines. 
With all of those different objects being tracked live it would be possible to make simple predictions for driving purposes, such as turning, stopping, and accelerating.


