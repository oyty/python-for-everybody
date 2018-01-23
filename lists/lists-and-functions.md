有很多内建函数可以用来遍历列表，而不需要你自己来写循环代码：
```python
>>> nums = [3, 41, 12, 9, 74, 15]
>>> print(len(nums))
6
>>> print(max(nums))
74
>>> print(min(nums))
3
>>> print(sum(nums))
154
>>> print(sum(nums)/len(nums))
25
```
只有当列表元素都是数字时，`sum()`函数才有效。其它的一些函数(max()，len()等等)对字符串列表或其它可比较的数据类型奏效。

我们来重写之前的通过用户输入列表来计算列表元素平均值的程序。

首先，不使用列表，计算输入数字的平均值：
```python
total = 0 
count = 0 
while (True):
    inp = input('Enter a number: ') 
    if inp == 'done': 
        break
    value = float(inp)
    total = total + value
    count = count + 1
average = total / count
print('Average:', average)
```
在上面这个例子中，不断地让用户输入数字，使用`count`和`total`两个变量分别来记录输入数字的个数和输入数字的总和。

现在有了更简单的方式，我们只需要记录下用户输入的数据，输入结束后，利用内建函数来计算总和和数字个数来求平均值即可。
```python
numlist = list() 
while (True):
    inp = input('Enter a number: ') 
    if inp == 'done': 
        break
    value = float(inp)
    numlist.append(value)
average = sum(numlist) / len(numlist)
print('Average:', average)
```
在循环开始之前，我们先创建一个空列表，然后每次循环，我们会得到一个数字，将该数字添加到列表中，在循环结束后，我们只需要简单的计算列表数字的和除以列表数字的个数就可以得到平均值了。


