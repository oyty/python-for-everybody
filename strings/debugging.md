写代码的时候，你要多问问自己，『这里可能会出现什么错误？』或者『我们的用户会做出什么疯狂的事情导致我们的（看似）完美的程序崩溃？』，要多培养这个意识哦。

例如，在第五章迭代中介绍while循环的程序示例如下：
```python
while True:
    line = input('> ') 
    if line[0] == '#': 
        continue
    if line == 'done': 
        break
    print(line)
print('Done!')
```
看看如果用户输入一个空行时会发生什么：
```python
> hello there
hello there
> # don't print this
> print this!
print this!
>
Traceback (most recent call last):
File "copytildone.py", line 3, in <module> if line[0] == '#':
IndexError: string index out of range
```
输入空行之前代码运行都是正常的，但是因为没有第0位字符，所以出错了。这里有两种方式处理这种错误，即使输入空行，程序也能安全运行：

一种方法是使用`startwith`方法判断，如果输入为空，就返回False
```python
    if line.startswith('#'):
```

还有一种是使用守护模式，通过一条if语句进行控制，保证第二个逻辑表达式只有在字符串中至少有一个字符时才进行判断。
```python
    if len(line) > 0 and line[0] == '#':
```
