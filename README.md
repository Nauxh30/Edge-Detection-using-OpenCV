# 🖼️ Edge Detection using OpenCV

This project demonstrates edge detection techniques using Python, OpenCV, and Matplotlib in a Jupyter Notebook (`.ipynb`).

Edge detection is an important image processing technique used to identify object boundaries and important features within an image.

---

# 📌 Features

- Read and display images using OpenCV
- Convert images from BGR to RGB
- Convert images to grayscale
- Perform edge detection using OpenCV
- Visualize edge-detected output using Matplotlib
- Handle image loading errors

---

# 🛠️ Technologies Used

- Python
- OpenCV
- Matplotlib
- NumPy
- Jupyter Notebook

---

# 📂 Project Workflow

1. Load the input image
2. Convert image color format
3. Convert image to grayscale
4. Apply edge detection
5. Display the processed image

---

# 📦 Required Libraries

Install the required libraries before running the notebook:

```bash
pip install opencv-python matplotlib numpy
```

---

# 💻 Sample Python Code

```python
import cv2
import matplotlib.pyplot as plt

# Read image
image = cv2.imread('download.jpg')

# Check if image loaded correctly
if image is not None:

    # Convert BGR to RGB
    image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

    # Convert to grayscale
    gray = cv2.cvtColor(image, cv2.COLOR_RGB2GRAY)

    # Apply edge detection
    edges = cv2.Canny(gray, 100, 200)

    # Display edge-detected image
    plt.imshow(edges, cmap='gray')
    plt.title("Edge Detection")
    plt.axis("off")
    plt.show()

else:
    print("Error: Image not found or failed to load.")
```

---

# ▶️ How to Run

1. Open the Jupyter Notebook
2. Run all cells step by step
3. Ensure the image file exists in the project folder
4. Observe the edge-detected output image

---

# ⚠️ Common Error

## Error

```python
error: (-215:Assertion failed) !_src.empty() in function 'cv::cvtColor'
```

## Cause

The image was not loaded properly using `cv2.imread()`.

## Fix

- Check whether the image path is correct
- Ensure the image exists in the folder
- Verify the image filename

---

# ✅ Output

The notebook successfully:

- Reads the input image
- Converts the image to grayscale
- Detects edges using OpenCV
- Displays the processed output using Matplotlib

---

# 🌟 Learning Outcomes

Through this project, we learn:

- Basics of edge detection
- Image preprocessing techniques
- Grayscale conversion
- OpenCV image operations
- Visualization using Matplotlib
- Error handling in image processing

---

# 🚀 Future Improvements

- Add Sobel edge detection
- Add Laplacian edge detection
- Real-time webcam edge detection
- Implement image filtering before detection
- Add object recognition

---

