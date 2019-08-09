# Computer-Vision
Computer Vision projects using python and librarires as `matplotlib`, `opencv`, so don't forget to install them.

## Image resizing using Bilinear interpolation

Bilinear interpolation considers the closest 2 × 2 neighborhood of known pixel values surrounding the unknown pixel's computed location. 
It then takes a weighted average of these 4 pixels to arrive at its final, interpolated value.
```
Q1 = ((x2 – x)/(x2 – x1)) * Q11 + ((x – x1)/(x2 – x1)) * Q21
Q2 = ((x2 – x)/(x2 – x1)) * Q12 + ((x – x1)/(x2 – x1)) * Q22

Q = ((y2 – y)/(y2 – y1)) * Q1 + ((y – y1)/(y2 – y1)) * Q2
```
For edge pixels I used the most nearest pixel.
