####表达式

一个表达式包含数值、变量和运算符，一个单单的值也是一个表达式，也是一个变量，所以下面的都是合法的。（假设变量`x`已经被赋值了）
```python
17
x
x + 17
```
如果你在命令行下输入一个表达式，解释器将会计算并输出：
```python
>>> 1 + 1 
2
```
但是在一个脚本中，单单是一个表达式，它什么都不会做，这对于新手来说可能有点困惑。

**习题 2.1**
在命令行模式下输入以下代码，看看是什么样的结果。
```python
5 
x=5 
x+1
```
