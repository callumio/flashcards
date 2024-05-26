# COMP2005 - Colour Spaces

## Colour Spaces

- Why is the RGB colour model not always ideal for image processing?
    - The RGB model mixes light colours and may not separate colour from intensity
    - Can be sensitive to illumination changes
- How do HSV colour spaces represent colours?
    - Hue (colour)
    - Saturation (intensity of colour)
    - Value (brightness)
- How can an RGB image be converted to grayscale?
    - Using the formula i = 0.30r + 0.59g + 0.11b
    - This is weighted using the sensitivity of the human eye
- Why are colour values not (usually) 100% reliable?
    - They are often interpolated, unless you have a 3 CCD camera
- Why might you want to convert an image to a different colour space?
    - To separate colour from intensity
    - To make the image more robust to illumination changes
    - To make the image more robust to noise
- Why might you want to ignore certain channels?
    - Not all applications will require all 3 channels
        - E.g. human skin is tightly clustered in HS space so you can ignore V
