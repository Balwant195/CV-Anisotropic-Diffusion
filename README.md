# Anisotropic Diffusion for Image Processing and Computer Vision

This repository contains an implementation of anisotropic diffusion, also known as Perona-Malik filtering. This technique is essential in computer vision for reducing noise in images while preserving important details such as edges and textures.

## Features

- Efficient image smoothing that maintains edge integrity
- Customizable parameters: diffusion coefficient, iterations, and more
- Robust handling of image boundaries
- Easy integration into computer vision workflows

## Applications

- **Edge Detection**: Enhance edges to improve object detection and segmentation.
- **Image Denoising**: Remove noise while preserving structural details.
- **Preprocessing**: Prepare images for feature extraction, object recognition, and other analysis tasks.

## Acknowledgments

This implementation was developed as part of a computer vision course taught at the Indian Statistical Institute by Professor Pradipta Maji, Professor at the Machine Intelligence Unit, Indian Statistical Institute, Kolkata, located at 203 B. T. Road, Kolkata 700108, India, from August 2022 to December 2022.

## Usage

Example usage of the anisotropic diffusion function:

```python
import numpy as np
import matplotlib.pyplot as plt
from skimage import data, img_as_float
from anisotropic_diffusion import anisotropic_diffusion

image = img_as_float(data.camera())
diffused_image = anisotropic_diffusion(image, num_iterations=10, kappa=50, lamda=0.25)

fig, (ax1, ax2) = plt.subplots(1, 2, figsize=(12, 6))
ax1.imshow(image, cmap='gray')
ax1.set_title('Original Image')
ax1.axis('off')

ax2.imshow(diffused_image, cmap='gray')
ax2.set_title('Diffused Image')
ax2.axis('off')

plt.show()
```

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE) - see the LICENSE file for details.
