Cartooning an Image using OpenCV
This project demonstrates how to transform a regular photograph into a cartoon-like image using a combination of image processing techniques. By applying median filtering for noise reduction, color quantization using K-Means clustering, and edge detection for feature enhancement, we achieve a stylized, cartoon-like rendition of the original image.

Features
Color Quantization with K-Means: Reduce the image’s color palette to a specified number of colors, resulting in a posterized effect.
Median Filtering: Smooths the image and reduces noise before the clustering step.
Edge Detection: Uses Canny edge detection combined with morphological operations to extract and emphasize image contours.
Cartoon Effect: Combines the quantized color image with detected edges, resulting in a cartoon-like appearance.
Project Structure
markdown
Copy code
.
├── README.md
├── requirements.txt
├── cartoon.py
└── Hummingbird.png
cartoon.py: Main script that:
Reads the input image.
Applies median filtering.
Performs K-Means clustering to reduce colors.
Detects and processes edges.
Combines edges with the quantized image to produce a cartooned result.
images: Directory that stores the input image (e.g., Hummingbird.jpg) and can hold additional test images.
Installation
Clone the repository:

bash
Copy code
git clone https://github.com/Krishna2004M/Cartooning-an-Image-using-OpenCV
cd Cartooning-an-Image-using-OpenCV
Create and activate a virtual environment (optional but recommended):

bash
Copy code
python3 -m venv venv
source venv/bin/activate  # For Linux/Mac
# or
venv\Scripts\activate     # For Windows
Install the required dependencies:

bash
Copy code
pip install -r requirements.txt
Usage
Place your input image:

Put your image file (e.g., Hummingbird.jpg) inside the images directory.
Run the script:

bash
Copy code
python cartoon.py --input images/Hummingbird.jpg --output images/Hummingbird_cartoon.png
The script will:
Read Hummingbird.jpg.
Convert it to grayscale and apply median blur.
Perform K-Means clustering for color quantization.
Detect edges and combine them with the quantized image.
Save the resulting cartooned image as Hummingbird_cartoon.png.
Adjust Parameters:

Inside cartoon.py, you can tweak parameters such as numColors for the number of color clusters, Canny thresholds, and the number of iterations for the K-Means algorithm to achieve the desired cartooning effect.
Visualization
The script uses matplotlib to visualize intermediate steps, such as:
Original image
Grayscale and blurred images
Edges (thin and thickened)
Color-quantized image
Final cartoon result
These visualizations help understand the transformation at each stage.

Requirements
Python 3.6+ recommended
See requirements.txt for the list of dependencies.