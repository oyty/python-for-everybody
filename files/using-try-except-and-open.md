如果用户输入的不是一个文件名呢？
```python
python search6.py
Enter the file name: missing.txt
Traceback (most recent call last):
  File "search6.py", line 2, in <module>
    fhand = open(fname)
FileNotFoundError: [Errno 2] No such file or directory: 'missing.txt'

python search6.py
Enter the file name: na na boo boo
Traceback (most recent call last):
  File "search6.py", line 2, in <module>
    fhand = open(fname)
FILES
FileNotFoundError: [Errno 2] No such file or directory: 'na na boo boo'
```
不要笑，不管是有意还是无意，用户可以做他们能做的任何事情而导致你的程序崩溃，事实上，软件开发团队中有一个重要的部分就是质量保障或测试（简称QA  Quality Assurance），这部分可能由一个人或一个小组负责，他们的工作就是尽可能地尝试破坏程序员写的程序。

在我们发布软件之前，QA的责任就是寻找程序的缺陷，可以这样说，QA团队是程序员的最佳搭档，呵呵。

现在我们可以使用rry/except结果来快速修复这个bug，我们应该假设打开文件这个操作会出错，然后添加一个修复的代码，这样打开文件出错时，程序继续正常运行：
```python
fname = input('Enter the file name: ') 
try:
    fhand = open(fname) 
except:
    print('File cannot be opened:', fname)
    exit()
count = 0
for line in fhand:
    if line.startswith('Subject:'):
        count = count + 1
print('There were', count, 'subject lines in', fname)
```
`exit()`方法会终止程序，它没有返回值。现在当用户或QA输入不正确的文件名时，我们捕获到这个异常，然后优雅修复：
```python
python search7.py
Enter the file name: mbox.txt
There were 1797 subject lines in mbox.txt

python search7.py
Enter the file name: na na boo boo
File cannot be opened: na na boo boo
```
在Python程序中，对open方法调用的保护是try/except的典型用法，这还有一个专有术语`Pythonic`，意思是Python风格，以"Python的方式"做事。上面的例子就可以说是Python风格的文件打开方式。

随着你的Python技能越来越厉害，你可能会和其他Python程序员讨论决定，结果相同的两个方案，哪一个更Pythonic，追求Pythonic的目的是为了让我们的程序变得工程性和艺术性兼备，我们不仅要让程序能够正常工作，还要让解决方案更优雅。



