文本文件可以理解为若干文本行的序列，就像字符串可以理解为若干字符的序列一样。下面是一个文本文件示例，文件记录了一个开源项目开发中团队邮件往来的记录：
```python
From stephen.marquard@uct.ac.za Sat Jan 5 09:14:16 2008
Return-Path:  <postmaster@collab.sakaiproject.org>
Date:  Sat, 5 Jan 2008 09:12:18 -0500
To:  source@collab.sakaiproject.org
From:  stephen.marquard@uct.ac.za
Subject:  [sakai] svn commit:  r39772 - content/branches/
Details:  http://source.sakaiproject.org/viewsvn/?view=rev&rev=39772
...
```
完整的文件位置：xxxx
一个缩略版的文件位置：

这些文件以某种标准的格式存储着多条邮件信息。以`From`开头的行分割开每条邮件，已`From：`开头的行只是邮件内容的一部分。

文本文件由多行文本组成，每一行的末尾有一个特殊的字符，换行符（不可见），表示一行的结束。

在Python中，我们用`\n`表示换行符，尽管这看起来像是两个字符，但是实际上它就是一个字符，当我们在Python解释器中输入`stuff`，会得到带`\n`的字符串，但是如果我们使用print语句输出这个字符串，我们看到字符串被`\n`分割成了两行。
```python
>>> stuff = 'Hello\nWorld!'
>>> stuff
'Hello\nWorld!'
>>> print(stuff)
Hello
World!
>>> stuff = 'X\nY'
>>> print(stuff)
X
Y
>>> len(stuff)
3
```
你也发现了，字符串`X\nY`的长度是3，因为换行符也是一个字符。

所以，当我们处理文件的时候，你要意识到，有一个不可见的字符叫做换行符，它标记着每一行的结束。

总之，换行符将文本文件分割成若干行。

