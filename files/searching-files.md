当你要搜索文件数据时，一种很常规的方式是通读文件，然后只处理符合特定条件的文本行，其它一概忽略。我们将文件读取和字符串方法结合起来，构建简单的搜索机制。

举个栗子，你要读取一个文件，然后只打印出以`From:`开头的行，我们可以使用`startwith`方法去过滤出符合我们前缀要求的行。
```python
fhand = open('mbox-short.txt') 
count = 0
for line in fhand:
    if line.startswith('From:'): 
        print(line)
```
程序执行，输出结果如下：
```
From: stephen.marquard@uct.ac.za

From: louis@media.berkeley.edu

From: zqian@umich.edu

From: rjlowe@iupui.edu

...
```
输出的结果正是我们想要的以`From:`开头的行，但是我们好像看到了多余的空行，这就是每行末尾那个不可见的换行符。所以`print`语句打印了自带换行符的文本行，然后因为`print`语句本身带一个换行符，所以结果就是两个空行。

我们当然可以使用字符串分割来打印不含最后换行符的文本行，但是最简单的方式是使用`rstrip`方法截掉字符串后面的空白符：
```python
fhand = open('mbox-short.txt') 
for line in fhand:
    line = line.rstrip()
    if line.startswith('From:'):
        print(line)
```
程序运行，输出结果如下：
```python
From: stephen.marquard@uct.ac.za
From: louis@media.berkeley.edu
From: zqian@umich.edu
From: rjlowe@iupui.edu
From: zqian@umich.edu
From: rjlowe@iupui.edu
From: cwen@iupui.edu
...
```

随着文件搜索程序变得越来越复杂，你可能想在你的循环中使用`continue`语句，迭代搜索的一个基本思路是，找到你感兴趣的文本行，然后做相应处理，对于不感兴趣的，就高效地跳过。

跳过不感兴趣的文本行的循环结构：
```python
fhand = open('mbox-short.txt') 
for line in fhand:
    line = line.rstrip()
    # Skip 'uninteresting lines'
    if not line.startswith('From:'): 
        continue
    # Process our 'interesting' line
    print(line)
```
程序的运行结果是一样的，你可以这样理解，那些不感兴趣的行就是不以`From:`开头的行，然后我们就使用continue跳过，对于感兴趣的行（以`From:`开头的行），进行相关处理。

我们可以使用find方法来模拟文本编辑器的搜索功能，由于find方法可以找出一个字符串在另一个字符串中出现的次数，也可以返回查询字符串的位置或者-1（也就是没有找到），所以我们可以写出如下循环打印出那些包含`@uct.ac.za`的行：
```python
fhand = open('mbox-short.txt') 
for line in fhand:
    line = line.rstrip()
    if line.find('@uct.ac.za') == -1: 
        continue 
    print(line)
```
程序输出如下：
```

From stephen.marquard@uct.ac.za Sat Jan  5 09:14:16 2008
X-Authentication-Warning: set sender to stephen.marquard@uct.ac.za using -f
From: stephen.marquard@uct.ac.za
Author: stephen.marquard@uct.ac.za
From david.horwitz@uct.ac.za Fri Jan  4 07:02:32 2008
X-Authentication-Warning: set sender to david.horwitz@uct.ac.za using -f
From: david.horwitz@uct.ac.za
Author: david.horwitz@uct.ac.za
...
```





