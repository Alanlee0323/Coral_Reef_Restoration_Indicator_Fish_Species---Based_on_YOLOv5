---
layout: post
title: Object Detection
author: [ALAN_LEE]
---
# Coral_Reef_Restoration_Indicator_Fish_Species---Based_on_YOLOv5
---
## Image Annotation
---
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
![P4-2021-09-24-12-00 mp4_001023 400](https://github.com/Alanlee0323/Coral_Reef_Restoration_Indicator_Fish_Species---Based_on_YOLOv5/assets/95911604/b46d0388-9353-48db-a9d4-5bb39ced4f78)
![P4-2021-09-24-12-00 mp4_001023 400](https://github.com/Alanlee0323/Coral_Reef_Restoration_Indicator_Fish_Species---Based_on_YOLOv5/assets/95911604/7a455642-1e1e-4f54-bfed-55201a77ee88)
![P1-2021-09-23-12-00 mp4_000731 769](https://github.com/Alanlee0323/Coral_Reef_Restoration_Indicator_Fish_Species---Based_on_YOLOv5/assets/95911604/6c56843b-1f94-487c-a1d2-3d7a64d7a5bb)
![2022-06-14-0630-0700_視長 mp4_20220728_115850 457](https://github.com/Alanlee0323/Coral_Reef_Restoration_Indicator_Fish_Species---Based_on_YOLOv5/assets/95911604/06b458cd-4742-4042-b8a8-3ad23eac892e)

</details>

<details open>
<summary>Training</summary>


```bash
python train.py --data FIsh/Coral_Reef_Restoration_Indicator_Fish_Species --epochs 200 --weights '' --cfg yolov5m.yaml  --batch-size 128
```

![](https://github.com/Alanlee0323/Coral_Reef_Restoration_Indicator_Fish_Species---Based_on_YOLOv5/assets/95911604/ecdd3916-e81a-43c6-b631-056827ca9e0a)

</details>

