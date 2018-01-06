数值是程序处理的最基本的事情，比如一个字符或者一个数字。我们目前所见到的数值有`1`，`2` 和`"Hello World"`。  
这些数值属于不同的类型：2是一个整型\(`Integer`\)，`"Hello World"`是一个字符串\(`string`\)，字符串被双引号包含。

输出语句一样适用于整型，我们可以使用命令行开启python解释器。

```python
python
>>> print(4)
4
```

如果你不确定一个数值是什么类型，那么解释器会告诉你：

```python
>>> type('Hello, World!') 
<class 'str'>
>>> type(17)
<class 'int'>
```

看起来并不意外，字符串输属于`str`类型，整型属于`int`类型，或许你可以猜到带小数点的数字是`float`类型，这叫做浮点型(`floating point`)

