Shape Detection App
A computer vision application that automatically detects and classifies geometric shapes in images using OpenCV and Gradio.
Features

Automatic Shape Detection: Identifies triangles, squares, rectangles, and circles
Real-time Processing: Instant results when you upload an image
Visual Feedback: Draws contours and labels on detected shapes
Detailed Analysis: Provides shape count, vertices, area, and position information
User-friendly Interface: Clean and intuitive Gradio web interface

How it Works

Image Processing: Converts uploaded image to grayscale and applies Gaussian blur
Edge Detection: Uses Canny edge detection to find shape boundaries
Contour Analysis: Finds and analyzes contours in the image
Shape Classification: Determines shape type based on number of vertices:

3 vertices → Triangle
4 vertices → Square (if ratio ≈ 1) or Rectangle


6 vertices → Circle





Usage

Upload an image containing geometric shapes
The app will automatically process and detect shapes
View the annotated result with detected shapes highlighted
Check the summary for detailed information about each detected shape

Technical Details

Minimum Shape Size: 500 pixels area (filters out noise)
Edge Detection: Canny algorithm with thresholds 50-150
Approximation: Contour approximation with 2% epsilon
Square Detection: Width/height ratio between 0.95-1.05

Requirements

Python 3.8+
OpenCV
Gradio
NumPy
Pillow

Local Development
bashpip install -r requirements.txt
python app.py
The app will be available at http://localhost:7860
License
MIT License
