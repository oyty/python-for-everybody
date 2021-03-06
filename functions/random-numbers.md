在相同的输入下，大部分计算机程序都会输出相同的结果，这很好理解，我们当然希望同一个算法，相同的输入产生相同的结果。但是有时候，我们却希望计算机具备不确定性，游戏比较明显，还有一些其它例子。

让一个程序完全处于不确定状态，这很难做到，但是，有一些方法可以让它看起来具有不确定性。一种方法是利用算法产生伪随机数，伪随机数并不是真正的随机数，原因在于它们是用确定的算法计算出来的。如果单看这些数字并不会发现它们和真正的随机数有什么不同。

随机数模块提供了伪随机数生成的函数，也就是`random`。

`random`函数返回一个介于`0.0-1.0`的随机浮点数（包括`0.0`，但不包括`1.0`），每次调用时，你会得到一长串的数字：
```python
import random
for i in range(10):
    x = random.random() 
    print(x)
```
程序生成了10个介于`0.0-1.0`之间但是不包括1.0的随机数。
```python
0.11132867921152356
0.5950949227890241
0.04820265884996877
0.841003109276478
0.997914947094958
0.04842330803368111
0.7416295948208405
0.510535245390327
0.27447040171978143
0.028511805472785867
```

**习题 4.1**
运行以下程序，并观察得到的结果，不妨多试几次。
random函数只是众多随机数函数中的一个，`randint`函数传入两个整数参数，并返回介于这两个参数之间的整数（包括这两个参数在内）。
```python
>>> random.randint(5, 10)
5
>>> random.randint(5, 10)
9
```

要取得一组值中的随机元素，可以使用下面的程序：
```python
>>> t = [1, 2, 3]
>>> random.choice(t)
2
>>> random.choice(t)
3
```

`random`模块还提供了从高斯函数、指数函数和伽玛函数等函数中获取随机数的函数。
