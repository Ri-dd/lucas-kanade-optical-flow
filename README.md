# Lucas–Kanade Sparse Optical Flow

A Python implementation of the **Lucas–Kanade Sparse Optical Flow** algorithm from scratch using **NumPy** and **OpenCV**. The project tracks sparse feature points across consecutive video frames by estimating pixel motion through image gradients and solving the optical flow equations.

---

## Features

- Implemented the Lucas–Kanade optical flow algorithm from scratch
- Computes spatial and temporal image gradients manually
- Solves optical flow using least-squares estimation
- Includes iterative refinement with multi-level neighborhood processing
- Eigenvalue-based feature quality validation
- Tracks Shi-Tomasi corner features across video frames
- Real-time visualization of tracked feature trajectories

---

## Algorithm Overview

The implementation follows the classical Lucas–Kanade approach:

1. Detect strong corner features using the Shi-Tomasi detector.
2. Compute image gradients:
   - Horizontal gradient (Ix)
   - Vertical gradient (Iy)
   - Temporal gradient (It)
3. Construct the optical flow system:

   ```
   M · V = N
   ```

4. Solve for the motion vector using matrix inversion.
5. Validate solutions using determinant and eigenvalue checks.
6. Refine estimates through iterative neighborhood processing.
7. Draw tracked feature trajectories on the video.

---

## Project Structure

```
.
├── lukas.py          # Lucas–Kanade implementation
├── main.py           # Video processing and visualization
├── README.md
└── sample_video.mp4  # Input video (user provided)
```

---

## Technologies Used

- Python
- NumPy
- OpenCV

---

## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/LK-sparse-optical-flow.git
cd LK-sparse-optical-flow
```

Install dependencies:

```bash
pip install numpy opencv-python
```

---

## Usage

Update the video path inside `main.py` if required.

Run:

```bash
python main.py
```

Press **Q** to quit the visualization window.

---

## Implementation Details

The project includes custom implementations for:

- Image gradient computation
- Least-squares motion estimation
- Matrix inversion
- Eigenvalue-based feature validation
- Multi-level neighborhood refinement
- Sparse feature tracking

OpenCV is used only for:

- Reading video frames
- Detecting Shi-Tomasi corners
- Displaying tracking results

---

## Sample Output

The output visualizes:

- Red circles representing tracked feature points
- Green trajectories showing feature motion across frames

---

## Learning Outcomes

This project demonstrates practical implementation of:

- Optical Flow
- Computer Vision
- Linear Algebra
- Least Squares Optimization
- Image Processing
- Feature Tracking

---

## References

- Lucas, B. D., & Kanade, T. (1981). *An Iterative Image Registration Technique with an Application to Stereo Vision.*
- OpenCV Documentation
