有时候在循环迭代的过程中，你想跳过当前迭代，直接进去下一轮迭代，这种情况下，你可以使用`continue`语句，直接跳入到下一轮迭代而无需完成当前迭代。

下面的例子不断地打印输入值，直到用户输入"done"才会结束。但是#开头的输入不会被打印出来(这有点像Python的注释)。

运行下面加了`continue`语句的新程序：
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
除了#号开头的行，其它所有的行都被打印出来，当`continue`语句被执行，当前迭代就会结束，跳到`while`语句的开头，执行下一轮循环。这样也就跳过了`print`语句。




