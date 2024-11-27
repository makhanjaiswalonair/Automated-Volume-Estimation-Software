
Automated Volume Estimation Software
====================================

Overview
--------
This project focuses on automating the volume estimation process for structural components such as beams and columns. It leverages drone-based image acquisition and advanced machine learning models for object detection, segmentation, and dimension extraction. The software addresses inefficiencies in manual volume measurement and enhances scalability and accuracy in construction monitoring.

Features
--------
- Automation: Eliminates the need for manual measurements by automating volume calculations.
- Drone Integration: Supports remote image acquisition using drones.
- Machine Learning: Implements state-of-the-art models for object detection and segmentation:
  - YOLOv8: Object detection.
  - SAM: Segmentation refinement.
  - U-Net: Previously explored segmentation model.
- Real-Time Performance: Optimized for real-time applications using advanced algorithms.
- User-Friendly Workflow: Incorporates UI design, image processing, and volume computation into an intuitive software package.

Problem Statement
-----------------
Manual volume measurement methods are inefficient, prone to error, and lack scalability. This project addresses these challenges by:
1. Automating the measurement process.
2. Minimizing errors through advanced AI techniques.
3. Enhancing scalability with drone-based image acquisition.

Objectives
----------
- Automate volume estimation for structural components.
- Enable remote image acquisition via drones.
- Achieve precise segmentation and volume computation using machine learning models.

Methodology
-----------
1. Image Acquisition: Drones capture images of structural components with specific orientation requirements.
2. Object Detection: Use YOLOv8 for identifying beams and columns.
3. Segmentation: Refine detections with SAM for accurate volume calculations.
4. Volume Estimation: Compute dimensions and volumes based on segmented images.

Implementation Tools
--------------------
- UI Design: Qt Designer
- Image Processing: OpenCV
- Packaging: PyInstaller

Results
-------
- Achieved accurate detection and segmentation of rectangular columns and beams.
- Reduced errors with high-resolution images.
- Balanced computational cost for real-time applications.

Comparison of Methods
---------------------
| Method                 | Description                                    | Benefits                       | Limitations                         |
|------------------------|-----------------------------------------------|--------------------------------|-------------------------------------|
| findContours (OpenCV)  | Detects object boundaries.                   | Simple and fast.               | Sensitive to noise; struggles with complex shapes. |
| CNN-Based Bounding Box | Predicts bounding boxes for objects.         | Good for clean objects.        | Limited handling of multi-object scenes. |
| U-Net for Segmentation | Pixel-level segmentation for dimensions.     | High precision.                | Slower for large datasets.         |
| YOLOv8 + SAM           | Combines detection and segmentation.          | High accuracy.                 | High computational cost.            |

Challenges
----------
- Dependency on image quality for accurate measurements.
- Limited detection capabilities for irregular shapes.
- Computational costs for large-scale real-time deployment.

Future Work
-----------
1. Expand detection capabilities to include diverse structural shapes.
2. Optimize the software for large-scale applications.
3. Minimize user dependency for reference dimensions.

Getting Started
---------------
Prerequisites:
- Python 3.8 or higher
- Required Python libraries: opencv-python, torch, numpy, pyqt5
- Compatible drone setup for image acquisition

Installation:
1. Clone this repository:
   ```
   git clone <repository-link>
   cd automated-volume-estimation
   ```
2. Install dependencies:
   ```
   pip install -r requirements.txt
   ```
3. Run the software:
   ```
   python main.py
   ```

Contributors
------------
- Makhan Jaiswal  
  Department of Civil Engineering, IIT Delhi  
  Supervisor: Prof. Sahil Garg  

License
-------
This project is licensed under the MIT License. See the LICENSE file for details.
