# Document Scanner
This project is a Python script to detect and extract the four corners of a rectangular object in a live video stream and warp the perspective to get a top-down view.

## Libraries used
* cv2 (OpenCV)
* numpy

## How to use
* Clone the repository: git clone https://github.com/BachirMasroua/Document_Scanner
* Change directory: cd Document_Scanner
* Run the Python script: python Document_Scanner_opencvproject.py 

## Explanation
* We first capture the video stream using OpenCV's cv2.VideoCapture() method.
* We define the width and height of the video frame.
* We preprocess the captured image using the preProcessing() function which converts the image to grayscale, applies Gaussian blur, detects edges using Canny edge detection, dilates and erodes the edges.
* We then use the getContours() function to get the contour with the largest area and four corners. We also apply some filters to eliminate small contours that could be detected.
* We then use the reorder() function to rearrange the four corners of the contour.
* We use getWarp() function to get the top-down view of the object. We use OpenCV's cv2.getPerspectiveTransform() method to calculate the transformation matrix and the cv2.warpPerspective() method to apply the perspective transformation.
* Finally, we use the stackImages() function to display the original image and the warped image side by side.
