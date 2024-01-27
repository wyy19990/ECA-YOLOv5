# 面向海事巡航场景的ECA-Yolov5
# ECA Yolov5 for Maritime Cruise Scenarios



## Performance
|  Model             	|  Precision    	|  Recall     	|   mAP(iou=0.5) 	|
|:--------------------------------------------------------------------------------------------------------------------------:	|:-------------------------------------------:	|:-----------------------------------------------------------------------------------------:	|:--------------------------------------------------------------------------------------------:	|
|   YOLOv4 	|  78.3 	|  65.6 	|  64.1 	|
|   YOLOv5 	|  84.7 	|  76.1 	|  79.0 	|
|   YOLOv6 	|  86.5 	|  75.8 	|  80.1 	|
|   YOLOx 	|  86.6 	|  68.2 	|  79.4 	|
|   YOLOv7  	| 85.3  	|  77.3 	|  80.9 	|
|   ECA-YOLOv5-EIOU 	|  85.9 	|  77.4 	|  81.1 	|





## <div>How to use</div>
<details open>
<summary>Install</summary>

[**Python>=3.6.0**](https://www.python.org/) is required with all
[requirements.txt](https://github.com/ppogg/YOLOv5-Lite/blob/master/requirements.txt) installed including
[**PyTorch>=1.7**](https://pytorch.org/get-started/locally/):
<!-- $ sudo apt update && apt install -y libgl1-mesa-glx libsm6 libxext6 libxrender-dev -->

```bash
$ git clone https://github.com/wyy19990/ECA-YOLOv5
$ cd ECA-YOLOv5
$ pip install -r requirements.txt
```

</details>

<details>
<summary>Inference with detect.py</summary>
  `detect.py` runs inference on a variety of sources, downloading models automatically from
the [latest ECA-YOLOv5 release](https://github.com/wyy19990/ECA-YOLOv5/releases) and saving results to `runs/detect`.

```bash
$ python detect.py --source 0  # webcam
                            file.jpg  # image 
                            file.mp4  # video
                            path/  # directory
                            path/*.jpg  # glob
                            'https://youtu.be/NUsoVlDFqZg'  # YouTube
                            'rtsp://example.com/media.mp4'  # RTSP, RTMP, HTTP stream
```

</details>

<details open>
<summary>Training</summary>

```bash
$ python train.py --data boat.yaml --cfg ECA-yolov5.yaml --weights best.pt --batch-size 64
```
</details>

<details open>
<summary>DataSet</summary>

Training set and test set distribution （the path with xx.jpg）
  
 ```bash
train: ../coco/images/train2017/
val: ../coco/images/val2017/
```
```bash
├── images            # xx.jpg example
│   ├── train2017        
│   │   ├── 000001.jpg
│   │   ├── 000002.jpg
│   │   └── 000003.jpg
│   └── val2017         
│       ├── 100001.jpg
│       ├── 100002.jpg
│       └── 100003.jpg
└── labels             # xx.txt example      
    ├── train2017       
    │   ├── 000001.txt
    │   ├── 000002.txt
    │   └── 000003.txt
    └── val2017         
        ├── 100001.txt
        ├── 100002.txt
        └── 100003.txt
```
  
</details> 

<details><summary> <b>Acknowledgements</b> </summary>
https://github.com/ultralytics/yolov5
</details>


