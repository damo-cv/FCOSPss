# Object Detection Made Simpler by Eliminating Heuristic NMS
PyTorch Implementation for Our Paper: "Object Detection Made Simpler by Eliminating Heuristic NMS"


## Requirements
* Python 3.7
* PyTorch 1.5.1
* [mmdetectoin](https://github.com/open-mmlab/mmdetection)

## Usage:

The code is being submitted to the company for open source review.

## PSS for nms-free Object Detection:

#### End-to-End Training

|  Model | Backbone | lr sched | mAP (COCO2017 val) | link
| ------------ | ------------ |------------ |------------ |------------ |
| FCOS | R50  | 3x | 42.0 | [model](http://ai4prz5kwonline.oss-cn-zhangjiakou.aliyuncs.com/jianchong_new%2Ffcos_r50-caffe_coco-480-800-3x.pth?Expires=1931844166&OSSAccessKeyId=FbmV29ZaCO4CLhjO&Signature=7pHiB3dhpl5lgzxJaR5i5J87dBA%3D) |
| ATSS | R50 | 3x | 42.8 | [model](http://ai4prz5kwonline.oss-cn-zhangjiakou.aliyuncs.com/jianchong_new%2Fatss_r50-caffe_coco-480-800-3x.pth?Expires=2416484320&OSSAccessKeyId=FbmV29ZaCO4CLhjO&Signature=JnsqZMLOWd6grL%2F6thoa4kITlWM%3D) |
| FCOS<sub>pss</sub> | R50  | 3x | 42.3 |  |
| ATSS<sub>pss</sub> | R50  | 3x | 42.6 |  |
| VFNET<sub>pss</sub> | R50 | 3x | 44.0 |  |
| FCOS<sub>pss</sub> | R101  | 3x | 44.1 |  |
| ATSS<sub>pss</sub> | R101 | 3x | 44.2 |  |
| VFNET<sub>pss</sub> | R101 | 3x | 45.7 |  |
| FCOS<sub>pss</sub> | X-101-DCN  | 2x | 47.0 |  |
| ATSS<sub>pss</sub> | X-101-DCN  | 2x | 47.3 |  |
| VFNET<sub>pss</sub> | X-101-DCN | 2x | 49.3 |  |
| FCOS<sub>pss</sub> | R2N-101-DCN | 2x | 48.2 |  |
| ATSS<sub>pss</sub> | R2N-101-DCN  | 2x | 48.6 |  |
| VFNET<sub>pss</sub> | R2N-101-DCN | 2x | 50.0 |  |
**NOTE:** All models are trained with multi-scale training schedule of ‘[480, 800] $\times$ 1333’.

#### Two-Step Training
If we have a pretrained model, only finetuning the PSS head can save the training time.

| Model  | Backbone  | MS Training  | lr sched  | mAP <br> pretrain model (w NMS)  | mAP <br> finetuned PSS (w/o NMS)
| ------------ | ------------ | ------------ | ------------ | ------------ |------------ |
| GFocalV2<sub>pss</sub>  | R50  | Yes  | 12  | [43.9](https://github.com/implus/GFocalV2 "43.9")  |43.3 |
| GFocalV2<sub>pss</sub> | X-101-32x4d-DCN  | Yes | 12  | [48.8](https://github.com/implus/GFocalV2 "48.8")  | 48.2 |
| GFocalV2<sub>pss</sub> | R2N-101-DCN | Yes | 12 | [49.9](https://github.com/implus/GFocalV2 "49.9") | 49.2 |



## PSS for nms-free Instance Segmentation

#### End-to-End Training

|  Model | Backbone  | lr sched | bbox mAP  | segm mAP | link
| ------------ | ------------ | ------------ |------------ |------------ |------------ |------------ | ------------ |
| [CondInst](https://github.com/aim-uofa/AdelaiDet/tree/master/configs/CondInst)  | R50  | 3x | 41.9 | 37.5 | |
| CondInst<sub>pss</sub> | R50  | 3x | 41.2 | 36.7 | |
| [CondInst + sem](https://github.com/aim-uofa/AdelaiDet/tree/master/configs/CondInst)  | R50  | 3x | 42.6 | 38.2 | |
| CondInst<sub>pss</sub> + sem | R50  | 3x | 42.3 | 37.7 | |
| [CondInst](https://github.com/aim-uofa/AdelaiDet/tree/master/configs/CondInst)  | R101  | 3x | 43.3 | 38.6 | |
| CondInst<sub>pss</sub> | R101  | 3x | 43.1 | 38.2 | |
| [CondInst + sem](https://github.com/aim-uofa/AdelaiDet/tree/master/configs/CondInst)  | R101  | 3x | 44.6 | 39.8 | |
| CondInst<sub>pss</sub> + sem | R101  | 3x | 44.1 | 39.3 | |

**NOTE:** All models are trained with multi-scale training schedule of ‘[640, 800] $\times$ 1333’.

## Citation
If you use the package in your research, please cite our paper:
```
@misc{zhou2021object,
      title={Object Detection Made Simpler by Eliminating Heuristic NMS}, 
      author={Qiang Zhou and Chaohui Yu and Chunhua Shen and Zhibin Wang and Hao Li},
      year={2021},
      eprint={2101.11782},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
}
```

## PS
团队长期招聘中，社招/实习/校招，我们都要 !
欢迎投递简历，邮箱: `zhouqiang@zju.edu.cn`
