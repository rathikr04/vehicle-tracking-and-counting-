# Vehicle Tracking and Counting System

## CODTECH Internship - Task 2 (Data Science)

### Objective
To build a computer vision system that automatically detects, tracks and counts vehicles from a traffic video in real-time.

### Technologies Used
- **Language:** Python 3
- **Library:** OpenCV, NumPy
- **Technique:** Background Subtraction (MOG2)

### How It Works
1.  **Background Subtraction:** Uses `cv2.createBackgroundSubtractorMOG2()` to separate moving vehicles from static road background.
2.  **Noise Removal:** Applies thresholding, morphological closing and dilation to clean the mask and remove shadows/small noise.
3.  **Vehicle Detection:** Finds contours of moving objects. Filters by minimum width/height (80x80) to avoid detecting humans/bikes as noise.
4.  **Counting Logic:** A virtual green line is drawn at Y=500. When the center of a detected vehicle crosses this line (+- 6 pixel offset), the total counter increases by 1.
5.  **Display:** Shows bounding boxes around vehicles, center points, counting line and total count on screen.

### Project Structure
