# COMP2005 - Spatial Filtering

## Spatial Filtering

- Why do we use spatial filtering over intensity transforms?
    - Spatial filtering allows us to apply different operations to different parts of the image
    - Images are spacially organised data structures with important attributes varying across the image
        - Object identity
        - Viewed surface orientation, colour, etc
        - Illumination

- What is the difference between spatial and intensity filtering?
    - Spatial filtering can modify multiple parts of an image
    - Intensity transforms can only read and affect a single pixel

## Noise

- What is noise?
    - Small errors in image values
- How is noise introduced into images?
    - Imperfect sensors introduce noise
    - Lossy compression
- What is Gaussian Noise?
    - Noise that follows a Gaussian distribution
    - Has a mean u and variance sigma^2
- How can noise be reduced from multiple images?
    - Take the mean value of each pixel
    - The larger the set of images, the better the noise reduction
- How can noise be reduced from a single image?
    - Averaging over a local region has a similar affect
    - Ideally, the region should only include puxels that should have the same value

## Convolution

- What is convolution?
    - A mathematical operation that combines two functions to produce a third function
- How is convolution used in image processing?
    - Used to apply filters to images
- What pattern is used for these filters?
    - A small matrix of values is given in the filter window and picture window
    - Each image value is multiple by the corresponding filter value
    - The sum of these values is the new image value

## Mean Filtering

- What is mean filtering?
    - A type of spatial filtering that replaces each pixel value with the average of its neighbours
- How is mean filtering applied?
    - A filter window is moved over the image
    - The average of the values in the window is calculated
    - The central pixel is replaced with this average

## Gaussian Filtering

- What is Gaussian filtering?
    - Convolution with a mask
    - The mask is determined by a 2D Gaussian function
    - Pixels near the source value are given a higher weight
    - This is because they are more likely to lie on the same object
- What is discrete Gaussian filtering?
    - The function is restricted to a square window
    - The end result is normalised so the filter sums to 1
- How should the size of the filter window be chosen?
    - The size of the filter should be chosen based on the standard deviation of the Gaussian function
    - The larger the standard deviation, the larger the filter
- How is a Gaussian filter applied?
    - A 2D Gaussian is equivalent to two, 1D Gaussians
    - First, filter with a horizontal Gaussian
    - Then, filter with a vertical Gaussian

## Separable Filters

- Why are separable filters used?
    - A separated filter is far more efficient
    - Given an n\*n filter and a N\*N image
        - The number of operations is O(N^2 * n^2)
    - Given two n\*1 (separated) filters and a N\*N
        - The number of operations is O(N^2 * 2n)
        - This is a significant reduction in operations
