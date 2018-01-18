通常，我们想要在一个字符串中寻找它的子串，下面是一个结构化的字符串：
```python
From stephen.marquard@ uct.ac.za Sat Jan 5 09:14:16 2008
```
我们只想抽出电子邮件的第二部分（即uct.ac.za），可以使用find方法和字符串切片来实现。

首先，在字符串中找到`@`符号的位置，然后，我们找到`@`符号之后第一个空格的位置，最后，我们使用切片来提取字符串中我们需要的部分。
```python
>>> data = 'From stephen.marquard@uct.ac.za Sat Jan  5 09:14:16 2008'
>>> atpos = data.find('@')
>>> print(atpos)
21
>>> sppos = data.find(' ',atpos)
>>> print(sppos)
31
>>> host = data[atpos+1:sppos]
>>> print(host)
uct.ac.za
>>>
```
这里使用是find方法的一种用法，指定find方法从何处开始寻找。当切分字符串时，我们提取的字符是"位于`@`符号之后但不包括空格"的字符。

find方法的文档：
`http://docs.python.org/library/string.html。`
