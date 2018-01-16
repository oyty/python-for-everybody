有时候我们需要遍历一组东西，比如，单词列表，文件中的每一行或是一组数字。要遍历这样一组东西，可以使用for语句来构造循环。因为while语句只是简单地进行循环，知道条件变为False，与之不同的是，for语句是对已知的数据项集合进行循环，因为它的迭代次数取决于数据项的个数。

for循环和while循环的语法相似，下面是一个for语句的循环体代码示例：
```python
friends = ['Joseph', 'Glenn', 'Sally'] 
for friend in friends:
    print('Happy New Year:', friend)
print('Done!')
```
在Python语法中，friends变量是包含三个字符串的数组，for循环遍历整个数组，依次打印每个字符串，输出结果如下：
```python
Happy New Year: Joseph
Happy New Year: Glenn
Happy New Year: Sally
Done!
```

直接来白话解释for循环不像while循环那么直接，你可以把它当做是一个朋友名单，那么这段代码的作用是：对friends集合中的每个朋友执行for循环体。
```python
for friend in friends:
    print('Happy New Year:', friend)
```
具体来说，friend是for循环的迭代变量，变量friend的值每次迭代时都会改变，并且控制着for循环什么时候结束。

