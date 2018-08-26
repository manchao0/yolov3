<img src="https://storage.googleapis.com/ultralytics/UltralyticsLogoName1000×676.png" width="200">  

# Introduction

This directory contains software developed by Ultralytics LLC. For more information on Ultralytics projects please visit:
http://www.ultralytics.com  

# Description

The https://github.com/ultralytics/yolov3 repo contains code to train YOLOv3 on the COCO dataset: https://cocodataset.org/#home. Credit to P.J. Reddie for YOLO (https://pjreddie.com/darknet/yolo/) and to Erik Lindernoren for the pytorch implementation this repo is based on (https://github.com/eriklindernoren/PyTorch-YOLOv3).

# Requirements

Python 3.6 or later with the following `pip3 install -U -r requirements.txt` packages:

- `numpy`
- `torch`
- `opencv-python`

# Running

Run `train.py` to begin training. Each epoch trains on 120,000 images from the train and validate sets, and validates on 5000 images in the validation set. An Nvidia GTX 1080 Ti will run about 16 epochs per day. Loss plots for the bounding boxes, objectness and class confidence should appear similar to results shown here.
![Alt](https://github.com/ultralytics/yolov3/blob/master/data/xview_training_loss.png "training loss")

Checkpoints will be saved in `/checkpoints` directory. Run `detect.py` to apply trained weights to an image, such as `zidane.jpg` from the `data/samples` folder, shown here.
![Alt](https://github.com/ultralytics/yolov3/blob/master/data/zidane_result.jpg "example")

Run `test.py` to test the latest checkpoint on the 5000 validation images. Joseph Redmon's official YOLOv3 weights produce a mAP of .581 using this method, compared to .579 in his paper.

# Contact

For questions or comments please contact Glenn Jocher at glenn.jocher@ultralytics.com or visit us at http://www.ultralytics.com/contact