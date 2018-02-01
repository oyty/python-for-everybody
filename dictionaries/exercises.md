**习题 9.2**
编写一个程序，按照接收的星期时间对邮件进行分类，首先找出以"From"开头的行，然后找到每一行中的第三个单词，使用一个计数器统计一周中每一天的邮件被接收的次数。最后输出字典的内容（不要求顺序）。
```

Sample Line:

    From stephen.marquard@uct.ac.za Sat Jan  5 09:14:16 2008

        
Sample Execution:

python dow.py
Enter a file name: mbox-short.txt
{'Fri': 20, 'Thu': 6, 'Sat': 1}
```


**习题 9.3**
编写一个程序，读取邮件日志，使用字典来创建一个直方图，来统计每个邮箱发出的邮件数量，打印出这个字典。
```
Enter file name: mbox-short.txt
{'gopal.ramasammycook@gmail.com': 1, 'louis@media.berkeley.edu': 3,
'cwen@iupui.edu': 5, 'antranig@caret.cam.ac.uk': 1,
'rjlowe@iupui.edu': 2, 'gsilver@umich.edu': 3,
'david.horwitz@uct.ac.za': 4, 'wagnermr@iupui.edu': 1,
'zqian@umich.edu': 4, 'stephen.marquard@uct.ac.za': 2,
'ray@media.berkeley.edu': 1}

```


**习题 9.4**
在上述程序中添加代码，找出谁的邮件多。
读完所有数据并创建完字典后，使用最大循环对字典进行遍历，找出谁的邮件最多，并输出他的邮件总数。
```
python schoolcount.py
Enter a file name: mbox-short.txt
{'media.berkeley.edu': 4, 'uct.ac.za': 6, 'umich.edu': 7,
'gmail.com': 1, 'caret.cam.ac.uk': 1, 'iupui.edu': 8}
```
