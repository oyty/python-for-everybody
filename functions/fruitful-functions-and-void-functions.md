我们目前使用过的函数，像math函数就是带返回值的，像print_twice函数，执行任务但是没有返回值，当调用有返回值的函数时，大部分时候你想要利用返回值，例如将函数赋值给一个变量，也可以将函数作为表达式的一部分：
```python
x = math.cos(radians)
golden = (math.sqrt(5) + 1) / 2
```

当你在命令行下调用函数时，Python解释器会直接显示结果：
```python
>>> math.sqrt(5)
2.23606797749979
```

但是在代码里，如果不把函数的返回值存储在一个变量里面或者打印出来的话，返回值就会丢失。

空函数可能会在屏幕上输出一些信息，也可能会有其它的用途，但其本身没有返回值，如果你将一个空函数赋值给一个变量，就会得到一个特殊的值`None`。
```python
>>> result = print_twice('Bing')
Bing
Bing
>>> print(result)
None
```
`None`值和字符串"None"是不一样的，它是一种特殊的值并拥有自己的类型。
```python
>>> print(type(None)) 
<class 'NoneType'>
```
使用`return`语句从函数中返回结果：
```python
def addtwo(a, b): 
    added = a + b
    return added 
x = addtwo(3, 5)
print(x)
```


