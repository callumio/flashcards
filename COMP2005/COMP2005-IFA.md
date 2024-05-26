# COMP2005 - Image Formation and Acquisition

## Sampling and Quantisation

- What is the purpose of sampling?
    - Digitises the spatial coordinates of an image, determines it's spatial resolution
- What is the purpose of quantisation?
    - Digitises the light intensity function, detmining the grey level or colour
- What is the Nyquist rate?
    - The minimum sampling rate required to avoid aliasing and undersampling - 2x the highest frequency

## Aliasing and Anti-Aliasing

- What is aliasing?
    - When two signal become indistinguishable when sampled, this leads to artifacts in the image.
- How can anti-aliasing be achieved?
    - Applying a low pass filter
- What is the purpose of anti-aliasing?
    - Smooths out high frequency signals before sampling, minimising aliasing artifacts

## Re-Sampling and Re-Sizing

- What is the difference between down-sampling and up-sampling?
    - Down-sampling reduces the image size by summarising pixel values (pick one, mean, weighted mean)
    - Up-sampling increases the image size by interpolating pixel values from known values (interpolation)

## Re-Quantisation

- What is the purpose of re-quantisation?
    - To reduce the number of grey levels in an image, reducing the amount of data required to store the image
- How can this be done?
    - Dividing each pixel value by a constant
- What are the side affects of doing this?
    - Can't increase grey level resolution of a single pixel
