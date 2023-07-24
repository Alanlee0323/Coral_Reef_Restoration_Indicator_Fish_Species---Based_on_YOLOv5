---
layout: post
title: Object Detection
author: [ALAN_LEE]
---
# Coral_Reef_Restoration_Indicator_Fish_Species---Based_on_YOLOv5

The quantity of indicator species in coral reefs is a critical reference for coral surveys. However, manual calculation requires a significant amount of human resources and time. Therefore, utilizing artificial intelligence for automated classification and counting is of utmost importance. The objective of this study is to achieve an accuracy of over 85% in correctly identifying common designated indicator fish species (Parrotfish, Snappers, Butterflyfish, Groupers, and Wrasses) in the Northeastern coastline. Additionally, the accuracy for other fish species should be above 80%. This approach not only reduces the training time for identification personnel but also enables continuous monitoring, potentially allowing for real-time surveillance 24 hours a day.

<br>

## Description
This research employs the YOLOv5 algorithm for fish species recognition. The development environment is set up on Anaconda, using Python 3.7 as the programming language, and deep learning is performed using PyTorch 1.2 + CUDA 10.0 as the framework. Training is conducted on the Taiwan AI Cloud Computing (TWCC) server. Transfer Learning is employed during the training process, utilizing the YOLOv5 provided pre-trained weights 'yolov5m.pt' . This approach accelerates the training efficiency and safeguards against weight corruption.

<br>

## Environment
<ul>
<li>python = 3.7.0</li>
<li>CUDA = 10.0</li>
<li>Pytorch =1.2</li>
</ul>

<br>

## Image Annotation
### [LabelImg](https://github.com/tzutalin/labelImg)
![](https://github.com/Alanlee0323/Coral_Reef_Restoration_Indicator_Fish_Species---Based_on_YOLOv5/assets/95911604/a8599b43-b508-48e2-96fb-989e50f5adca)

`$pip install labelImg`<br>

---
### Annotation formats
* YOLO format in .txt
**class_num x, y, w, h**<br>
```
0 0.5222826086956521 0.5518115942028986 0.025 0.010869565217391304
0 0.5271739130434783 0.5057971014492754 0.013043478260869565 0.004347826086956522
```
<br>

## Requirements

<details open>
<summary>Install</summary>

```bash
git clone https://github.com/Alanlee0323/Coral_Reef_Restoration_Indicator_Fish_Species---Based_on_YOLOv5  # clone
cd Coral_Reef_Restoration_Indicator_Fish_Species---Based_on_YOLOv5
pip install -r requirements.txt  # install
```
</details>

<details open>
<summary>Inference with detect.py</summary>

`detect.py` runs inference on a variety of sources, and saving results to `runs/detect`.

```bash
python detect.py --weights Original_Imgsize_1280_batchsize_16_epoch_200_models_yolov5m.pt --source 0                               # webcam
                                               img.jpg                         # image
                                               vid.mp4                         # video
                                               screen                          # screenshot
                                               path/                           # directory
                                               list.txt                        # list of images
                                               list.streams                    # list of streams
                                               'path/*.jpg'                    # glob
                                               'https://youtu.be/Zgi9g1ksQHc'  # YouTube
                                               'rtsp://example.com/media.mp4'  # RTSP, RTMP, HTTP stream
```
![P3-2021-10-05-08-00 mp4_000056 000](https://github.com/Alanlee0323/Coral_Reef_Restoration_Indicator_Fish_Species---Based_on_YOLOv5/assets/95911604/48ed7f44-3f46-46dd-b363-b33118f5b472)
![P4-2021-09-24-12-00 mp4_001023 400](https://github.com/Alanlee0323/Coral_Reef_Restoration_Indicator_Fish_Species---Based_on_YOLOv5/assets/95911604/7a455642-1e1e-4f54-bfed-55201a77ee88)
![P1-2021-09-23-12-00 mp4_000731 769](https://github.com/Alanlee0323/Coral_Reef_Restoration_Indicator_Fish_Species---Based_on_YOLOv5/assets/95911604/6c56843b-1f94-487c-a1d2-3d7a64d7a5bb)
![2022-06-14-0630-0700_視長 mp4_20220728_115850 457](https://github.com/Alanlee0323/Coral_Reef_Restoration_Indicator_Fish_Species---Based_on_YOLOv5/assets/95911604/06b458cd-4742-4042-b8a8-3ad23eac892e)
![P3-2021-10-03-07-00 mp4_002731 001](https://github.com/Alanlee0323/Coral_Reef_Restoration_Indicator_Fish_Species---Based_on_YOLOv5/assets/95911604/0823e509-b9f5-474a-aa0d-2d40b53b515a)


</details>

<details open>
<summary>Training</summary>


```bash
python train.py --data FIsh/Coral_Reef_Restoration_Indicator_Fish_Species --epochs 200 --cfg ./models/yolov5s.yaml --weights weights/yolov5m.pt  --batch-size 32
```

![](https://github.com/Alanlee0323/Coral_Reef_Restoration_Indicator_Fish_Species---Based_on_YOLOv5/assets/95911604/ecdd3916-e81a-43c6-b631-056827ca9e0a)

</details>



## Acknowledgements
NSTC-110-2634-F-019 -002 -
