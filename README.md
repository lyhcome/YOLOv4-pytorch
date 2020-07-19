# YOLOv4-pytorch

This is a PyTorch re-implementation of YOLOv4 architecture based on the official darknet implementation [AlexeyAB/darknet](https://github.com/AlexeyAB/darknet) with PASCAL VOC, COCO and Custom dataset
---
## Environment

* Nvida GeForce RTX 2070
* CUDA10.0
* CUDNN7.0
* windows or linux
* python 3.6
```bash
# install packages
pip3 install -r requirements.txt --user
```
---
## Brief
* [x] Mish
* [x] Custom data
* [x] Data Augment (RandomHorizontalFlip, RandomCrop, RandomAffine, Resize)
* [x] Multi-scale Training (320 to 640)
* [x] focal loss
* [x] GIOU
* [x] Label smooth
* [x] Mixup
* [x] cosine lr

---
## Prepared work

### 1、Git clone YOLOv4 repository
```Bash
git clone github.com/argusswift/YOLOv4-pytorch.git
```
update the `"PROJECT_PATH"` in the config/yolov4_config.py.

---

### 2、Download dataset
* Download Pascal VOC OR COCO dataset : [VOC 2012_trainval](http://host.robots.ox.ac.uk/pascal/VOC/voc2012/VOCtrainval_11-May-2012.tar) 、[VOC 2007_trainval](http://host.robots.ox.ac.uk/pascal/VOC/voc2007/VOCtrainval_06-Nov-2007.tar)、[VOC2007_test](http://host.robots.ox.ac.uk/pascal/VOC/voc2007/VOCtest_06-Nov-2007.tar). 
http://images.cocodataset.org/zips/train2017.zip 
http://images.cocodataset.org/annotations/annotations_trainval2017.zip
http://images.cocodataset.org/zips/val2017.zip 
http://images.cocodataset.org/annotations/stuff_annotations_trainval2017.zip
http://images.cocodataset.org/zips/test2017.zip 
http://images.cocodataset.org/annotations/image_info_test2017.zip
put them in the dir, and update the `"DATA_PATH"` in the params.py.
* Convert data format :use utils/voc.py convert the pascal voc *.xml format to txt format (Image_path0 &nbsp; xmin0,ymin0,xmax0,ymax0,class0 &nbsp; xmin1,ymin1...)

## Reference

* tensorflow : https://github.com/Stinky-Tofu/Stronger-yolo
* pytorch : https://github.com/ultralytics/yolov3
https://github.com/Peterisfar/YOLOV3
* keras : https://github.com/qqwweee/keras-yolo3
