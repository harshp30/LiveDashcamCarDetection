September 2022

# Live Car Detection Model

#### Credits:

Some of the pipeline is dependent on Nicholas Renotte's tutorial (https://www.youtube.com/watch?v=yqkISICHH-U) and repo (https://github.com/nicknochnack/TFODCourse). The verification script is by him as well as a few coding blocks which take into account different operating systems.

For this project I took an existing set of TFrecords based on this roboflow dataset (https://universe.roboflow.com/gaurigodghase-gmail-com/vehicles-openimages-svzce/dataset/1)

## Description:

This is a computer vision model which utilizes open-cv and tensorflow object-detection to make predicitions on images and a live video feed showing detected vehicles. The model can differeniate between 5 different vehicle types ('Ambulance', 'Bus', 'Car', 'Motorcycle', 'Truck').

The first thing I did when approaching this project was create a virtual environement where all packages would be isolated from the rest of teh computer this helped a lot with organization. Once all of the neccessary packages, dependencies, and dataset where gathered

## Use Case:

This can be used as...

- a dashcam setup for object tracking purposes.
- a object-detction software autonomous vechiles to help with collision avoidance algorithms

## Demonstration

#### Video Demonstration

Following a basic React App model and ibm cloud hosting for the model I published a webiste to create a video demonstration:

(https://car-detection-ed16.netlify.app/)

[![video demo](https://img.youtube.com/vi/sTTXLbIhBGE&ab_channel=HarshPatel/0.jpg)](https://www.youtube.com/watch?v=sTTXLbIhBGE&ab_channel=HarshPatel)

#### Image Demonstration

Here is the model performing on an image:

![image demo](https://github.com/harshp30/LiveDashcamCarDetection/blob/main/images/imagedemo.png)

Here is the model performing through a live feed on an image with multiple object targets:

![image demo](https://github.com/harshp30/LiveDashcamCarDetection/blob/main/images/liveDemo.png)
    
## Performance
 
Using tensorboard I was able to get a few charts displaying training and evaluation metrics as shown below.

#### Evaluation Metrics:

![eval metrics](https://github.com/harshp30/LiveDashcamCarDetection/blob/main/images/evalboxprecision.png)
![eval metrics](https://github.com/harshp30/LiveDashcamCarDetection/blob/main/images/evalboxrecall.png)
 
#### Training Metrics:

![training metrics](https://github.com/harshp30/LiveDashcamCarDetection/blob/main/images/train1.png)

## Key Learnings

I learned a lot througjout this project, everything from hwo to find a reliable dataset to modifying and manpulating labelmaps, and 

The most significant thing I learned through the project is the general pipeline used for computer vision (more specifically object detection). The sequence of creating a isolated env, using TFRecords for training, using my NVIDIA GPU for training with CUDA, evaluating, and finally actually being able to use the model was a great new experience. 

I also learned hwo to export this models into different formats that can then be integrated into application.

## Key Challenges

For this particular project I would say getting the environemnt setup was the hardest part, I had a lot of troubles with packages and versions of certain tools not aligning with requirnments for others. It would have helped me a great deal more if I had the proper documentation and resources that specify things like supported versions ahead of time. Once the environment I was successfully able to use my GPU for accelerated training, which although difficult at first, saved a lot of time.

## Future Expantion
 
This project can be expanded to detect other objects on the road besides vehicles, such as people, traffic signs, and lane lines. 
With all of those different objects being tracked live it would be possible to make simple predictions for driving purposes, such as turning, stopping, and accelerating.


