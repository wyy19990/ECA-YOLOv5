# 面向海事巡航场景的ECA-Yolov5
# ECA Yolov5 for Maritime Cruise Scenarios

------



## Performance
| Model                                                                                                | size<br><sup>(pixels) | mAP<sup>val<br>0.5:0.95 | mAP<sup>val<br>0.5 | Speed<br><sup>CPU b1<br>(ms) | Speed<br><sup>V100 b1<br>(ms) | Speed<br><sup>V100 b32<br>(ms) | params<br><sup>(M) | FLOPs<br><sup>@640 (B) | Weights
|------------------------------------------------------------------------------------------------------|-----------------------|-------------------------|--------------------|------------------------------|-------------------------------|--------------------------------|--------------------|------------------------|------------------------|
| YOLOv5n                   | 640                   | 28.0                    | 45.7               | **45**                       | **6.3**                       | **0.6**                        | **1.9**            | **4.5**                | [YOLOv5n](https://github.com/ultralytics/yolov5/releases/download/v6.1/yolov5n.pt)
| YOLOv5s                   | 640                   | 37.4                    | 56.8               | 98                           | 6.4                           | 0.9                            | 7.2                | 16.5                   | [YOLOv5s](https://github.com/ultralytics/yolov5/releases/download/v6.1/yolov5s.pt)
| YOLOv5m                   | 640                   | 45.4                    | 64.1               | 224                          | 8.2                           | 1.7                            | 21.2               | 49.0                   | [YOLOv5m](https://github.com/ultralytics/yolov5/releases/download/v6.1/yolov5m.pt)
| YOLOv5l                   | 640                   | 49.0                    | 67.3               | 430                          | 10.1                          | 2.7                            | 46.5               | 109.1                  | [YOLOv5l](https://github.com/ultralytics/yolov5/releases/download/v6.1/yolov5l.pt)
| YOLOv5x                   | 640                   | 50.7                    | 68.9               | 766                          | 12.1                          | 4.8                            | 86.7               | 205.7                  | [YOLOv5x](https://github.com/ultralytics/yolov5/releases/download/v6.1/yolov5x.pt)
|                                                                                                      |                       |                         |                    |                              |                               |                                |                    |                        |
| YOLOv5n6                 | 1280                  | 36.0                    | 54.4               | 153                          | 8.1                           | 2.1                            | 3.2                | 4.6                    |[YOLOv5n6](https://github.com/ultralytics/yolov5/releases/download/v6.1/yolov5n6.pt)
| YOLOv5s6                 | 1280                  | 44.8                    | 63.7               | 385                          | 8.2                           | 3.6                            | 12.6               | 16.8                   |[YOLOv5s6](https://github.com/ultralytics/yolov5/releases/download/v6.1/yolov5s6.pt)
| YOLOv5m6                 | 1280                  | 51.3                    | 69.3               | 887                          | 11.1                          | 6.8                            | 35.7               | 50.0                   |[YOLOv5m6](https://github.com/ultralytics/yolov5/releases/download/v6.1/yolov5m6.pt)
| YOLOv5l6                 | 1280                  | 53.7                    | 71.3               | 1784                         | 15.8                          | 10.5                           | 76.8               | 111.4                  |[YOLOv5l6](https://github.com/ultralytics/yolov5/releases/download/v6.1/yolov5l6.pt)
| YOLOv5x6<br>+ TTA | 1280<br>1536          | 55.0<br>**55.8**        | 72.7<br>**72.7**   | 3136<br>-                    | 26.2<br>-                     | 19.4<br>-                      | 140.7<br>-         | 209.8<br>-             |[YOLOv5x6](https://github.com/ultralytics/yolov5/releases/download/v6.1/yolov5x6.pt)


 <details><summary> <b>SPP Structure Parameter and GFLOPs</b> </summary>

| Model         | 参数量(parameters) | 计算量(GFLOPs) |
| ------------- | ------------------ | -------------- |
| SPP           | 7225885            | 16.5           |
| SPPF          | 7235389            | 16.5           |
| SimSPPF       | 7235389            | 16.5           |
| ASPP          | 15485725           | 23.1           |
| BasicRFB      | 7895421            | 17.1           |
| SPPCSPC       | 13663549           | 21.7           |
| SPPCSPC_group | 8355133            | 17.4           |

</details>

<details><summary> <b>Others Structure Parameter and GFLOPs</b> </summary>

| Model         | 参数量(parameters) | 计算量(GFLOPs) |
| ------------- | ------------------ | -------------- |
| TransposeConv upsampling| 7241917            | 16.6           |
| InceptionConv | 7233597            | 16.2           |
| BiFPN         | 7384006            | 17.2           |
| ShuffleNetv2  | 3844193            | 8.1            |
| CARAFE        | 7369445            | 17.0           |
</details>




<details><summary> <b>Update log</b> </summary>
2022.8.22 yolo.py Add Chinese annotations🍀

2022.8.24 Add Demo of Pyqt page🍀
</details>

<details><summary> <b>Acknowledgements</b> </summary>
https://github.com/ultralytics/yolov5
</details>
