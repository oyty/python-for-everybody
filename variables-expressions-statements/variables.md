####变量

编程语言的一个最强大的特性就是可以操作变量(`variables`)
一个赋值语句创建了一个新的变量，并且为这个变量赋值：
```python
>>> message = 'And now for something completely different'
>>> n = 17
>>> pi = 3.1415926535897931
```
上面的例子干了三件事，第一个创建了一个字符串变量`message`，第二个整型变量`n`，值是17，第三个将π的近似值赋值给了变量`pi`。

要输出一个变量的值，你可以使用`print`语句
```python
>>> print(n)
17
>>> print(pi)
3.141592653589793
```
一个变量的类型就是变量的值所代表的类型：
```python
>>> type(message) <class 'str'>
>>> type(n) <class 'int'>
>>> type(pi) <class 'float'>
```


