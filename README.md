# Glove-Helmet-Detection-YoloV4-Darknet
YoloV4 Darknet Model can easily detect humans wearing safety Gloves and Helmets at Work Place.
This Deep Learning model has been trained on 800 gloves + 800 Helmet image datasets on Darknet + YoloV4 architecture.
Such models can be used for a variety of applications which are not limited to security, industrial safety and monitoring.

## 1. Image Source

* Images were collected from [Google Open Image Dataset](https://storage.googleapis.com/openimages/web/index.html)
* Dependent folders and Files used in Codes on [Google Drive](https://drive.google.com/drive/folders/1WXq05wOYd6pf9LU0DCi2eVLl6xsPaB-C?usp=sharing)

## 2. Deep Learning Model

### a. Training
* Install Darknet on Google Colab first.
* Training of the model on YOLOv4.

### b. YoloV4 Traning Details
* Pretrained Weights for initialization = yolov4.conv.137
* Main Configs from yolov4-obj.cfg.

                * learning_rate=0.001
                * batch=32
                * subdivisions=16
                * steps=3200,3600
                * max_batches = 4000
                * Classes = 02
                * Fliter = 21
### c. Weights of YOLOv4 trained on Glove & Helmet Dataset: yolov4_train_final.weights 

## 3. Inference

* You can run model inference or detection on image/video.

Command for image:
`!./darknet detector test data/Glove_Helmet/image_data.data cfg/yolov4_train.cfg /currdrive/YOLO_V4/darknet/backup/yolov4_train_last.weights /currdrive/YOLO_V4/darknet/data/test_data/Worker.jpg -thresh 0.3`

Output image:

![Worker1](https://user-images.githubusercontent.com/38158849/98509312-fc5f5400-2286-11eb-9a07-7ab30a1aa8b4.jpg)

Command for Video:
`!./darknet detector demo data/Glove_Helmet/image_data.data cfg/yolov4_train.cfg /currdrive/YOLO_V4/darknet/backup/yolov4_train_last.weights /currdrive/YOLO_V4/darknet/data/test_data/Workers_dance2.mp4 -out_filename result3.mp4 -ext_output -dont_show`

Output Video:
[![Fifth Harmony song](http://img.youtube.com/vi/q6YMFKUJukY/0.jpg)](http://www.youtube.com/watch?v=q6YMFKUJukY)



## 4. Suggestions to improve Performance

* Use more Training Data.
* Use more Data Augmentation for Training Data.
* Train with larger network-resolution by setting your .cfg-file (height=640 and width=640) (any value multiple of 32).
* For Detection use even larger network-resolution like 864x864.
* Try YOLOv5 or any other Object Detection Algorithms like SSD, Faster-RCNN, RetinaNet, etc. as they are very good as of now (year 2020).

Follow me On [Linkedin](https://www.linkedin.com/in/nikhil-singh-9a5324b4/)

