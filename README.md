# Cartoonify-the-images-using-ml
Cartoonify Reality  is an OpenCV project that uses core OpenCV functions and the K-Means clustering algorithm to perform image processing and cartoony them. This project shows how good image processing can be used to do the same task that normally takes a machine learning model and high computational power. Usually, the same task is done using either auto-encoders or GANs(Generative Adversarial Networks). In this blog, we will explore more of Computer Vision and Image processing.

The workflow is as described below-



We will start by working on images as input. These images can easily be converted to videos. Take the source image, blur it using a Bilateral filter. Use canny to finds its edges. Then convert the image into HSV(Hue-Saturation-Value) format and apply K-means clustering to it. Convert it back to RGB(Red-Green-blue) format and draw contours on the image. Finally, use erosion to thicken the boundaries and display the output image.



# Computer Vision

Computer Vision(CV) is a field of computing that deals with replicating the complexity and vision of the human eye. Various algorithms and formulae are developed to help computers visualize better. Input is taken from cameras, and output can vary with use. The most famous application as of today is object detection as shown below.



# OpenCV

OpenCV is an open-source software containing pre-built functions and algorithms used for implementing Image Processing and Computer Vision. The python library that we will be using is “cv2”. It is one of the most widely used libraries in python with over 18 million downloads. We will be using some of those built-in functions to process our input image.

Start by creating a new python file and importing it.


import cv2
Define the main function of our code-


 takes input image as parameter
def cartoon(image):
    
    returns the output image 
   return output
   
# Burring

Blurring in terms of digital image processing is smoothing of the image, removing noise from it. Filtering is one of the fundamental operations of Image Processing. Filters like Gaussian Blur, Median Blur blur images, but they also tend to smooth the edges. To avoid that we will use the Bilateral Filter.


The figure shows the most commonly used blurring techniques. It may be hard to distinguish but as the filter size is increased the difference becomes more visible.

# Contours

A contour is a closed curve joining all the points with either the same intensity or color. They help in visualizing the shape of objects or figures in an image. Normally to use this filter we first need to use either canny or some thresholding. The specifics of the function may get tricky, it is recommended to go through its documentation. We will use this method in our code to give boundaries to our output image so that each object is distinctly visible.


# Erosion

Erosion is a morphological process that mostly deals with altering shapes in an image. Dilation and erosion are sister processes. In simple terms, they are used to thicken or lessen boundary shapes in an image. We will use it to erosion to thicken the contour boundaries to make them stand out.


