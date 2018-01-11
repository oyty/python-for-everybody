Python的math模块提供了很多常见的数学函数，要记住，在使用这些函数之前要先导入相应的包：
```python
>>> import math
```
这条语句创建了一个名为math的模块对象，如果将这个模块对象打印出来，可以得到关于它的一些信息：
```python
>>> print math
<module 'math' from '.../math.so'>
>>> 
```
这个模块对象包含了模块中定义的函数和变量，如果要使用它们，你必须指定模块名和函数名，用圆点隔开，也就是英文的句号，这种格式叫做`点标记(dot natation)`。

```python
>>> ratio = signal_power / noise_power
>>> decibels = 10 * math.log10(ratio)

>>> radians = 0.7
>>> height = math.sin(radians)
```
第一个例子是计算以10为底的信噪比的对数，math模块还提供了`log`函数用来求以`e`为底的对数。
第二个例子调用正弦函数，变量名见名知意，除了正弦函数还有余弦，正切等其它三角函数，它们都采用弧度作为参数，将度数转化成弧度：度数除以360，然后乘以2π：
```python
>>> degrees = 45
>>> radians = degrees / 360.0 * 2 * math.pi
>>> math.sin(radians)
0.7071067811865476
```
`math.pi`表达式从`math`模块中取得变量`pi`的值，这个`pi`是π的一个近似值，保留了小数点后15位数。

运用你的数学知识，与-2的平方根再除以2的结果进行比较，看看程序输出的结果是否正确。
```python
>>> math.sqrt(2) / 2.0
0.7071067811865476
```


