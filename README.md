# OpenCV Motion Detection Security Camera with Auto Recording

A Python/OpenCV security-camera project intended to detect motion from a camera feed and save video when activity is detected.

> **Status:** The repository is currently an unfinished prototype. The checked-in `main.py` does not yet implement motion detection or automatic recording; it contains a face-recognition webcam script instead. This README distinguishes the intended project from the current code so users do not expect features that are not present yet.

## Intended project behavior

The project name suggests a system that will:

- Read video from a webcam or other camera supported by OpenCV.
- Detect movement between video frames.
- Record and save video when motion is detected.
- Keep a log of detected activity.

These features still need to be implemented and verified in the repository.

## Current repository contents

- `main.py` — currently contains a face-recognition example using OpenCV and the `face_recognition` package.
- `motion_log.txt` — a text file in the repository; the current script does not write to it.
- `scanned_output.png` — an image included in the repository.

## Current script requirements

To run the code currently in `main.py`, you need Python 3, a webcam, and these packages:

```bash
python -m pip install opencv-python face_recognition numpy
```

The `face_recognition` package may require additional native dependencies depending on your operating system. The script also expects a local image named `Shiva.jpeg`, which is not included in the repository.

## Run the current prototype

```bash
python main.py
```

The current script is not ready to run as committed: it assigns `image_shiva` but later uses `image_Shiva`, and the reference image is absent. Correct the variable name and provide an image locally before attempting to run it. Press **Q** in the video window to exit once it starts.

## Work needed to match the project name

1. Replace or separate the current face-recognition script from the motion-detection implementation.
2. Add frame-difference or background-subtraction logic to detect motion.
3. Add video recording that starts on motion and stops after a configurable quiet period.
4. Save recordings to a configurable output directory with timestamps.
5. Write motion events to `motion_log.txt` or another documented log format.
6. Add configuration for camera source, sensitivity, recording duration, and output path.
7. Handle unavailable cameras, failed frame reads, and clean shutdown reliably.
8. Add sample output, setup instructions, and a `requirements.txt` file, then test the complete workflow.

## Privacy and responsible use

Use cameras only where you have permission and provide appropriate notice to people being recorded. Protect recorded footage, restrict access, set a retention period, and delete footage when it is no longer needed. Check local rules that apply to video recording and surveillance.

## License

No `LICENSE` file was visible in the repository when this README was prepared. Add a license file if you want to specify how others may use, modify, or distribute the project.
