# InsightfulEyes-Object-detection-for-the-Visually-impaired
InsightfulEyes : Empowering visually impaired individuals with Object detection technology . Enhancing independance and accessibility through innovative AI solutions . 

# YOLOv4 OpenCV DNN

Run YOLOv4 directly with OpenCV using the DNN module.



## Index

1. [Clone the repository](#Clone-the-repository)
2. [Install pip packages](#Install-pip-packages)
3. [Run the code](#Run-the-code)

## Clone the repository

 clone the repository

```sh
# Using HTTPS
git clone https://github.com/aj-ames/YOLOv4-OpenCV-DNN.git
# Using SSH
git clone git@github.com:aj-ames/YOLOv4-OpenCV-DNN.git
```

Finally, enable lfs and pull the yolo weights

```sh
git lfs install
git lfs pull
```

## Install pip packages

First, we need to install python dependencies. Make sure you have a working build of python3.7/3.8

```sh
pip install python3-dev python3-pip
```

The dependencies needed are the following:

```sh
numpy==1.19.4
opencv-contrib-python==4.5.1.48
opencv-python==4.5.1.48
```

You can either install them with pip command or use the requirements.txt file.

```sh
# For individial packages
pip3 install <packagename>

# For requirements.txt
pip3 install -r requirements.txt
```

## Running the code

The code supports a number of command line arguments. Use help to see all supported arguments

```sh
❯ python3 dnn_inference.py --help

usage: dnn_inference.py [-h] [--image IMAGE] [--stream STREAM] [--cfg CFG] [--weights WEIGHTS] [--namesfile NAMESFILE] [--input_size INPUT_SIZE]

Object Detection using YOLOv4 and OpenCV4

optional arguments:
  -h, --help            show this help message and exit
  --image IMAGE         Path to use images
  --stream STREAM       Path to use video stream
  --cfg CFG             Path to cfg to use
  --weights WEIGHTS     Path to weights to use
  --namesfile NAMESFILE
                        Path to names to use
  --input_size INPUT_SIZE
                        Input size
```

To pass an image, run the script in the following way:

```sh
python3 dnn_infernece.py --image images/example.jpg
```

To run a stream, run the script this way:

```sh
# Video
python3 dnn_inference.py --stream video.mp4

# RTSP
python3 dnn_inference.py --stream rtsp://192.168.1.1:554/stream

# Webcam
python3 dnn_inference.py --stream webcam
```
