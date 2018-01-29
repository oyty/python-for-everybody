**习题 8.4**
从[www.py4e.com/code3/romeo.txt](/www.py4e.com/code3/romeo.txt)下载一个文本文件。
编写一个程序，打开remeo.txt文件，逐行读取，对于每一行，使用split函数将其分解为一些列的单词列表。
对于每一个单词，检查它是否已经存在于列表中，如果没有的话，就把它加进去。

程序运行完成，按字母顺序打印出这些单词。
```python
Enter file: romeo.txt
['Arise', 'But', 'It', 'Juliet', 'Who', 'already',
'and', 'breaks', 'east', 'envious', 'fair', 'grief',
'is', 'kill', 'light', 'moon', 'pale', 'sick', 'soft',
'sun', 'the', 'through', 'what', 'window',
'with', 'yonder']
```


**习题 8.5**
编写一个程序，读取邮件数据，如果遇到以From开头的行的话，就用split函数将该行分解为单词列表，我们要把第二个单词抽取出来，也就是发件人。
```
From stephen.marquard@uct.ac.za Sat Jan 5 09:14:16 2008
```
解析以From开头的行，打印出每行中的第二个单词，还可以计算以From开头的总行数，然后在最后输出总行数。
下面是部分输出：
```
python fromcount.py
Enter a file name: mbox-short.txt
stephen.marquard@uct.ac.za
louis@media.berkeley.edu
zqian@umich.edu
[...some output removed...]
ray@media.berkeley.edu
cwen@iupui.edu
cwen@iupui.edu
cwen@iupui.edu
There were 27 lines in the file with From as the first word
```


**习题 8.6**
改写之前提示用户输入一系列数字，并在用户输入done后输出最大值最小值的程序，用列表去存储这些输入数字，然后用max()和min()函数输出最大值和最小值。
```python
Enter a number: 6
Enter a number: 2
Enter a number: 9
Enter a number: 3
Enter a number: 5
Enter a number: done
Maximum: 9.0
Minimum: 2.0
```