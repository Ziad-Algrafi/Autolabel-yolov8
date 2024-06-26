![output](https://github.com/Ziad-Algrafi/ODLabel/assets/117011801/0bf8f35d-5337-4ee4-b694-5c957fe25992)

<div align="center">
   
# ODLabel

[![PyPI version](https://badge.fury.io/py/odlabel.svg)](https://badge.fury.io/py/odlabel)
[![Python Version](https://img.shields.io/badge/python-3.9%2B-blue)](https://www.python.org/downloads/)
[![License: AGPL v3](https://img.shields.io/badge/License-AGPL%20v3-blue.svg)](https://www.gnu.org/licenses/agpl-3.0)

</div>

ODLabel (Open Dictionary Labeler) is a powerful tool for zero-shot object detection, labeling and visualization. It provides an intuitive graphical user interface for labeling objects in images using the YOLO-World model and supports various output formats such as YOLO, COCO, CSV, and XML.

## Features

- Select a YOLO-World model for object detection
- Choose an images folder for labeling
- Specify output directory for annotated data
- Define object categories for detection
- Use Slicing Adaptive Inference (SAHI) for improved detection for small objects
- Select device type (CPU or GPU) for inference
- Customize train/validation split ratio
- Adjust confidence level and non-maximum suppression (IoU) threshold
- Visualize input image statistics and output detection results

## Installation

### PyTorch Version

To install the PyTorch version of ODLabel, run the following command:

```bash
pip install odlabel

```

### ONNX Version

To install the ONNX version of ODLabel, run the following command:

```bash
pip install odlabel-onnx

```

## Usage

To launch the PyTorch version of ODLabel application, run the following command:

```bash
odlabel

```

To launch the ONNX version of ODLabel application, run the following command:

```bash
odlabel-onnx

```

1. Select a YOLO-World model file based on your installation for object detection.
2. Choose the folder containing the images you want to label.
3. Specify the output directory where the labeled data will be saved.
4. Enter the object categories you want to detect, separated by commas.
5. Configure additional options such as SAHI, device type, output format, train/validation split, confidence level, and NMS threshold.
6. Click the "Start" button to begin the labeling process.
7. Monitor the progress and view the detection results in the application.

## Pytroch Model

| Model Type      | mAP  | mAP50 | mAP75 | Model                                                                                         |
| --------------- | ---- | ----- | ----- | --------------------------------------------------------------------------------------------- |
| yolov8s-worldv2 | 37.7 | 52.2  | 41.0  | [Download](https://github.com/ultralytics/assets/releases/download/v8.2.0/yolov8s-worldv2.pt) |
| yolov8m-worldv2 | 43.0 | 58.4  | 46.8  | [Download](https://github.com/ultralytics/assets/releases/download/v8.2.0/yolov8m-worldv2.pt) |
| yolov8l-worldv2 | 45.8 | 61.3  | 49.8  | [Download](https://github.com/ultralytics/assets/releases/download/v8.2.0/yolov8l-worldv2.pt) |
| yolov8x-worldv2 | 47.1 | 62.8  | 51.4  | [Download](https://github.com/ultralytics/assets/releases/download/v8.2.0/yolov8x-worldv2.pt) |

## ONNX Models

| Model Type      | mAP  | mAP50 | mAP75 | Model                                                                                              |
| --------------- | ---- | ----- | ----- | -------------------------------------------------------------------------------------------------- |
| yolov8s-worldv2 | 37.7 | 52.2  | 41.0  | [Download](https://github.com/Ziad-Algrafi/ODLabel/raw/main/assets/yolov8s-worldv2.onnx?download=) |
| yolov8m-worldv2 | 43.0 | 58.4  | 46.8  | [Download](https://github.com/Ziad-Algrafi/ODLabel/raw/main/assets/yolov8m-worldv2.onnx?download=) |
| yolov8l-worldv2 | 45.8 | 61.3  | 49.8  | [Download](https://github.com/Ziad-Algrafi/ODLabel/raw/main/assets/yolov8l-worldv2.onnx?download=) |
| yolov8x-worldv2 | 47.1 | 62.8  | 51.4  | [Download](https://github.com/Ziad-Algrafi/ODLabel/raw/main/assets/yolov8x-worldv2.onnx?download=) |

## GUI Figures and Dashboard

ODLabel provides a comprehensive dashboard with various figures and visualizations to assist in analyzing the input image data and object detection results. The dashboard is displayed within the graphical user interface (GUI) of the application, allowing for interactive exploration and understanding of the data.

The following figures are available in the dashboard:

1. **Format and Instances Chart:** This chart combines two visualizations in one figure:

   - A bar chart displaying the total number of input images.
   - A bar chart showing the distribution of image file formats (e.g., .jpg, .jpeg, .png, jfif).

2. **Image Resolution Distribution:** A histogram that illustrates the distribution of image resolutions across the input dataset. The x-axis represents the image width, and the bars show the frequency of images within each resolution bin.

3. **Image Quality:** A bar chart depicting the number of images falling into different quality categories:

   - Blurred images
   - Grayscale images
   - Black and white images
   - Corrupted or invalid images

4. **Color Space Distribution:** A 3D scatter plot that visualizes the color space distribution of the input images. Each point in the plot represents a unique color space, with its position determined by the mean values of the red, green, and blue channels. The size of the points indicates the frequency of that particular color space in the dataset.

5. **Detected Object Count:** A bar chart displaying the count of detected objects for each class. The first bar represents the total number of input images, while the subsequent bars show the number of instances for each object class detected across the dataset.

6. **Detection Confidence Histogram:** A histogram that illustrates the distribution of detection confidence scores. The x-axis represents the confidence level, and the bars show the frequency of detections within each confidence bin.

7. **Spatial Distribution of Objects:** A chart that visualizes the bounding boxes of detected objects. Each bounding box is represented by a rectangle, with the color intensity indicating the degree of overlap with other bounding boxes. Areas with darker colors signify a higher concentration of overlapping bounding boxes.

8. **Heatmap of Detection:** A heatmap visualization that showcases the spatial distribution of detected objects within the image space. The heatmap uses different colors to indicate the density of detections at various locations, with brighter colors representing higher concentrations.

These figures provide valuable insights into the input image data and the object detection results, enabling users to identify potential issues, patterns, and areas for further analysis or improvement. The dashboard serves as a powerful tool for exploring and understanding the data, facilitating informed decision-making and enhancing the overall object detection and labeling workflow.

## Upgrade

You can upgrade PyTorch version of ODLabel using pip:

```bash
pip install --upgrade odlabel

```

You can upgrade ONNX version of ODLabel using pip:

```bash
pip install --upgrade odlabel-onnx

```

## License

This project is licensed under the GNU Affero General Public License v3.0 (AGPL-3.0). See the [LICENSE](LICENSE) file for details.

## Contributing

We welcome contributions! Please read our [Code of Conduct](CONTRIBUTING.md#code-of-conduct) and follow the [contribution guidelines](CONTRIBUTING.md#how-to-contribute) when submitting issues or pull requests.

## Acknowledgements

ODLabel is built using the following open-source libraries:

- [CustomTkinter](https://github.com/TomSchimansky/CustomTkinter)
- [Ultralytics YOLO](https://github.com/ultralytics/ultralytics)
- [Matplotlib](https://matplotlib.org)
- [OpenCV](https://opencv.org)
- [PyTorch](https://pytorch.org)
- [ONNX](https://onnxruntime.ai)

- ODLabel runs locally on your machine and does not collect or send any data externally. Your data remains private and secure within your local environment.
- We extend our gratitude to [AILab-CVC](https://github.com/AILab-CVC) for generously open-sourcing their model.

## Contact

For any questions or inquiries, please contact the maintainer at - ZiadAlgrafi@gmail.com.
