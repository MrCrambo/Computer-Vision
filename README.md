# Computer Vision
Computer Vision projects using python and librarires as `matplotlib`, `opencv`, so don't forget to install them.

## 1. Image resizing

### Bilinear interpolation for image size increasing

Bilinear interpolation considers the closest 2 × 2 neighborhood of known pixel values surrounding the unknown pixel's computed location. 
It then takes a weighted average of these 4 pixels to arrive at its final, interpolated value.
```
Q1 = ((x2 – x)/(x2 – x1)) * Q11 + ((x – x1)/(x2 – x1)) * Q21
Q2 = ((x2 – x)/(x2 – x1)) * Q12 + ((x – x1)/(x2 – x1)) * Q22

Q = ((y2 – y)/(y2 – y1)) * Q1 + ((y – y1)/(y2 – y1)) * Q2
```
For edge pixels I used the most nearest pixel.

You can find notebook with code and examples [here](https://github.com/MrCrambo/Computer-Vision/blob/master/Image%20Resizing/ImageBilinearResizing.ipynb).

### Decreasing image size using convolution and averaging

Convolution allows to change the image using different filters, and one of these filters we used for smoothing (kernel with ones - averaging kernel).

Also there are a lot of other types of kernels for filtering like highpass kernel, lowpass kernel, laplacian kernel, etc. Here is the few examples.
- Averaging kernel

![Averaging kernel](http://aishack.in/static/img/tut/conv-simple-blur.jpg)

- Edge detection kernel

![Edge detection kernel](http://aishack.in/static/img/tut/conv-edge-detection.jpg)

- Laplacian of Gaussian kernel

![Laplacian of Gaussian kernel](http://aishack.in/static/img/tut/conv-laplacian-of-gaussian.jpg)

You can find more info about this kernels by clicking this [link](https://northstar-www.dartmouth.edu/doc/idl/html_6.2/Filtering_an_Imagehvr.html) and this [link](http://aishack.in/tutorials/image-convolution-examples/) and use all this kernels in code. Just pass the array of your kernel to the convolution function like below:
```python
# highpass kernel
krl = np.array([[0, -1, 0], [-1, 5, -1], [0, -1, 0]])

conv_img = convolution(img, krl)
```

You can find notebook with code and examples [here](https://github.com/MrCrambo/Computer-Vision/blob/master/Image%20Resizing/ImageSizeDecreasing.ipynb).

## 2. Object detection

Detecting objects using OpenCV library.

Change the masks and it will be possible to use it for detecting another images, in this case we are detecting strawberry. And so masks are prepared for detecting strawberry features.

![Image detection](https://github.com/MrCrambo/Computer-Vision/blob/master/Object%20Detection%20With%20OpenCV/detected.jpg)
