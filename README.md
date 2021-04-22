# Air Canvas
Air Canvas is a tool which can draw anything on it by just capturing the motion of a colored marker with a camera. Here a colored object at the tip of the finger is used as the
marker.
We will be using the computer vision techniques of OpenCV to build this project. The preferred language is Python due to its exhaustive libraries and easy to use syntax but
understanding the basics it can be implemented in any OpenCV supported language.

Here Color Detection and tracking are used in order to achieve the objective. The color marker is detected and a mask is produced. It includes the further steps of
morphological operations on the mask produced which are Erosion and Dilation. Erosion reduces the impurities present in the mask and dilation further restores the eroded main
mask.

# Requirements
1. python3
2. numpy
3. opencv

# Algorithm
1. Start reading the frames and convert the captured frames to HSV color space (Easy for color detection).
2. Prepare the canvas frame and put the respective ink buttons on it.
3. Adjust the track bar values for finding the mask of the colored marker.
4. Preprocess the mask with morphological operations (Eroding and dilation).
5. Detect the contours, find the center coordinates of largest contour and keep storing them in the array for successive frames (Arrays for drawing points on canvas).
6. Finally draw the points stored in an array on the frames and canvas.
