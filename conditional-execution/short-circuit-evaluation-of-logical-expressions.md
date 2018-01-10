当Python处理诸如`x>=2 and (x/y)>2`这样的逻辑表达式时，会从左至右进行判断。根据`and`的含义，如果`x`小于`2`，则表达式`x>=2`为假，那么整个表达式即为假，不管后面的`(x/y) > 2`的判断是真是假。

当Python发现逻辑表达式剩余部分的判断没有意义了，它就会停止对剩余部分的判断。这种特性会带来一种灵活的处理方式，我们看看下面的代码：
```python
>>> x = 6
>>> y = 2
>>> x >= 2 and (x/y) > 2
True
>>> x = 1
>>> y = 0
>>> x >= 2 and (x/y) > 2
False
>>> x = 6
>>> y = 0
>>> x >= 2 and (x/y) > 2
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: division by zero
>>>
```
第三次运算出错了，由于`y`等于`0`，Python计算`x/y`时出现运行时错误。

