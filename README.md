# Object Detection Made Simpler by Eliminating Heuristic NMS
PyTorch Implementation for Our Paper: "Object Detection Made Simpler by Eliminating Heuristic NMS"


## Requirements
* Python 3.7
* PyTorch 1.1
* [mmdetectoin](https://github.com/open-mmlab/mmdetection)

## Usage:

The code is being submitted to the company for open source review.

## Models:

------------

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
