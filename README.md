# Canny-Edge-Detection-Using-OpenCV

## Reference Number: 212225230118
## Developed by: Joshna.M

## Aim
To implement the Canny Edge Detection algorithm on a sample image using Python and OpenCV to obtain the edges.

## Introduction

Canny Edge Detection is an image processing technique used to detect important edges in an image.

It helps identify boundaries of objects by detecting areas where the intensity of the image changes significantly.

## Requirements

* Python
* OpenCV
* Matplotlib
* Jupyter Notebook

## Program

```python
import cv2
import matplotlib.pyplot as plt

# Read the image
image = cv2.imread("parrot.jpg")

# Convert to grayscale
gray = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Apply Canny Edge Detection
edges = cv2.Canny(gray, 100, 200)

# Display the edges
plt.imshow(edges, cmap="gray")
plt.title("Canny Edge Detection")
plt.axis("off")
plt.show()
```

## Parameter Comparison

```python
edges1 = cv2.Canny(gray, 100, 200)
edges2 = cv2.Canny(gray, 50, 150)

plt.figure(figsize=(10, 4))

plt.subplot(1, 2, 1)
plt.imshow(edges1, cmap="gray")
plt.title("Threshold: 100, 200")
plt.axis("off")

plt.subplot(1, 2, 2)
plt.imshow(edges2, cmap="gray")
plt.title("Threshold: 50, 150")
plt.axis("off")

plt.show()
```

## Discussion

The Canny algorithm detects the boundaries of objects in the image.

Different threshold values produce different results:

* Lower threshold values detect more edges, including weaker edges.
* Higher threshold values detect fewer but stronger edges.
* Very low thresholds may also detect unwanted noise.
* Choosing suitable threshold values gives clearer and more useful edges.

## Result

The Canny Edge Detection algorithm was successfully implemented using OpenCV. The edges of objects were detected from the sample image, and the effect of different threshold values was observed.

## Files

* `Canny_Edge_Detection.ipynb` – Jupyter Notebook containing the Python program.
* `parrot.jpg` – Sample input image.
* `README.md` – Experiment details and explanation.
