布尔表达式要么是True，要么是False，`==`运算符用来比较相关运算对象是否相等，若两者相等则返回True，否则返回False。

```python
>>> 5 == 5
True
>>> 5 == 6
False
```

`True`或`False`是bool类型的两个值，可不是字符串哦。

```python
>>> type(True) 
<class 'bool'> 
>>> type(False) 
<class 'bool'>
```

`==`是比较运算符中的一个，还有一些其它的比较运算符：
```python
x != y  # x不等于y
x>y     # x大于y
x<y     # x小于y
x >= y  # x大于等于y
x <= y  # x小于等于y
x is y      # x is the same as y
x is not y  # x is not the same as y
```



