上面示例中使用的remeo.txt文件是在我们手动移除掉标点符号后得到的尽可能简化的文本，实际上文本中有很多标点，就像下面这样：
```
But, soft! what light through yonder window breaks?
It is the east, and Juliet is the sun.
Arise, fair sun, and kill the envious moon,
Who is already sick and pale with grief,
```

由于Python的`split`方法将单词看作是由空格分开的词单元，所以，`soft`和`soft！`会视为不同的单词，会分别为它们创建一个字典项。

同样由于文本中存在大写，所以`who`和`Who`也是不同的单词，会分别进行统计。

我们可以使用`lower`、`punctuation`和`translate`方法来同时解决上面的问题。其中`translate`方法是最精妙的，下面是它的文档：
```
line.translate(str.maketrans(fromstr, tostr, deletestr))

```



