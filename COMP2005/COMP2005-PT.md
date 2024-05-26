# COMP2005 - Point Transforms

## Linear Transformations

- What are the two common types of linear intensity transforms?
    - Multiplication by a constant (gain), controlling contrast
    - Addition of a constant (bias), controlling brightness
- What is the formula for gain?
    - g(x,y) = a*f(x,y)
- What is the formula for bias?
    - g(x,y) = f(x,y) + b
- What is the formula for negations?
    - g(x,y) = fmin + (fmax - f(x,y))
    - g(x,y) = -f(x,y) + (fmin + fmax)
- Why might negations be used?
    - To make fine details more visible
    - To make the image more suitable for edge detection
- What is contrast stretching?
    - Converts an image with intensity minx to maxx to an image with intensity miny to maxy
- What is the formula for contrast stretching?
    - g(x,y) = ((f(x,y) - minx) * (maxy - miny) / (maxx - minx)) + miny

## Non-Linear Transformations

- What are three common non-linear transforms?
    - Thresholding
    - Grey level slicing
    - Gamma Correction
- What is thresholding?
    - See (Thresholding and Binary Images)[./COMP2005-TBI.md]
- What is grey level slicing?
    - Highlighting a specific range of grey levels
    - Can reduce other grey levels to a lower level, or preserve them
- What is gamma correction?
    - Adjusting the luminance of the image to match the displays response curve
    - Ensures the image is displayed as intended

