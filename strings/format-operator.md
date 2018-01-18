格式化操作符`%`可以让我们构建字符串，使用变量中存储的数据来替换字符串的一部分。对于整数而言，`%`是模运算符，如果第一个操作对象是字符串，那么`%`就是格式操作符。

第一个操作对象是格式字符串，它包含一个或多个格式化序列，用来指定第二个操作对象的格式，处理后的结果是字符串。

例如，格式序列`%d`标示第二个操作对象会被格式化为整数（d表示10进制）：
```python
>>> camels = 42 
>>> '%d' % camels 
'42'
```
结果是字符串'42'，可不要与整数42搞混了。

格式序列在出现在字符串中的任一位置，让你可以在字符串中嵌入值。
```python
>>> camels = 42
>>> 'I have spotted %d camels.' % camels '
I have spotted 42 camels.
```

如果字符串中有多个格式序列，那么第二个参数应该是一个元组，每个格式序列与元组的元素依次对应。

下面的例子使用`%d`来格式化整型，`%g`来格式化浮点型（don't ask why），`%s`来格式化字符串：
```python
>>> 'In %d years I have spotted %g %s.' % (3, 0.1, 'camels') 
'In 3 years I have spotted 0.1 camels.'
```
元组中的元素的数量必须与字符串中的格式序列数量一致，另外，元素的类型也要与格式序列匹配。
```python
>>> '%d %d %d' % (1, 2)
TypeError: not enough arguments for format string >>> '%d' % 'dollars'
TypeError: %d format: a number is required, not str
```
第一个例子中元组中元素数量不够，第二个例子中，元素的格式不匹配。

格式运算符很强大，但是不是那么容易上手，如果要了解更多，请查看：`http://docs.python.org/lib/typesseq-strings.html`



