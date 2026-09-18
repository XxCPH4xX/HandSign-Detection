# HandSign-Detection

Real-time hand sign language detection using OpenCV, MediaPipe, and deep learning. Detects American Sign Language letters **I, L, O, V, E, U** from webcam input in real-time.

## Features

- **Real-time detection** - Live webcam hand sign recognition
- **Data collection** - Capture custom hand sign training data
- **Deep learning model** - Keras/TensorFlow classification model
- **Preprocessing** - Automatic hand cropping and normalization

## Tech Stack

- Python
- OpenCV
- MediaPipe (via cvzone)
- TensorFlow/Keras
- NumPy

## Project Structure

```
HandSign-Detection/
├── Data Collection.py    # Script to collect hand sign training data
├── Testing.py            # Real-time hand sign detection & classification
├── Data/                 # Training data organized by class (I, L, O, V, E, U)
├── Model/
│   ├── keras_model.h5    # Pre-trained Keras model
│   └── labels.txt        # Class labels
└── .idea/                # IDE config
```

## Quick Start

```bash
# Install dependencies
pip install opencv-python cvzone numpy tensorflow

# Collect training data (press 's' to save frames)
python "Data Collection.py"

# Run real-time detection
python Testing.py
```

## How It Works

1. **Data Collection** - Uses MediaPipe to detect hands via webcam, crops the hand region, resizes to 300x300, and saves labeled images
2. **Training** - Model trained on collected data using Keras (saved as `keras_model.h5`)
3. **Testing** - Real-time inference: detects hand, preprocesses frame, classifies with trained model, and overlays prediction on screen

## Labels

| Index | Sign |
|-------|------|
| 0 | I |
| 1 | L |
| 2 | O |
| 3 | V |
| 4 | E |
| 5 | U |

## License

MIT
