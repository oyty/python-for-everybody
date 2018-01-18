下面的程序统计了字符`a`在字符串中出现的次数：
```python
word = 'banana' 
count = 0
for letter in word:
    if letter == 'a': 
    count = count + 1
print(count)
```
这个程序演示了另一种计算模式，称为计数器。变量`count`初始值为0，然后遍历过程中，每发现一个`a`，`count`值就加一。当循环结束时，`count`就是`a`在字符串中出现的次数。


**习题 6.3**
定义一个count函数并封装这段代码，对其进行通用化改造，能够接收字符串和字母作为参数。

