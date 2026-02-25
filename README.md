# FaceDetectCV

A lightweight OpenCV project for **real-time face detection** in both static images and webcam video streams using a Haar Cascade classifier.

## Project Overview

FaceDetectCV demonstrates a classic computer vision workflow:

- Load a pre-trained Haar Cascade model (`haarcascade_frontalface_default.xml`)
- Convert frames/images to grayscale
- Detect faces with `detectMultiScale(...)`
- Draw bounding boxes around detected faces
- Visualize results in an OpenCV window

This is a simple, beginner-friendly starter repository for developers who want to understand face detection basics before moving on to deep learning-based approaches.

## Features

- Face detection from a single image
- Face detection from live webcam feed
- Uses OpenCV's built-in Haar Cascade model
- Minimal dependencies and easy setup

## Repository Structure

```text
.
├── detect_face_image.py                # Detect faces in an image
├── detect_face_video.py                # Detect faces in webcam stream
├── haarcascade_frontalface_default.xml # Pre-trained Haar Cascade model
├── requirements.txt                    # Python dependencies
├── fac_recog.jpg                       # Example image asset
├── pic2.jpeg                           # Example image asset
└── README.md
```

## Requirements

- Python 3.8+
- Webcam (for `detect_face_video.py`)
- OS with GUI support for OpenCV windows (`cv2.imshow`)

Install dependencies:

```bash
pip install -r requirements.txt
```

> Note: `requirements.txt` currently pins older OpenCV/Numpy versions. If installation fails on modern Python versions, consider upgrading those pins.

## Usage

### 1) Detect faces in an image

```bash
python detect_face_image.py
```

By default, `detect_face_image.py` reads a hardcoded image file:

```python
img = cv2.imread('maaya_img.jpg')
```

Update this path to one of your own images (or an existing file in this repo) before running.

### 2) Detect faces in live webcam video

```bash
python detect_face_video.py
```

Controls:

- Press `Esc` to close the video window and stop the program.

## How It Works

Both scripts follow the same detection pipeline:

1. Initialize the Haar Cascade classifier
2. Read image/frame input
3. Convert input to grayscale
4. Run `face_cascade.detectMultiScale(gray, 1.1, 4)`
5. Draw rectangles around detections
6. Display output

## Limitations

- Haar Cascades are fast but less robust than modern deep learning detectors
- Detection quality can drop in poor lighting, occlusion, or extreme face angles
- Current scripts are minimal and use hardcoded file/webcam inputs

## Suggested Improvements

- Add CLI arguments for input image/video path
- Save output image/video to disk
- Add confidence filtering and configurable parameters
- Add support for processing video files
- Upgrade dependencies for modern Python compatibility
- Add unit/integration tests

## GitHub Metadata Suggestions

If you are publishing this repository, you can use:

**Repository description**

> Face detection in images and live webcam streams using OpenCV Haar Cascades (Python).

**Suggested GitHub topics**

- `opencv`
- `computer-vision`
- `face-detection`
- `python`
- `haar-cascade`
- `realtime-detection`
- `webcam`
- `image-processing`

## License

No license file is currently included. Add a `LICENSE` file (for example MIT) before open-source distribution.
