# ImageNoiseLab

This repository contains the implementation for **Assignment 3** of the **Digital Image Processing** course offered by the Department of Mathematical Sciences, Spring 2025. The assignment focuses on handling salt and pepper noise in images and implementing image compression using Discrete Cosine Transform (DCT).

## Objectives
- Add salt and pepper noise to an image (`lena.png`) with varying noise rates (0.1 to 1.0).
- Implement and compare mean and median filters (3x3, 5x5, 7x7 kernels) using NumPy and OpenCV's built-in functions for noise reduction.
- Apply DCT on 8x8 image blocks, quantize the coefficients, convert to a vector, and decompress using inverse DCT on `realImage.jpg`.
- Provide theoretical explanations for the differences between filter outputs and their effectiveness.

## Repository Structure
- `HW3.ipynb`: Jupyter notebook implementing salt and pepper noise addition, mean and median filters (custom and OpenCV), and visualization of results.
- `HW3_Q2.ipynb`: Jupyter notebook implementing DCT, quantization, matrix-to-vector conversion, and inverse DCT for image compression.
- `lena.png`: Input image for noise and filtering tasks.
- `realImage.jpg`: Input image for DCT compression tasks.
- `README.md`: Project description and setup instructions.

## Technologies Used
- Python 3.x
- OpenCV (`cv2`)
- NumPy
- Matplotlib
- Jupyter Notebook

## Setup Instructions
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/<your-username>/ImageNoiseLab.git
   cd ImageNoiseLab
   ```
2. **Install Dependencies**:
   Ensure Python is installed, then install required libraries:
   ```bash
   pip install opencv-python numpy matplotlib jupyter
   ```
3. **Add Input Images**:
   Ensure `lena.png` and `realImage.jpg` are in the repository root directory.
4. **Run the Notebooks**:
   - Start Jupyter Notebook:
     ```bash
     jupyter notebook
     ```
   - Open and run `HW3.ipynb` for noise and filtering tasks.
   - Open and run `HW3_Q2.ipynb` for DCT compression tasks.
5. **View Results**:
   Output images and plots will be displayed within the Jupyter notebooks.

## Implementation Details
- **Salt and Pepper Noise** (`HW3.ipynb`): Randomly sets pixels to 0 (pepper) or 255 (salt) based on the noise rate using NumPy’s random number generation.
- **Mean Filter** (`HW3.ipynb`): Custom implementation averages pixel values in a kernel (3x3, 5x5, 7x7) with zero padding, compared with OpenCV’s `blur` function.
- **Median Filter** (`HW3.ipynb`): Custom implementation selects the median pixel value in a kernel, compared with OpenCV’s `medianBlur` function.
- **DCT Compression** (`HW3_Q2.ipynb`): Applies DCT on 8x8 blocks, quantizes using a provided matrix, converts to a zigzag vector, and decompresses with inverse DCT using OpenCV’s `dct` and `idct` functions.
- **Theory Questions**: Explanations of filter differences and their effectiveness are included in the notebooks or a separate report.

## Author
- **Name**: [Your Full Name]
- **Student Number**: [Your Student Number]

## Course
- **Digital Image Processing**
- **Department of Mathematical Sciences**
- **Spring 2025**

## Notes
- Ensure `lena.png` and `realImage.jpg` are available in the repository root.
- The code assumes grayscale images for noise and filtering tasks.
- Theoretical explanations for filter differences are documented within the notebooks or a separate report.
