# Analyze Sports Activities
<center>
<a href="http://commonmark.org" title="Redirect to homepage">
<img src="BackgroundImages/pexels-ivan-samkov-7676505.png"
     alt="Sports Activities Icon"
     style="width:648px;height:432px;" />
</a>
</center>

Fig. 1: Human Pose Detection. Adapted from Ivan Samkov, www.pixels.com

Various gymnastic exercises are recognized, classified and analyzed via video.

## Motivation
If you exercise regularly, it is desirable to have a recording of your activities. This gives you an overview of the intensity of the workouts and development of your fitness over the weeks and months. Therefore, tracking tools for running, cycling, etc. are very popular. Unfortunately, for many kinds of sports (weight training, gymnastics, etc.) there is no automatic recording option.

## Solution
Activities are recorded by a camera and analyzed by various methods. The Algorithms detect the type of exercise (squat, jump, pull-up, ...) and count the number of repetitions. This is done by applying the body pose tracking algorithm from [MediaPipe](https://google.github.io/mediapipe/solutions/pose.html). The identified landmarks (Fig. 1) are used for identifying the type of exercise, measuring the speed of an exercies und count the number of repetitions.
Unfortunately there is not much data available to train the system. Therefore a simple learning strategy is used. For each exercise one video with several repetitions of this exercise is provided together with a very limited number of required labels. 


## Learning: Input data
These labels are the name of the exercise as well as the start and end time of the exercises within the video is manual added. Fig. 2 shows the parameters and labels for 5 different exercises (mp4-files) to be learned. 
<a href="https://github.com/Sepp28" title="CSV-File">
<img src="BackgroundImages/ExampleCSV_File.png"
     alt="Sports Activities Icon"
     style="width:648px;height:432px;" />
</a>

Fig. 2: Data provided for the learning phase

Note that it is always possible to add further exercises. The learning algorthim will generate a modell for the new activity and will recognize it furtheron.

## Learning: Algorithms
The algorithms extract characteristic features of that exercise 

## Evaluation


## Conclusion

