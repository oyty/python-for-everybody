赋值语句的常见模式就是对变量进行更新，变量的新值依赖旧值。
```python
x = x+1
```
这条语句的作用是：得到x的当前值，加一，然后将相加结果作为新值赋值给x。

如果更新一个不存在的变量，就会出错，因为Python会在给x赋值之前，先计算等号右边的表达式。
```python
>>> x = x + 1
NameError: name 'x' is not defined
```

在更新变量之前，必须先初始化，通常使用简单的赋值语句：
```python
>>> x = 0
>>> x = x + 1
```

通过加一操作更新变量成为增量操作，减一操作称为减量更新。
