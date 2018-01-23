字符串是字符的序列，列表是数值的序列，但是字符列表和字符串是不同的，要将字符串转换成字符列表，你可以使用`list`方法。
```python
>>> s = 'spam'
>>> t = list(s)
>>> print(t)
['s', 'p', 'a', 'm']
```
因为`list`是一个内建函数名，所以要避免使用`list`作为变量名。也应该避免使用`l`作为变量名，因为它和数字`1`很相似，容易搞混，所以上面用了`t`做变量名。

`list`函数将一个字符串转换成一些独立的字母，如果你想将字符串分割成一些单词，你可以使用`split`函数。
```python
>>> s = 'pining for the fjords'
>>> t = s.split()
>>> print(t)
['pining', 'for', 'the', 'fjords']
>>> print(t[2])
the
```

一旦你使用split函数将字符串分割成由单词组成的序列，你就可以使用索引操作符（方括号）来访问列表中的特定单词了。

split有一个可选参数，称为分隔符，它可以指定某一特定字符作为分割的界线，下面的示例使用`-`作为分隔符：
```python
>>> s = 'spam-spam-spam'
>>> delimiter = '-'
>>> s.split(delimiter)
['spam', 'spam', 'spam']
```

`join`函数和`split`函数的作用相反，它将一个字符串序列里面的每个元素连接在一起，`join`是一个字符串方法，所以你必须指定分隔符，并将字符串序列作为参数。
```python

>>> t = ['pining', 'for', 'the', 'fjords'] 
>>> delimiter = ' '
>>> delimiter.join(t)
'pining for the fjords'
```
在上面例子中，分隔符是空格，所以`join`方法将元素用空格连接。如果不用空格将元素连接，分隔符可以使用`''`
