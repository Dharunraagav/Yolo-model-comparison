# Pest Detection Dataset Model Comparison

This repository contains a comprehensive comparison of YOLOv8, YOLOv9, YOLOv10, and YOLOv11 models applied to a pest detection dataset. The goal is to determine which model performs best under specific conditions and to guide users in selecting the most suitable model for their pest detection tasks.

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Models](#models)
- [Results](#results)
- [How to Use](#how-to-use)
- [Contributing](#contributing)
- [License](#license)

## Overview

This project evaluates four versions of the YOLO (You Only Look Once) model family on a pest detection dataset. The evaluation includes metrics such as precision, recall, mAP (mean Average Precision), and inference speed. The results aim to assist researchers and practitioners in choosing the optimal model for their specific use cases.

## Dataset

The pest detection dataset consists of images annotated with bounding boxes for different pest species. The dataset was preprocessed and split into training, validation, and test sets with the following characteristics:

- **Training Set**: X images
- **Validation Set**: Y images
- **Test Set**: Z images

The dataset includes diverse conditions such as varying lighting, backgrounds, and pest types to simulate real-world scenarios.

## Models

We compared the following YOLO models:


- **YOLOv9**: Improved accuracy at the cost of slightly slower inference. [View Details](#)
  - [F1 Score Graph](Results/yolov9_F1_curve.png)
  - [Precision-Recall Curve](Results/yolov9_PR_curve.png)
  - [Results Curve](Results/yolov9_results.png)
  - [Inference Images](Results/yolov9_latency.jpg)

- **YOLOv10**: Focuses on high precision with more complex architecture. [View Details](#)
  - [F1 Score Graph](Results/yolov10_F1_curve.png)
  - [Precision-Recall Curve](Results/yolov10_PR_curve.png)
  - [Results Curve](Results/yolov10_results.png)
  - [Inference Images](Results/yolov10_latency.jpg)

- **YOLOv11**: The latest version, optimized for both accuracy and speed using advanced techniques. [View Details](#)
  - [F1 Score Graph](Results/yolov11_F1_curve.png)
  - [Precision-Recall Curve](Results/yolo11_PR_curve.png)
  - [Results Curve](Results/yolov11_results.png)
  - [Inference Images](Results/yolov11_latency.jpg)
### Configuration

Each model was trained with the following hyperparameters:

- **Batch Size**: 16
- **Epochs**: 50
- **Learning Rate**: 0.001
- **Input Size**: 640x640 pixels

## Results

The results of the evaluation are summarized below:

| Model   | Precision | Recall | mAP\@50 | Inference Speed (ms) |
| ------- | --------- | ------ | ------- | -------------------- |
| YOLOv8  | 85.6%     | 83.2%  | 84.4%   | 15                   |
| YOLOv9  | 88.3%     | 85.0%  | 86.6%   | 18                   |
| YOLOv10 | 90.1%     | 87.8%  | 89.0%   | 25                   |
| YOLOv11 | 91.5%     | 89.3%  | 90.4%   | 20                   |

### Key Observations

- **YOLOv8** is suitable for applications requiring faster inference with decent accuracy.
- **YOLOv9** provides a good balance between accuracy and speed.
- **YOLOv10** excels in precision and recall but is slower, making it ideal for high-accuracy needs.
- **YOLOv11** achieves the best overall performance with moderate speed.

## How to Use

### Clone the Repository

```bash
git clone [https://github.com/yourusername/pest-detection-model-comparison.git]
cd pest-detection-model-comparison
```

### Install Dependencies

Ensure you have Python 3.8+ and install the required libraries:


```

### Run Evaluation

To run the evaluation script for a specific model:

```bash
python evaluate.py --model yolov8 --dataset path/to/dataset
```

Replace `yolov8` with `yolov9`, `yolov10`, or `yolov11` for other models.

### View Results

The results for each model are saved in the `results/` directory as CSV and visual plots.

## Contributing

We welcome contributions! Please open an issue or submit a pull request if you have:

- Suggestions for improving the evaluation.
- New models or techniques to compare.
- Bug fixes or code optimizations.

## License

This project is licensed under the [MIT License](LICENSE).

