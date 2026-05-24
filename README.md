# ColorX - Colorful Image Colorization

[![Python](https://img.shields.io/badge/Python-3.12-blue?style=flat-square&logo=python)](https://www.python.org/)
[![OpenCV](https://img.shields.io/badge/OpenCV-4.x-green?style=flat-square&logo=opencv)](https://opencv.org/)
[![NumPy](https://img.shields.io/badge/NumPy-1.x-blueviolet?style=flat-square&logo=numpy)](https://numpy.org/)

**[Command-Line Interface for Automatic Image Colorization]**

---

## 📋 About the Project

**ColorX** is a command-line interface (CLI) application that performs automatic colorization on grayscale photographs. Based on the deep neural network architecture and original research by **Richard Zhang**, the system utilizes OpenCV's DNN module to load and execute a pre-trained Caffe model. The algorithm treats colorization as a classification task and employs class-rebalancing to map color channels, producing vibrant and realistic results within the CIELAB color space.

## 🚀 Installation

### Prerequisites
* Python 3.12+
* `pip` package manager

### 1: Clone the Repository
```bash
git clone <your-repository-url>
cd ColorX
```

### 2: Install Dependencies
```bash
pip install numpy opencv-python
```

### 3: Set Up Model Files
Due to GitHub's file size limitations, the pre-trained model is not included in this repository and must be downloaded manually.

1. Download the model file from the link below:
   * [Download colorization_release_v2.caffemodel (123 MB)](https://www.dropbox.com/s/dx0qvhhp5hbcx7z/colorization_release_v2.caffemodel?dl=1)
2. Move the downloaded file into 'Model' folder.

The final directory structure must look exactly like this:
```text
ColorX/
├── model/
│   ├── colorization_deploy_v2.prototxt
│   ├── pts_in_hull.npy
│   └── colorization_release_v2.caffemodel
└── colorize.py
```
*(Note: Ensure you adjust the `DIR` variable inside `colorize.py` to reflect the correct absolute or relative path of your local environment if any path resolution errors occur).*

---

## 💻 Usage

### Run Colorization via Terminal
Open your terminal or Command Prompt (CMD) inside the root folder of the project and execute the script, passing the path to the target image as an argument:

```bash
python colorize.py --image samples/X.jpg
```
*Replace `samples/X.jpg` with the actual path of the grayscale image you wish to test.*

---

## 📄 License and Credits
This project is a practical implementation based on the original research architecture and publication by **Richard Zhang, Phillip Isola, and Alexei A. Efros**. Developed strictly for technical demonstration, educational purposes, and software engineering portfolio development.
