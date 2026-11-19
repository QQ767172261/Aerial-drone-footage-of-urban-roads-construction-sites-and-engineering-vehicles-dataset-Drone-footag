航拍无人机城市道路空中俯拍影像施工现场以及工程车辆数据集![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/811701939f724f1aaf7529416757551e.png)

数据采集：DJI M4E![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/8358dc6201de4f61bbf82849150e16dc.png)

数据类型：原始图片+XML标签+TXT标签
总内存大小：5.8G（2743张图片）
图片分辨率：3840*2160
采集高度：40～120m
采集角度：0~90°
类别：共2类，包括：施工现场、工程车辆![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/bcfc45925d0e4040976206491fa9ef6d.png)


用于城市道路空中俯拍影像施工场地、工程车辆等低空目标检测等低空目标检测领域

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/b8de59a264b8405887e8c76ea6d54384.png)

# 无人机城市道路俯拍施工现场及工程车辆数据集![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/87563cb2f5be4745bd28e3081da9b12b.png)

|项目|详情|
| ---- | ---- |
|数据集名称|无人机城市道路空中俯拍影像施工现场以及工程车辆数据集|
|总图像数量|2743张|
|文件大小|5.8G|
|采集设备|DJI M4E|
|分辨率|3840*2160|
|标注格式|原始图片 + XML标签 + TXT标签（YOLO、VOC检测标注）|
|采集高度|40～120m|
|采集角度|0~90°|
|类别数量|2类|

### 类别明细![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/8c8eff4e381648f6a3b349437485f6a5.png)

|类别|中文名称|
| ---- | ---- |
|construction_site|施工现场|
|engineering_vehicle|工程车辆|

### 应用价值![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/24fc1b9bf82f4646aeb19241a216e30e.png)

城市道路航拍巡检、工地占道识别、工程车辆管控、违规施工监测，适合低空无人机目标检测模型训练，辅助城建、交管自动化巡查。![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/382a8f33a57b418da9ef374b7019e787.png)


```python
# YOLOv11 检测训练脚本
from ultralytics import YOLO

if __name__ == '__main__':
    model = YOLO("yolov11n.pt")
    model.train(
        data="road_construction.yaml",
        epochs=80,
        imgsz=640,
        batch=8,
        device=0
    )
```

