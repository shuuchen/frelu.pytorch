# frelu.pytorch
An unofficial pytorch implementation of funnel activation https://arxiv.org/pdf/2007.11824.pdf. Official implementation can be found [here](https://github.com/megvii-model/FunnelAct).

<div align=left>
![](images/frelu.jpg)
</div>


## Requirements
[]()

## Usage
* Simply replace nn.ReLU with FReLU(num_channels), details can be found [here]().
```python
from frelu import FReLU

conv = nn.Conv2d(in_channels, out_channels, 3, padding=1)
bn = nn.BatchNorm2d(out_channels)
frelu = FReLU(out_channels) # ⬅️
```


## Performance
<div align=left>
![](images/frelu.jpg)
</div>


## References
* [official implementation](https://github.com/megvii-model/FunnelAct)
* https://github.com/pytorch/examples/blob/master/imagenet/main.py
* https://github.com/pytorch/vision/blob/master/torchvision/models/resnet.py
