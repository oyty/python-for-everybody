切片操作也适用于列表：
```python
>>> t = ['a', 'b', 'c', 'd', 'e', 'f']
>>> t[1:3]
['b', 'c']
>>> t[:4]
['a', 'b', 'c', 'd']
>>> t[3:]
['d', 'e', 'f']
LISTS
```
如果省略第一个索引，切片将从列表头部开始，如果省略第二个索引，切片将处理到列表的末尾。如果两个索引都被省略，将会得到整个列表。
```python
>>> t[:]
['a', 'b', 'c', 'd', 'e', 'f']
```

由于列表是可变的，在对列表进行操作前，最好先备份一份。

赋值语句左边的切片操作可以同时更新多个元素：
```python
>>> t = ['a', 'b', 'c', 'd', 'e', 'f']
>>> t[1:3] = ['x', 'y']
>>> print(t)
['a', 'x', 'y', 'd', 'e', 'f']
```
