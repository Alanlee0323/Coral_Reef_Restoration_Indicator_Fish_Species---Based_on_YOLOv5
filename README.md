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

<details>
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
<details>
<summary>Training</summary>

The commands below reproduce YOLOv5 [COCO](https://github.com/ultralytics/yolov5/blob/master/data/scripts/get_coco.sh)
results. [Models](https://github.com/ultralytics/yolov5/tree/master/models)
and [datasets](https://github.com/ultralytics/yolov5/tree/master/data) download automatically from the latest
YOLOv5 [release](https://github.com/ultralytics/yolov5/releases). Training times for YOLOv5n/s/m/l/x are
1/2/4/6/8 days on a V100 GPU ([Multi-GPU](https://docs.ultralytics.com/yolov5/tutorials/multi_gpu_training) times faster). Use the
largest `--batch-size` possible, or pass `--batch-size -1` for
YOLOv5 [AutoBatch](https://github.com/ultralytics/yolov5/pull/5092). Batch sizes shown for V100-16GB.

```bash
python train.py --data coco.yaml --epochs 300 --weights '' --cfg yolov5n.yaml  --batch-size 128
                                                                 yolov5s                    64
                                                                 yolov5m                    40
                                                                 yolov5l                    24
                                                                 yolov5x                    16
```

<img width="800" src="https://user-images.githubusercontent.com/26833433/90222759-949d8800-ddc1-11ea-9fa1-1c97eed2b963.png">

</details>

<details open>
