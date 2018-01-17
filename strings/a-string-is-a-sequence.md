字符串是若干字符的序列，你可以用方括号逐一访问每个字符：
```python
>>> fruit = 'banana'
>>> letter = fruit[1]
```
第二条语句从`fruit`变量中提取位置为1的字符，然后赋值给`letter`变量。

方括号里面的表达式称为索引，索引表明你要访问字符序列中的哪个字符。
但是这可能并不是你想要的：
```python
>>> print(letter)
a
```

大多数人认为，`"banana"`的第一个字符是`b`而不是`a`，但是在Python中，index是从字符串头部算起的一个偏移量，第一个字符的偏移量是`0`。
```python
>>> letter = fruit[0]
>>> print(letter)
b
```
所以，`b`是`banana`的第0个字母，`a`是第一个字母，`n`是第二个字母。
索引可以是任何表达式，包括变量和运算符。但是索引的值必须是整型，不然你会得到如下错误：
```python
>>> letter = fruit[1.5]
TypeError: string indices must be integers
```


