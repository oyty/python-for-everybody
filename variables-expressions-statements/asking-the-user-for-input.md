####用户主动输入

有时候我们期望一个变量的值是用户主动通过键盘输入的，Python提供了一个内建函数`input`，可以获取用户从键盘输入的值，当`input`方法被调用或执行的时候，程序暂停运行以等待用户从键盘输入，当用户敲击回车键的时候，程序恢复运行，`input`方法以字符串形式返回用户的输入。
> 在python 2.x，这个方法是`raw_input`

```python
>>> inp = input()
Some silly stuff
>>> print(inp)
Some silly stuff
```
在从用户哪里获得输入之前，最好是有一个提示告诉用户要输入什么，可以给`input`方法传入一个字符串。
```python
>>> name = input('What is your name?\n')
What is your name?
Chuck
>>> print(name)
Chuck
```

提示最后的`\n`表示换行，这是一个特殊字符，你可以看到用户的输入在提示的下方。

如果你希望用户输入的是一个整型，你可以使用`int()`方法将用户的输入强转成`int`：
```python
>>> prompt = 'What...is the airspeed velocity of an unladen swallow?\n'
>>> speed = input(prompt)
What...is the airspeed velocity of an unladen swallow?
17
>>> int(speed)
17
>>> int(speed) + 5
22
```
但是如果用户输入的不是数字，那就会出错：
```python

>>> speed = input(prompt)
What...is the airspeed velocity of an unladen swallow? What do you mean, an African or a European swallow?
>>> int(speed)
ValueError: invalid literal for int() with base 10:
```
我们稍后将会了解如何处理这种错误。













