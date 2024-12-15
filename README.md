# Train Model for Self-Driving Car

This project uses the Udacity self-driving car simulator to collect training data and implement autonomous driving using deep learning.

## Overview

The project consists of two main phases:
1. Data Collection using Training Mode
2. Autonomous Driving using Trained Model

## Prerequisites

- Python 3.7+
- [Udacity Self-Driving Car Simulator](https://github.com/udacity/self-driving-car-sim.git)
- Required Python packages (see requirements.txt)

## Installation

1. Clone this repository:
```bash
git clone [<your-repo-url>](https://github.com/osamaalschame/Train-model-for-Self-Driving-Car.git)
cd Train-model-for-Self-Driving-Car
```



3. Download and install the Udacity simulator from:
   https://github.com/udacity/self-driving-car-sim.git

## Project Structure

```
Train-model-for-Self-Driving-Car/
├── drive.py           # Data collection script
├── train.py          # Model training script
├── model.h5          # Trained model (after training)
├── data/             # Collected training data
│   ├── IMG/          # Training images
│   └── driving_log.csv  # Steering angles data
└── README.md
```

## Usage

### 1. Data Collection (Training Mode)

1. Launch the simulator in Training Mode
2. Run the data collection script:
```bash
python drive.py
```
3. Drive the car in the simulator to collect training data
4. The script will save:
   - Images in the `data/IMG` directory
   - Steering angles in `data/driving_log.csv`

### 2. Model Training

After collecting data, train the model using:
```bash
python train.py
```

This will:
- Load the collected images and steering angles
- Train the neural network
- Save the trained model as `model.h5`

### 3. Autonomous Mode

1. Launch the simulator in Autonomous Mode
2. Run the trained model:
```bash
python drive.py model.h5
```



## Training Data

The training data includes:
- Center camera images
- Left camera images
- Right camera images
- Corresponding steering angles

## Performance Tips

1. Collect diverse training data:
   - Multiple laps
   - Recovery scenarios
   - Different lighting conditions

2. Data augmentation techniques:
   - Flipping images
   - Adjusting brightness
   - Adding shadows

## Troubleshooting

- If the car veers off track: Collect more recovery data
- If steering is too aggressive: Adjust steering angle correction factor
- If model isn't learning: Check data distribution and augmentation

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## Acknowledgments

- Based on the [Udacity Self-Driving Car Simulator](https://github.com/udacity/self-driving-car-sim.git)
- Inspired by end-to-end deep learning for self-driving cars


