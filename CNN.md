在定义CNN模块时需要的参数：

```python
def conv3x3(in_channels, out_channels, stride=1):
    return nn.Conv2d(in_channels, out_channels, kernel_size=3,
                     stride=stride, padding=1, bias=False)
def __init__(self,
             in_channels: int,
             out_channels: int,
             kernel_size: Union[int, tuple],
             stride: Any = 1,
             padding: Any = 0,
             dilation: Any = 1,
             groups: int = 1,
             bias: bool = True,
             padding_mode: str = 'zeros') -> None

  padding=1表示四周进行1个像素点的零填充，将那些位置都填充成0
  padding=0表示不进行零填充
  
  in_channels表示输入数据体的深度
  out_channels表示输出数据体的深度
  
  kernel_size=3表示卷积核的大小，这里只用一个数字，表示高和宽相同，也可以 kernel_size=（3，2）表示高和宽不同
  
  groups=1表示所有的输入和输出都是相关联的，groups=2表示输入的深度被分割成两份，输出的深度也被分割成两份。
  
  dilation表示卷积核对于输入数据体的空间间隔，想像成两个平面之间的距离。
    
```

