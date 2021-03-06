虽然文件句柄并不包含文件数据，但是通过它我们可以很方便的读取文件内容，我们构造一个for循环来统计文件行数：
```python
fhand = open('mbox-short.txt') 
count = 0
for line in fhand:
    count = count + 1
print('Line Count:', count)
```
在for循环中，我们可以把文件句柄当做序列来使用，上面的for循环只是简单的计数了文件中的文本行数，然后打印出来。

想想，为什么open方法不读取整个文件呢？那是因为有时候我们的文件可能非常大，大到几个G，这要是一次性读出来，你的内存肯定爆满，你平时打开比较大的word或excel文件的时候是不是特别慢，因为word或excel或加载数据到内存中。但是open方法打开文件的时间是不变的，不管文件本身有多大，for循环读取了文件数据。

以for循环这种方式读取文件时，Python使用换行符将文件分割成多行，在循环迭代中，Python根据换行符读取一行，并将换行符作为一行的最后一个字符。

因为通过for循环读取文件，一次只读取一行，所以就算是很大的文件，也可以很高效的读取和计数，而无需消耗大量内存来存储数据。上面的程序可以对任意大小的文件的行数进行计数，而只需要消耗很小的内存（也就是一行的文本数据），读取完这行数据内存就释放了。

如果文件大小相对于你的内存来说很小的话，你可以使用通过文件句柄使用read方法来读取整个文件，并将文件内容赋值为一个字符串：
```python
>>> fhand = open('mbox-short.txt')
>>> inp = fhand.read()
>>> print(len(inp))
94626
>>> print(inp[:20])
From stephen.marquar
```
在上面的示例中，`mbox-short.txt`文件的整个内容(94626个字节)被直接读入到变量`inp`中。然后使用`slice`方法打印出`inp`中存储字符的前20个字符。

以这种方式打开文件，所有的字符，包括所有的文本行和换行符，作为一个整体，一个很大的字符串，存储在变量inp中，所以要记住，只有当计算机内存能够承载文件数据大小的情况，才能用这种方式打开。不过还是不建议这样做，用for循环分块读取，高效的多。

