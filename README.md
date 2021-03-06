# frelu.pytorch
An unofficial pytorch implementation of funnel activation https://arxiv.org/pdf/2007.11824.pdf. Official implementation can be found [here](https://github.com/megvii-model/FunnelAct).

<img src="https://github.com/shuuchen/frelu.pytorch/blob/master/images/frelu.png" width="480" height="220" />


## Requirements
```
pip install -r requirements.txt
```

## Usage
* Simply replace nn.ReLU with FReLU(num_channels), details can be found [here](https://github.com/shuuchen/frelu.pytorch/blob/master/resnet.py).
```python
from frelu import FReLU

conv = nn.Conv2d(in_channels, out_channels, 3, padding=1)
bn = nn.BatchNorm2d(out_channels)
frelu = FReLU(out_channels) # ⬅️
```

## TODO
- [ ] ImageNet training & performance checking


## References
* [official implementation](https://github.com/megvii-model/FunnelAct)
* https://github.com/pytorch/examples/blob/master/imagenet/main.py
* https://github.com/pytorch/vision/blob/master/torchvision/models/resnet.py
