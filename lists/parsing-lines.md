通常我们在读取一个文件的时候，我们相对文件行做一些处理，而不仅仅是打印整个文件行。我们可能想找到一些我们感兴趣的行，然后解析这些行，找出我们想要的部分，如果我们想打印这些行中以`From`开头的行中的星期呢？
```
From stephen.marquard@uct.ac.za Sat Jan 5 09:14:16 2008
```
split方法处理这类问题非常高效，我们可以写一个小程序，寻找那些以From开头的行，然后分割这些行，打印出行中的第三个单词：
```python
fhand = open('mbox-short.txt') 
for line in fhand:
    line = line.rstrip()
    if not line.startswith('From '): 
        continue 
    words = line.split()
    print(words[2])
```
程序输出如下：
```python
Sat
Fri
Fri
Fri
...
```
后面我们会介绍更复杂的行间文本提取技术，以及如何分析文本行以找到我们想要的信息。