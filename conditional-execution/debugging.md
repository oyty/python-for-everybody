当错误发生时，Python的错误追踪会显示很多信息，但是消息可能有点多，其中最有用的部分是：
- 错误的类型是什么
- 错误发生的位置
语法错误通常很容易找到，但是也有一些错误比较麻烦，像空格和制表符都是不可见的，出现这种错误可能比较发现。
```python
>>> x = 5 
>>>  y = 6
File "<stdin>", line 1 y=6
    ^
IndentationError: unexpected indent
```
这个例子中，第二行缩进只用了一个空格，但是错误却指向了y，这其实很容易误导我们。一般情况下，错误信息会显示问题在什么地方被发现，但是实际错误可能在所显示的代码之前，甚至前一行。


