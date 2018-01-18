字符串是一种Python对象，一个对象包含数据（即字符串本身）和方法，这些方法是内置在Python中的高效函数，作用于每一个对象实例。

Python有一个`dir`函数，它可以列出一个对象实例的所有方法，`type`函数获取的是对象的类型，`dir`函数获取的是对象的可用方法。
```python
>>> stuff = 'Hello world'
>>> type(stuff)
<class 'str'>
>>> dir(stuff)
['capitalize', 'casefold', 'center', 'count', 'encode', 'endswith', 'expandtabs', 'find', 'format', 'format_map', 'index', 'isalnum', 'isalpha', 'isdecimal', 'isdigit', 'isidentifier', 'islower', 'isnumeric', 'isprintable', 'isspace', 'istitle', 'isupper', 'join', 'ljust', 'lower', 'lstrip', 'maketrans', 'partition', 'replace', 'rfind', 'rindex', 'rjust', 'rpartition', 'rsplit', 'rstrip', 'split', 'splitlines', 'startswith', 'strip', 'swapcase', 'title', 'translate', 'upper', 'zfill']
>>> help(str.capitalize)
Help on method_descriptor:
capitalize(...)
    S.capitalize() -> str
    Return a capitalized version of S, i.e. make the first character
    have upper case and the rest lower case.
>>>
```
dir列出这些方法后，你可以使用help函数获取这些方法的简单文档描述，要查看更完善的string函数的文档：https://docs.python.org/3.5/library/stdtypes.html#string-methods

调用方法和调用函数类似，都是传入参数，返回结果，但是它们的语法有点不一样，调用方法的语法是，用句点作为分割，在变量名后面跟上方法名。（这里的方法指对象的内置方法，函数是我们自己在程序中写的函数，其实他们都是方法，只是作用域不一样，方法就是函数，这点要区分好，理解好）

比如，upper方法接收一个字符串，然后返回一个全部大写字符的新的字符串。
不是`upper(word)`，而是`word.upper()`。
```python
>>> word = 'banana'
>>> new_word = word.upper()
>>> print(new_word)
BANANA
```
这种点标记形式指定方法名为upper，将次方法应用于变量word，空的圆括号表明这个方法没有参数。

另一个字符串方法`find`，找到字符串中字符所在位置：
```python
>>> word = 'banana'
>>> index = word.find('a')
>>> print(index)
1
```
这这个例子中，我们在word对象上调用find方法，然后传入一个字符作为参数。
find方法不仅适用于字符，也可用于寻找字符串子串：
```python
>>> word.find('na')
2
```
find方法可以传入第二个参数，表示从哪个索引位置开始检查：
```python
>>> word.find('na', 3)
4
```

一个很常见的需求是使用strip方法移除字符串首尾的空白（包括空格、制表符和换行符）。
```python
>>>line=' Herewego ' 
>>> line.strip()
'Here we go'
```

还有一些方法，像`startwith`，返回的是一个布尔值：
```python
>>> line = 'Have a nice day'
>>> line.startswith('Have')
True
>>> line.startswith('h')
False
```
你应该发现了，startwith方法是对大小写敏感的，所以一般我们都使用lower方法将其统一转换成小写。
```python

>>> line = 'Have a nice day'
>>> line.startswith('h')
False
>>> line.lower()
'have a nice day'
>>> line.lower().startswith('h')
True
```
最后一个例子中调用了`lower`方法，然后使用`startwith`方法检查小写转换后的字符串是否以字母`p`开头。只要注意好次序，我们就可以在一个表达式中运用多个方法，就像这样`line.lower().startswith('h')`


**习题 6.4**
字符串方法`count`和我们之前练习过的函数类似，请访问`https://docs.python.org/3.5/library/stdtypes.html#string-methods`，查看这个方法的文档，编写一个方法调用，统计`a`在`banana`中出现的次数。




