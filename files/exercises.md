**习题 7.1**
编写一个程序，读取一个文件，然后以大写方式逐行打印文件内容，程序运行结果如下：
```python
python shout.py
Enter a file name: mbox-short.txt
FROM STEPHEN.MARQUARD@UCT.AC.ZA SAT JAN  5 09:14:16 2008
RETURN-PATH: <POSTMASTER@COLLAB.SAKAIPROJECT.ORG>
RECEIVED: FROM MURDER (MAIL.UMICH.EDU [141.211.14.90])
     BY FRANKENSTEIN.MAIL.UMICH.EDU (CYRUS V2.3.8) WITH LMTPA;
     SAT, 05 JAN 2008 09:14:16 -0500
```

你可以从下面地址下载文件：
[](/www.py4e.com/code3/mbox-short.txt)


**习题 7.2**
编写一个程序，让用户自己输入文件名，然后读取文件，寻找下面格式：
```
X-DSPAM-Confidence:0.8475
```
遇到以`X-DSPAM-Confidence:`开头的行，提取改行中的浮点数，读取完文件后，计算所有浮点数的平均数：
```python
Enter the file name: mbox.txt
Average spam confidence: 0.894128046745

Enter the file name: mbox-short.txt
Average spam confidence: 0.750718518519
```
用`mbox.txt`和`mbox-short.txt`文件测试你的结果。




