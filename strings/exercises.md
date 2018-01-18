**习题 6.5**
使用如下语句存储一个字符串：
```python
str = ’X-DSPAM-Confidence:0.8475’
```
使用find方法和字符串切片提取出字符串冒号后面的部分，然后使用float函数，将提取出来的字符串转换成浮点数。


**习题 6.6**
阅读文档`http://docs.python.org/lib/string-methods.html`，写些简单的代码，练习练习，熟悉熟悉里面的方法。`strip`和`replace`方法特别有用。

文档中的某些语法可能让人有点困惑，`find(sub[, start[, end]])`方括号里面表示可选参数，`sub`是必须的，`start`是可选的，如果包含了`start`，那么`end`是可选的。
