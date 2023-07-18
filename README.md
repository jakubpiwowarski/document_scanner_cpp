# Document Scanner
This program, scanner_document.cpp, is an implementation of a document scanner using the OpenCV library. It allows users to scan documents and obtain a digitally warped and cropped image.

## Features
- Preprocessing: Converts the input image to grayscale, applies Gaussian blur, and performs Canny edge detection.
- Contour Detection: Identifies the largest contour in the processed image that represents the document.
- Perspective Transformation: Warps the detected document contour to obtain a top-down view.
- Cropping: Removes the outer edges of the warped image to extract the document region.

## Requirements
- C++ compiler
- OpenCV library

## Usage
1. Clone the repository: git clone https://github.com/your-username/document-scanner.git
2. Navigate to the project directory: cd document-scanner
3. Compile the source code: g++ scanner_document.cpp -o scanner_document pkg-config --libs opencv``
4. Run the program: ./scanner_document

## How It Works
1. The program reads the input image and applies preprocessing steps such as grayscale conversion, Gaussian blur, and Canny edge detection.
2. Contours are detected in the processed image, and the largest contour, assumed to represent the document, is identified.
3. The four corners of the document contour are reordered to obtain the correct perspective transformation.
4. The perspective transformation is applied to obtain a top-down view of the document.
5. The outer edges of the warped image are cropped to extract the document region.
6. The original image, the dilated image, the warped image, and the cropped image are displayed.

## Contributing
Contributions are welcome! If you find any issues or have ideas for improvements, please open an issue or submit a pull request.
