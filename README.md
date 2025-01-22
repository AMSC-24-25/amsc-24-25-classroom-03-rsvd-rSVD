# Image Compression
Implementation of Image Compression using the RandomizedSVD algorithm with a GivensRotationQR. The basic idea is to approximate the image matrix with a low-rank matrix using RSVD and store only the significant singular values and vectors.

Main Steps:
1. Load the image as a 2D matrix (for grayscale) or a 3D tensor (for RGB)
2. Preprocessing: normalization of values to (0,1) interval and, if the image si RGB, splitting into three separate matrices.
3. Apply rSVD
4. Compress the data: store the truncated images instead of the full matrix, reducing the memory space required for storing.
5. Postprocessing: rescale the pixel values back to their original range (0, 255) and, for RGB images, combine the three channels again.
6. Save and Display the compressed image.