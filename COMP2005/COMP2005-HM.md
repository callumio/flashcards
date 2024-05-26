# COMP2005 - Histogram Methods

## Histograms in Image Processing

- Why are histograms used?
    - They provide global information about an image
    - Ease computation of some image properties
    - Can be manipulated to enhance / improve images
- What would a dark image vs a light image look like in a histogram?
    - Dark image: Peaks towards the left
    - Light image: Peaks towards the right
- What would a low contrast image vs a high contrast image look like in a histogram?
    - Low contrast: Peaks are close together
    - High contrast: Peaks are spread out

## Histogram Normalisation

- What makes a histogram normalised?
    - The sum of all the values in the histogram is equal to 1
- What does each value in a normalised histogram represent and why is this useful?
    - The probability of a pixel having that grey level
    - Useful for contrast enhancement and automatic thresholding

## Histogram Equalisation

- What is histogram equalisation?
    - A method to improve the contrast of an image
    - Spreads out the intensity values in the histogram into a uniform distribution
- What is the formula for histogram equalisation?
    - s = T(r)
        - s is the new histogram
        - T is the transformation function
        - r is the input histogram, normalised to [0,1]
- What are the strengths of histogram equalisation?
    - Can be used to enhance images with low contrast
    - Can be used to enhance images with high contrast
