你可能最常遇见的错误就是变量名不合法了，例如不知道`class`和`yield`是保留字，或者包含不合法字符的变量名`odd~job`、`UD$`等。

如果变量名中存在空格，Python认为它是没有运算符的两个运算对象。
```python
>>> bad name = 5
SyntaxError: invalid syntax
```

```python
>>> month = 09
  File "<stdin>", line 1
month = 09 ^
SyntaxError: invalid token
```
对于语法错误来说，错误信息还真提供不了什么帮助。最常见的错误信息就是SyntaxError: invalid syntax and SyntaxError: invalid token，没一个有价值。

最常见的运行时错误就是使用了一个还没有赋值的变量，这种情况最容易出现在变量名拼写错误的场景。

```python
>>> principal = 327.68
>>> interest = principle * rate
NameError: name 'principle' is not defined
```

变量名是区分大小写的，比如LaTex和latex是不一样的。

最容易出现的语义错误是运算顺序，比如`1/2π`，你很有可能会写成：
```python
>>> 1.0 / 2.0 * pi
```
程序原本的意思是先计算2*π，然后计算除法，可是代码中是先计算除法，再计算乘法，这种情况下，程序是不会报错的，但显然不是你要的结果。




