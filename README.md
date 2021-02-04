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

|  Model | Backbone | MS Training  | lr sched | mAP (COCO2017 val) | link
| ------------ | ------------ |------------ |------------ |------------ |------------ |
| FCOS | R50 | Yes  | 1x | 38.6 | soon |
| FCOS | R50 | Yes  | 2x | 41.0 | soon |
| FCOS | R50 | Yes | 3x | 42.0 | soon |
| ATSS | R50 | Yes | 1x | 39.5 | soon |
| ATSS | R50 | Yes | 2x | 41.9 | soon |
| ATSS | R50 | Yes | 3x | 42.8 | soon |
| FCOSPss | R50 | Yes | 3x | 42.3 | soon |
| ATSSPss | R50 | Yes | 3x | 42.6 | soon |
| ATSSPss | R101| Yes | 3x | 44.2 | |
| ATSSPss | X-101-32x4d-DCN | Yes | 3x | 47.5 | |
| ATSSPss | R2N-101-DCN | Yes | 3x | 48.5 | |

#### Two-Step Training
If we have a pretrained model, only finetuning the PSS head can save the training time.

| Model  | Backbone  | MS Training  | lr sched  | mAP <br> pretrain model (w NMS)  | mAP <br> finetuned PSS (w/o NMS)
| ------------ | ------------ | ------------ | ------------ | ------------ |------------ |
| GFocalV2Pss  | R50  | Yes  | 12  | [43.9](https://github.com/implus/GFocalV2 "43.9")  |43.3 |
| GFocalV2Pss | X-101-32x4d-DCN  | Yes | 12  | [48.8](https://github.com/implus/GFocalV2 "48.8")  | 48.2 |
| GFocalV2Pss | R2N-101-DCN | Yes | 12 | [49.9](https://github.com/implus/GFocalV2 "49.9") | 49.2 |



## PSS for nms-free Instance Segmentation

#### End-to-End Training

|  Model | Backbone | MS Training  | lr sched | bbox mAP (COCO2017 val) | segm mAP (COCO2017 val) | link
| ------------ | ------------ |------------ |------------ |------------ |------------ | ------------ |
| CondInst | R50 | Yes | 1x | 38.9 | 34.1 | |
| CondInstPss | R50 | Yes | 1x | 39.4 | 34.4 | |


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
