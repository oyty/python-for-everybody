len是Python内建函数，函数返回字符串中字符的个数：
```python
>>> fruit = 'banana'
>>> len(fruit)
6
```
为了获取字符串的最后一个字符，你可能会这样做：
```python
>>> length = len(fruit)
>>> last = fruit[length]
IndexError: string index out of range
```
出现`IndexError`的原因是，在字符串`banana`中，没有索引为6的字符，既然是从零开始，六个字母的编号就是从0到5，所以最后一个字母对应的所以应该是length减一。
```python
>>> last = fruit[length-1]
>>> print(last)
a
```
当然了，你也可以使用负索引，从字符串末尾倒着计数，表达式`fruit[-1]`表示最后一个字母，`fruit[-2]`表示倒数第二个字母，以此类推。
