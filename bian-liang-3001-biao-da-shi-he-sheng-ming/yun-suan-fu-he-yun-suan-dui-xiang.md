运算符是一堆特殊的符合，被用来计算数值，比如相加相减等。运算符操作的对象叫做运算对象（`operands`）。
运算符`+`,`-`,`*`,`/`和`**`分别表示加，减，乘，除和乘方。举例如下：
```python

20+32 hour-1 hour*60+minute minute/60 5**2 (5+9)*(15-7)
```

除法运算在Python 2.x和Python 3.x中有点不同，在Python 3.x中，除法运算的结果是浮点数：
```python
>>> minute = 59
>>> minute/60
0.9833333333333333
```
在Python 2.0中两个整型相除结果是一个整型：
```python
>>> minute = 59
>>> minute/60
0
```
如果要在Python 3.x中得到相同的结果，可以向下取余相除（`//integer`）
```python
>>> minute = 59
>>> minute//60
0
```
在Python 3.x中，除法运算更像是使用计算器运算得到结果。
