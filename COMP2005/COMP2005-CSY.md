# COMP2005 - Compression Systems

## Compression

- Why is compression used?
    - Images can be large
    - Lots of images can take up lots of space
- When can compression be useful?
    - Automated image gathering
    - Data size restrictions

## Types of Redundancy

### Coding Redundancy

- What is coding redundancy?
    -

### Spatial Redundancy

- What is spatial redundancy?
    - Neighbouring pixels have similar values
    - Compression usually involves pixel grouping or transformation
- What method can be used for spatial redundancy?
    - Run-length encoding

### Psychovisual Redundancy

- What is psychovisual redundancy?
    - The human eye can't see all the detail in an image
    - Some grey level and colour differences are imperceptible
- What is the goal of psychovisual redundancy?
    - Not modify the image visually whilst still compressing

## Structure of Compression Systems

### Symbol Coder (Coding Redundancy)

- What is a symbol coder?
    - A method of encoding symbols
    - Assigns the shortest code to the most frequently occuring output values
    - Reversible

### Mapper (Spatial Redundancy)

- What is a Mapper?
    - Transforms input data to facilitate compression
    - Reduces interpixel redundancies
    - Reversible

### Quantiser (Psychovisual Redundancy)

- What is a Quantiser?
    - Reduces the number of grey levels or colours in an image
    - Irreversible


## Components and Complete Schemes
