# COMP2005 - Non-Linear Filtering

## Median Filtering

- What is median filtering?
    - A non-linear filtering technique
    - Each pixel is set to the median value of its neighbourhood
- Why is median filtering used?
    - Result uses a *real* pixel value, as opposed to a combination (eg. mean filtering)
- When is median filtering ineffective?
    - If noise affects more than half of the pixels in the neighbourhood
- When is median filtering not good to use?
    - When the noise is not salt-and-pepper noise
    - When the edges of objects is important

## Anisotropic Diffusion

- What is anisotropic diffusion?
    - A non-linear filtering technique that smooths images while preserving edges
- How does anisotropic diffusion work?
    - Makes each pixel more like its neighbours, only if it's already similar to it
- What linear filter is this similar to?
    - The mean filter
        - With a similarity function of 1, they are identical

## Bilateral Filtering

- What is bilateral filtering?
    - A non-linear filtering technique that smooths images while preserving edges
- What linear filter is this similar to?
    - The Gaussian filter
        - One Guassian filter weights pixels near the source
        - Another Gaussian filter weights pixels with similar intensity
