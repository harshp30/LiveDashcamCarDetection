September 2022

# Live Car Detection Model

**More details and actual code can be found in the notebook**

#### Credits:

Some of the pipeline is dependent on Nicholas Renotte's tutorial (https://www.youtube.com/watch?v=yqkISICHH-U) and repo (https://github.com/nicknochnack/TFODCourse). The verification script is by him as well as a few coding blocks that take into account different operating systems.

For this project, I took an existing set of TFrecords based on this roboflow dataset (https://universe.roboflow.com/gaurigodghase-gmail-com/vehicles-openimages-svzce/dataset/1)

## Description:

This is a computer vision model which utilizes open-cv and TensorFlow object-detection to make predictions on images and a live video feed showing detected vehicles. The model can differentiate between 5 different vehicle types ('Ambulance', 'Bus', 'Car', 'Motorcycle', 'Truck').

The first thing I did when approaching this project was create a virtual environment where all packages would be isolated from the rest of the computer this helped a lot with organization. Once all of the necessary packages, dependencies, and dataset were gathered, I prepared different file paths in /TensorFlow for images. Even though the dataset was from an online source I created these paths for my own testing. After that, I set up variable paths for training purposes and ran the verification script (credited above) to make sure all packages and dependencies were in check. Lastly, before training, I adjusted the config file with the various paths. During training, I used CUDA to train the model on my NVIDIA GPU for accelerated speeds. After the model was done training I went through Tensorboard for evaluation metrics, did a test with an image, and then tested with a live feed. Finally, I froze the graph and made the model conversions to TFLite and TFJS.

## Use Case:

This can be used as...

- a dashcam setup for object tracking purposes.
- an object-detection software autonomous vehicles to help with collision avoidance algorithms

## Demonstration

#### Video Demonstration

Following a basic React App model and ibm cloud hosting for the model I published a webiste to create a video demonstration:

https://car-detection-ed16.netlify.app/

https://www.youtube.com/watch?v=sTTXLbIhBGE&ab_channel=HarshPatel

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

I learned a lot throughout this project, everything from how to find a reliable dataset, modifying and manipulating label maps, and different conversion methods for models to later be used in a practical application.

The most significant thing I learned through the project is the general pipeline used for computer vision (more specifically object detection). The sequence of creating an isolated env, using TFRecords for training, using my NVIDIA GPU for training with CUDA, evaluating, and finally actually being able to use the model was a great new experience.  

## Key Challenges

For this particular project, I would say getting the environment setup was the hardest part, I had a lot of troubles with packages and versions of certain tools not aligning with requirements for others. It would have helped me a great deal more if I had the proper documentation and resources that specify things like supported versions ahead of time. Once in the environment, I was successfully able to use my GPU for accelerated training, which although difficult at first, saved a lot of time.

## Future Improvements and Expansion

The biggest downside of this project is its speed, especially when converted into TFJS or TFLite and using it in an app. As you can see from the video demonstration below, the model does a good job at detecting a vehicle, however, it is quite slow in actually processing that information and "boxing" it in. Especially with a moving car, it struggles to move along with it. A solution to this could probably be a much larger dataset and an alternative to using converted model types.
 
This project can be expanded to detect other objects on the road besides vehicles, such as people, traffic signs, and lane lines. 
With all of those different objects being tracked live, it would be possible to make simple predictions for driving purposes, such as turning, stopping, and accelerating.

