当我们要处理不同的文件的时候，我们是真的不想每次都修改代码啊，所以让用户自己输入文件名是很有必要的，这样在不改动我们代码的情况下，用户可以处理不同的文件。

这个就很简单了，直接使用input方法读取用户输入的文件名：
```python
fname = input('Enter the file name: ') 
fhand = open(fname)
count = 0
for line in fhand:
    if line.startswith('Subject:'): 
        count = count + 1
print('There were', count, 'subject lines in', fname)
```
我们读取用户输入的文件名赋值给fname，然后打开文件，现在我们就可以对不同的文件重复运行我们的程序了：
```python
python search6.py
Enter the file name: mbox.txt
There were 1797 subject lines in mbox.txt

python search6.py
Enter the file name: mbox-short.txt
There were 27 subject lines in mbox-short.txt
```
在进入下一小节之前，再看看上面的程序，然后问问你自己，"程序可能会出现什么错误呢？"，或者"我们那友好的用户可能做了什么而导致这精巧的程序奔溃呢？"
