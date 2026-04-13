# 🎨 Cartoon Effect with OpenCV

A simple Python script that turns any image into a cartoon-style drawing using OpenCV.

## How It Works

The script processes an image through these steps:

1. **Greyscale** – Converts the image to greyscale
2. **Blur** – Applies a median blur to reduce noise
3. **Edge Detection** – Uses a Laplacian filter to detect edges
4. **Thresholding** – Turns edges into a clean black-and-white mask
5. **Bilateral Filter** – Smooths the original image while keeping colors vivid (runs 10 times)
6. **Final Cartoon** – Combines the smoothed image with the edge mask to produce the cartoon effect

## Requirements

- Python 3.x
- OpenCV
- NumPy

Install dependencies with:

```bash
pip install opencv-python numpy
```

## Usage

1. Place your image in the same folder as the script and name it `cvPedropPascal.jpg`  
   *(or change the filename in the script to match yours)*

2. Run the script:

```bash
python cartoon.py
```

3. A window will pop up for each step — press **any key** to move to the next one.

## Output Preview

| Step | Description |
|------|-------------|
| Greyscale | Black & white version of the image |
| Blurred | Noise-reduced greyscale |
| Laplacian | Raw edge map |
| Threshold | Clean edge mask |
| Bilateral | Smoothed color image |
| **Cartoon** | ✅ Final cartoon result |

## Notes

- The script displays each intermediate step so you can see how the effect builds up.
- You can tweak the `bilateralFilter` parameters or the threshold value (`25`) to adjust the cartoon style.
