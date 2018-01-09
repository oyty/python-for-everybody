一个条件语句也可以嵌套到另一个条件语句下，我们可以写出如下的三个分支的条件语句：
```python
if x == y:
    print('x and y are equal')
else:
    if x < y:
        print('x is less than y') 
    else:
        print('x is greater than y')
```
外面的条件语句包含了两个分支，第一条分支包含了一个简单语句，第二条分支包含了另一个由两个分支组成的`if`语句。

虽然缩进让语句结构变得清晰，但是嵌套条件还是很难让人快速阅读代码，所以尽量避免。逻辑运算符就提供了一种方法来简化嵌套条件语句。
例如，使用单个条件改写以下代码：
```python
if 0 < x:
    if x < 10:
        print('x is a positive single-digit number.')
```
当两个条件都满足时，`print`语句才会执行。使用`and`运算就可以达到这种效果：
```python
if 0 < x and x < 10:
    print('x is a positive single-digit number.')
```
