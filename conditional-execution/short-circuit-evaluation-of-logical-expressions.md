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
第三次运算出错了，由于`y`等于`0`，Python计算`x/y`时出现运行时错误。但是第二次计算没有出错，那是因为表达式第一部分`x >= 2`判断为假，所以`x / y`根本没有被执行，所以没有报错。

我们可以在错误发生之前，加一个安全判断：
```python
>>> x = 1
>>> y = 0
>>> x >= 2 and y != 0 and (x/y) > 2
False
>>> x = 6
>>> y = 0
>>> x >= 2 and y != 0 and (x/y) > 2
False
>>> x >= 2 and (x/y) > 2 and y != 0
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: division by zero
>>>
```
第一个逻辑表达式中`x >= 2`为假，所以在`and`之前判断就停止了。第二个逻辑表达式中`x >= 2`为真，但`y != 0`为假，所以`x / y`没有机会执行。第三个表达式中`y != 0`位于`x / y`之后，所以这个表达式的判断就失败了。

