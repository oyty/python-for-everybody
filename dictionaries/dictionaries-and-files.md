字典的常见用法之一是对书面文本的文本文件进行词频统计，让我们从《罗密欧与朱丽叶》中抽取一段简单的文本。
[http://shakespeare.mit.edu/Tragedy/romeoandjuliet/romeo_juliet.2.2.html](http://shakespeare.mit.edu/Tragedy/romeoandjuliet/romeo_juliet.2.2.html)
刚开始，我们先使用一个简短的不含标点符号的文本，稍后我们将处理包含标点的文本。
```
But soft what light through yonder window breaks
It is the east and Juliet is the sun
Arise fair sun and kill the envious moon
Who is already sick and pale with grief
```

我们将编写Python代码去逐行读取整个文件，并将每一行文本分解成一个一个单词组成的列表。循环行中的每一个单词，使用字典计算每一个单词出现的次数。

你可以看到，这段代码包含两个for循环，外层的for循环读取文件的每一行，内层的for循环迭代特定行的每个单词，这就是所谓的嵌套循环，分为外部循环和内部循环。

外层循环每迭代一次，内层循环将会执行它全部的迭代。

两个循环组合保证了文件中的每一个单词都会被统计到。
```python
fname = input('Enter the file name: ') 
try:
    fhand = open(fname) 
except:
    print('File cannot be opened:', fname)
    exit()
    
counts = dict() 
for line in fhand:
    words = line.split() 
    for word in words:
        if word not in counts: 
            counts[word] = 1
        else:
            counts[word] += 1
print(counts)
```
运行该程序，会输出包含全部计数的没有排序的统计结果。remeo.txt文件可以从[www.py4e.com/code3/romeo.txt](/www.py4e.com/code3/romeo.txt)获得。
```python
python count1.py
Enter the file name: romeo.txt
{'and': 3, 'envious': 1, 'already': 1, 'fair': 1,
'is': 3, 'through': 1, 'pale': 1, 'yonder': 1,
'what': 1, 'sun': 2, 'Who': 1, 'But': 1, 'moon': 1,
'window': 1, 'sick': 1, 'east': 1, 'breaks': 1,
'grief': 1, 'with': 1, 'light': 1, 'It': 1, 'Arise': 1,
'kill': 1, 'the': 3, 'soft': 1, 'Juliet': 1}
```
仅仅通过字典去找到出现次数最多的单词及其次数并不是那么方便，所以我们还需要增加一些Python代码以便输出更有用的信息。


