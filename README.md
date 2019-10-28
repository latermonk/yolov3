#  darknet
https://pjreddie.com/darknet/

##  install darknet
https://pjreddie.com/darknet/install/

## Compiling With CUDA

```
GPU=1
```
## Compiling With OpenCV
```
OPENCV=1
```

#  yolov3
https://pjreddie.com/darknet/yolo/

***You only look once (YOLO)***

You only look once (YOLO) is a state-of-the-art, real-time object detection system.


##  test

```
./darknet detect cfg/yolov3.cfg yolov3.weights data/dog.jpg
```
***equals to :***


```
./darknet detector test cfg/coco.data cfg/yolov3.cfg yolov3.weights data/dog.jpg
```
###  thresh 
**By default, YOLO only displays objects detected with a confidence of .25 or higher.**

```
./darknet detect cfg/yolov3.cfg yolov3.weights data/dog.jpg -thresh 0
```
##  `yolov3-tiny`[constrained environments]


```
wget https://pjreddie.com/media/files/yolov3-tiny.weights
```
***THEN:***

```
./darknet detect cfg/yolov3-tiny.cfg yolov3-tiny.weights data/dog.jpg
```




## Real-Time Detection on a Webcam



###  realtime camera

```
 ./darknet detector demo cfg/coco.data cfg/yolov3.cfg yolov3.weights 
```

If you have multiple webcams connected and want to select which one to use you can pass the flag `-c <num>` to pick (OpenCV uses webcam `0` by default).


###  rtsp stream

```
 ./darknet detector demo cfg/coco.data cfg/yolov3.cfg yolov3.weights rtsp://user:123456abcd@10.1.42.51/h264/ch1/main/av_stream
```
###  read from video
```
./darknet detector demo cfg/coco.data cfg/yolov3.cfg yolov3.weights data/s3.mp4
```

##  How  to  save the video after yolov3 recongnise ?


## Training YOLO on VOC

### Get The Pascal VOC Data
```
nohup wget https://pjreddie.com/media/files/VOCtrainval_11-May-2012.tar > 1.log 2>&1 &

nohup wget https://pjreddie.com/media/files/VOCtrainval_06-Nov-2007.tar > 2.log 2>&1 &

nohup wget https://pjreddie.com/media/files/VOCtest_06-Nov-2007.tar > 3.log 2>&1 &


```




-----
#  参考资料：
Series: YOLO object detector in PyTorch
https://blog.paperspace.com/tag/series-yolo/


YOLO v3 安装并训练自己数据
https://blog.csdn.net/qq_35451572/article/details/80384674


目标检测：yolov3训练自己的数据模型，避免踩坑
https://blog.csdn.net/xuanlang39/article/details/88642010



YOLO_v3_tutorial_from_scratch
https://github.com/ayooshkathuria/YOLO_v3_tutorial_from_scratch







