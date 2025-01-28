# 📸 Image Processing and Edge Detection

This repository contains **image processing techniques**, including **Canny Edge Detection, Image Smoothing, and Fourier Transform Noise Removal**, implemented as part of **Computer Vision Assignment 1**.

---

## 📌 Features
- **Canny Edge Detector**: Implemented from scratch and compared with OpenCV's built-in function.
- **Image Smoothing**: Applied **average, Gaussian, and median filtering** on `cameraman.jpeg`.
- **Fourier Transform for Noise Removal**: Used **2D FFT** to analyze and remove noise from `bandnoise.png`.

---

## 🛠 Implementation Details
### 1️⃣ Canny Edge Detector
Implemented **Canny Edge Detection** in the following steps:
1. **Gaussian Smoothing** - Removes noise.
2. **Gradient Calculation** - Computes edges.
3. **Non-Maximum Suppression** - Sharpens edge detection.
4. **Double Threshold and Hysteresis** - Filters weak edges.

The output is compared against OpenCV's `cv2.Canny()` implementation.

---

### 2️⃣ Image Filtering and Smoothing
Applied **three different filters** on `cameraman.jpeg`:
- **Average Blur** (9x9 and 25x25 kernel)
- **Gaussian Blur** (σ = 2.0, σ = 15)
- **Median Filter** (5x5 and 15x15 kernel)

**Resized images** to compare the effects of filtering on different scales.

---

### 3️⃣ Fourier Transform for Noise Removal
- Computed **2D Discrete Fourier Transform (DFT)** on `bandnoise.png`.
- Identified **frequency domain noise patterns**.
- Designed and applied a **custom filter** to remove noise.
- Displayed all results in a **matplotlib subplot**.

### 📊 Results
#### Canny Edge Detection Comparison
- Custom Implementation vs. OpenCV's cv2.Canny().
#### - Observations:
        - Both methods successfully detect edges, but parameter tuning impacts performance.
### Effect of Different Filters
- Gaussian blur provides better smoothing compared to average and median filters.
- Increasing the kernel size makes the image smoother but reduces detail.

### Noise Removal using Fourier Transform
- The FFT visualization shows a distinct noise pattern in bandnoise.png.
- Custom filtering significantly improves image clarity.
