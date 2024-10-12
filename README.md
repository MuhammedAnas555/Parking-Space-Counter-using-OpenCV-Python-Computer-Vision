# Parking Space Picker

This project is a computer vision-based solution to detect available parking spaces from a video feed or image of a parking lot. It uses OpenCV for image processing and employs Python for parking space detection logic.

## Features

- Detects parking spaces from a static video feed or image.
- Highlights occupied and free parking spaces with different colors.
- Dynamically updates the availability of parking spaces in real-time.
- Provides a customizable threshold for space detection using trackbars.
- Saves and loads parking space positions for easy reuse.

## Installation

### Prerequisites

Ensure you have the following dependencies installed:

- Python 3.x
- OpenCV (`cv2`)
- Numpy
- Cvzone (for easy rectangle and text handling)
- Pickle (for saving/loading parking space positions)

To install the required dependencies, run:

```bash
pip install opencv-python numpy cvzone
```

### Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/ParkingSpacePicker.git
   ```

2. Navigate to the project directory:

   ```bash
   cd ParkingSpacePicker
   ```

3. Ensure your parking video or image is properly set up in the project folder.

4. Place the initial positions of the parking spaces in the `CarParkPos` file using the `ParkingSpacePicker.py` script.

5. Run the `main.py` script to start detecting parking spaces in real-time from the video feed.

## Usage

### 1. Parking Space Picker Script (`ParkingSpacePicker.py`)

This script allows you to select and save the positions of parking spaces on a parking lot image. Use left-click to mark new spaces, and right-click to remove existing ones.

```bash
python ParkingSpacePicker.py
```

### 2. Main Detection Script (`main.py`)

The main script loads the parking positions from the saved file and detects occupied and available parking spaces from a video feed.

```bash
python main.py
```

### 3. Main Script with Trackbars (`main.py` with Trackbars)

This version of the main script allows you to fine-tune the image processing parameters via trackbars, giving more control over the detection process.

```bash
python main.py --trackbars
```

## How It Works

1. **Parking Space Picker**: Allows the user to manually select parking spaces by clicking on an image of the parking lot. These positions are saved in a `pickle` file (`CarParkPos`), so they can be reused later.
  
2. **Detection Algorithm**: The video feed is processed frame by frame to detect parking spaces. The spaces are highlighted in green if they are available, and in red if they are occupied.

3. **Trackbars**: Provide a way to adjust thresholds for image processing on the fly, ensuring better accuracy in varying lighting conditions.

## File Structure

- `ParkingSpacePicker.py`: Allows manual selection and saving of parking positions.
- `main.py`: Detects parking spaces in real-time from a video feed.
- `main.py (with Trackbars)`: Adds trackbars for fine-tuning detection.
- `CarParkPos`: A saved file containing the positions of parking spaces.
- `carPark.mp4`: A video feed of the parking lot.
- `carParkImg.png`: A reference image of the parking lot.

## Video Demonstration

A demonstration of the parking space detection can be found in `carPark.mp4`.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

