有时候我们期望一个变量的值是用户主动通过键盘输入的，Python提供了一个内建函数`input`，可以获取用户从键盘输入的值，当`input`方法被调用或执行的时候，程序暂停运行以等待用户从键盘输入，当用户敲击回车键的时候，程序恢复运行，`input`方法以字符串形式返回用户的输入。
> 在python 2.x，这个方法是`raw_input`

```python
>>> inp = input()
Some silly stuff
>>> print(inp)
Some silly stuff
```