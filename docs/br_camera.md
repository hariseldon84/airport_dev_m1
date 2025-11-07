# Camera & Imaging System Specification (br_camera)

## 1. Overview
This document details the camera and image processing architecture for the Airport Business Smartphone. The system is engineered to deliver professional-grade, true-to-life imagery with a focus on clarity, color accuracy, and utility for business applications. Our philosophy is "Computational Truth"—leveraging advanced processing to capture reality, not to create artificial-looking images.

## 2. Rear Camera System: Clarity Pro Array
The rear camera is a versatile, triple-lens system designed to excel in a wide range of professional scenarios, from documenting worksites to capturing high-quality marketing materials.

### 2.1 Main (Wide) Camera
- **Sensor**: 50MP Sony LYT-900 1-inch sensor.
- **Pixel Size**: 1.6μm (3.2μm with 4-in-1 pixel binning).
- **Lens**: 8-element aspherical lens with Zeiss T* anti-reflective coating.
- **Aperture**: Variable aperture, mechanically switching between f/1.6 (for low light and depth of field) and f/4.0 (for maximum sharpness in landscapes and documents).
- **Stabilization**: Sensor-shift Optical Image Stabilization (OIS) for superior stability in photos and videos.
- **Autofocus**: All-pixel autofocus for instantaneous and accurate focusing.

### 2.2 Ultrawide Camera
- **Sensor**: 50MP Sony IMX890 1/1.56-inch sensor.
- **Lens**: 120° field of view with a freeform lens design to minimize distortion at the edges.
- **Aperture**: f/2.2.
- **Autofocus**: Includes autofocus, enabling a high-resolution Macro Mode for capturing details from as close as 2.5cm.

### 2.3 Periscope Telephoto Camera
- **Sensor**: 50MP Sony IMX858 1/2.51-inch sensor.
- **Optical Zoom**: 5x optical zoom (equivalent to a 120mm focal length).
- **Stabilization**: Barrel OIS.
- **Aperture**: f/2.8.
- **Functionality**: Ideal for capturing details from a distance, such as text on a presentation screen or architectural details.

### 2.4 Supporting Hardware
- **LiDAR Scanner**: Emits a grid of infrared dots for instant, accurate autofocus in low-light conditions and for 3D scanning applications.
- **Multi-Spectrum Color Sensor**: Measures ambient light color and temperature to ensure perfect white balance and color accuracy in all conditions.
- **Flicker Sensor**: Eliminates banding and artifacts when shooting under artificial lighting.

## 3. Front Camera: True-Presence System
- **Sensor**: 32MP sensor with autofocus.
- **Technology**: Next-generation Under-Display Camera (UDC). The display above the camera uses a transparent pixel pattern and advanced AI algorithms to eliminate haze and artifacts, providing a truly uninterrupted screen while delivering clear, high-quality video for conferencing.
- **Aperture**: f/2.0.
- **Functionality**: Optimized for video conferencing with features like auto-framing and background blur processed by the BeeHive AI.

## 4. Image Processing: The Clarity Engine
Our imaging advantage comes from a dual-processor approach to image processing.

### 4.1 Dual ISP Architecture
- **Primary ISP**: The Qualcomm Spectra ISP on the Snapdragon 8 Gen 5 handles the initial image capture, RAW data processing, and standard tasks like autofocus and auto-exposure.
- **Dedicated Image Co-Processor**: A dedicated portion of the **Airport Hive-Core A1** AI Co-Processor is designated as the **Clarity Engine**. This engine runs advanced computational photography models on the RAW data from the ISP.

### 4.2 Clarity Engine Features
- **Semantic Segmentation**: The AI identifies up to 16 different object types within a scene (e.g., sky, skin, text, foliage, buildings) and applies tailored enhancements to each segment individually for a perfectly balanced and natural-looking final image.
- **Pro-Grade Color Science**: The color pipeline is tuned for natural, true-to-life colors, avoiding the oversaturated look of consumer phones. It supports 10-bit color depth and professional color spaces (Rec. 2020).
- **Document & Whiteboard Mode**: A key business feature. When the camera detects a document or whiteboard, it automatically switches to a high-contrast mode, corrects perspective, removes shadows and glare, and enhances text sharpness to produce a perfect, ready-to-share scan.

## 5. Professional Video Capabilities
- **Resolution & Frame Rates**: 8K at 30fps, 4K at 120fps.
- **Pro Video Mode**: Full manual control over video settings and support for LOG and RAW video formats for professional color grading.
- **AI-Powered Video**: The BeeHive AI enables real-time video bokeh for conferencing, advanced video stabilization (fusing OIS and EIS data), and intelligent noise cancellation for clear audio.

## 6. Next Steps
1. Procure sensor and lens prototypes for testing and characterization.
2. Develop the custom tuning for the Spectra ISP.
3. Train the neural network models for the Clarity Engine, with a focus on the Document & Whiteboard Mode.
4. Design the UI/UX for the camera application, ensuring easy access to both simple and professional controls.
