# COMP2005 - Thresholding and Binary Images

## Binary Image Processing (Thresholding)

- What are binary images?
    - Images with only two pixel values (0 and 1)
    - 1 if the pixel will be used in the processing, 0 if not
- Why use binary images?
    - Simplifies the image processing
    - Reduces the amount of data to be processed
    - Can be used to extract features from images
    - Can be used to segment images
- How are binary images created?
    - By using a threshold value to determine if a pixel is 0 or 1
    - Look at each value in the image and compare it to the threshold
- Why is the threshold value important?
    - It determines the quality of the binary image
    - It determines the features that will be extracted
    - It determines the segmentation of the image
- What could happen with an incorrect threshold value?
    - Too high, the background pixels will be classed as foreground
    - Too low, the foreground pixels will be classed as background

### Otsu Thresholding

- What is Otsu Thresholding?
- What does Otsu Thresholding assume?
    - Assumes the histograms are bimodal (two regions can be separated by one threshold)
- How does Otsu thresholding determine the best threshold?
    - It finds the threshold that minimises a weighted sum of the variances of the two regions

### Adaptive Thresholding

- What is adaptive thresholding?
    - A method of thresholding that uses a different threshold value for each pixel
    - The threshold value is determined by the local neighbourhood of the pixel

### Unimodal Thresholding

- Why is unimodal thresholding important?
    - Many histograms are not bimodal
        - E.g. text is mainly white with a small amount of black
- What method is used for unimodal thresholding?
    - Rosin's method
- How does Rosin's method work?
    - Finds the peak of the histogram
    - Draws a line from there to the top of the furthest bin
    - Finds the top of the bin that is furthest from this line
    - That bin value is the threshold
    - This maximises the perpendicular distance between the histogram and the straight line

### Local Adaptive Methods

- Why might a thresholding method fail?
    - If the image has varying illumination
    - If the image has varying contrast
    - If the histogram is too complex
- What is the solution to this?
    - Local Adaptive Thresholding
- How does Local Adaptive Thresholding work?
    - Divides the image into small regions
    - Determines the threshold for each region (could use Otsu)
    - Uses the threshold to create a binary image

## Morphology

### Connected Components

- What are connected components?
    - Groups of pixels that are connected to each other
- What can connected components be used for?
    - Can be used to identify objects in an image
- What can connected mean?
    - 4 or 8 neighbours
- What is the downside of connected component algorithms?
    - They are slow
    - Often a bottleneck
- How does the connected component algorithm work?
    - Look at each pixel in the image
    - If the pixel is part of an object, assign it a label
    - If the pixel is part of a new object, assign it a new label
    - If the pixel is part of an existing object, assign it the label of the object
    - Repeat until all pixels have been labelled

### Dilation

- What is dilation?
    - Takes a binary image and a set of points to be considered
    - The origin is the central element

### Erosion

- What is erosion?
    - Shrinks a foreground / bakcgorund object A, using structuring element B
