# FILIPE`S SUBMITION - REPO CHALLENGE  DSSIPD
 

First, I was trying to run the python codes like it is presented on the GitHub repo (https://github.com/surya-veer/movement-tracking).
However, I got an error message, and my camera did not pop up how it should be.

Then, I started checking on the above-mentioned repo if someone faced this problem before, and I found the solution.


In both moviment-v1.py (line 74) and moviment-v2.py (line 77), I changed the camera parameters, so the camera can capture the video and track my movements.

*IN BOTH CASES I CHANGED THE FOLLOWING:*
```bash
# before changing
video_capture = cv2.VideoCapture(-1)

# after changing 
video_capture = cv2.VideoCapture(0)

```
This simple change made the whole difference, because now the camera is tracking the movements very well.

## OBERSERVATION

By testing both moviment-v1.py and moviment-v2.py, I could notice that the version1 workes better. I could play few games using the moviment-v1.py, and the code response was quite satisfactory. I enjoyed it a lot.


## CONCLUSION

The code is working well and it is possible to use this simple code not only to play games with your camera but to control everything with is direction-based.
I have uploaded a video with myself testing the code: **Filipe_Leao_result.mp4**. 

Below you can check the original Readme text.
Thanks!
Filipe Leao

-----


# Realtime Face Movement Tracking ![](https://bit.ly/surya-veer-movement-tracking)
90 Lines of code to convert your face movement into keyboard commands.

# Description
This is a basic face movement tracking that can convert face movement into keyboard commands like **UP - DOWN - LEFT  - RIGHT**. I used facial landmarks to detect face and get the nose out of it for better referencing. I have created two versions of it, v1 is using a fixed reference boundary which not work expected properly because we need to come at the same position after each movement. To save this I created V2 which uses position change with respect to the previous position. This is more dynamic and easy to control the moves. No need to set position again and again.

## movement-v1.py
In version1, I used a fixed reference boundary. If nose reference is out of boundary then I calculate the direction of movement. After getting direction I am converting it into keyboard commands using the keyboard library.

## movement-v2.py
In version2, I am using reference change with respect to the previous position in a particular time window and then calculating the direction vector to get direction and converting it to keyboard command.

## Dependencies
This is the list of dependencies for running this application. Use pip to install them.
 * **opencv**
 * **keyboard**

 ```
 $ pip install -r requirements.txt
 ```

## How to use
1. Download or clone this repository.
2. Extract to some location.
3. First, run **```movement-v1.py```** (for fix boundary) or run **```movement-v2.py```**(for dynamic movement) <br>
  NOTE: If you are getting 215 assertion failed!! on line 81 check this (https://github.com/surya-veer/movement-tracking/issues/4#issuecomment-664018021)

4. open any online atari game like Subway surfers or temple run.
5. Start doing movements to play game. It will press up-down-left-right based on your movements.

# Fun with face movements
Open any online game on the browser which needs UP-DOWN-LEFT-RIGHT movements following games, you can find many games if you search on google.
1. Subway surfer https://www.kiloo.com/subway-surfers/
2. Temple run https://m.plonga.com/adventure/Temple-Run-2-Online-Tablet

### You can do a lot more things by the small code change.

### ** SUPPORT OPEN SOURCE **
