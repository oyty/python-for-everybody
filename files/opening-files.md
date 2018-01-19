当我们想要读写一个文件的时候，首先我们要打开这个文件。打开文件与操作系统对话，才知道文件数据存储位置。当你打开文件时，你就是在让操作系统根据文件名找到文件，并确认文件是否存在。在下面的例子中，我们打开了mbox.txt文件，你可以从xxxx下载这个文件。

```python
>>> fhand = open('mbox.txt')
>>> print(fhand)
<_io.TextIOWrapper name='mbox.txt' mode='r' encoding='cp1252'>
```
如果打开文件成功，操作系统会返回一个文件句柄，这个句柄并不是文件的实际数据，但是我们通过这个句柄可以读取到文件数据。如果文件存在，你会得到一个句柄和读取该文件的相应权限。

如果文件不存在，文件打开失败，也无法获取到读取文件的句柄：
```python
>>> fhand = open('stuff.txt')
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
FileNotFoundError: [Errno 2] No such file or directory: 'stuff.txt'
```
稍后，我们会使用`try`和`except`更优雅的处理打开文件而文件不存在的情况。

