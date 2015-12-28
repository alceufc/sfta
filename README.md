# SFTA Texture Extractor

This Matlab code extracts texture features from an image using the SFTA (Segmentation-based Fractal Texture Analysis) algorithm. To extract features, use the `sfta(I, nt)` function, where `I` corresponds to the input grayscale image and `nt` is a parameter that defines the size of the feature vector.

The features are returned as a 1 by (6*nt - 3) vector.

Example:

```
I = imread('coins.png'); 
D = sfta(I, 4)
```

## Brief description of the SFTA algorithm

The extraction algorithm consists in decomposing the input image into a set of binary images from which the fractal dimensions of the resulting regions are computed in order to describe segmented texture patterns.

Publication where the SFTA algorithm is described:

> Costa, A. F., G. E. Humpire-Mamani, A. J. M. Traina. 2012. "An Efficient Algorithm for Fractal Analysis of Textures." In SIBGRAPI 2012 (XXV Conference on Graphics, Patterns and Images), 39-46, Ouro Preto, Brazil.

I also wrote a [blog post](http://alceufc.blogspot.com/2013/09/texture-classification.html) showing how SFTA can be used to classify textures.