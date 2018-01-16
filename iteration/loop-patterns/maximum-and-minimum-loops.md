为了找出列表或序列中的最大值，我们构造了如下循环：
```python
largest = None
print('Before:', largest)
for itervar in [3, 41, 12, 9, 74, 15]:
    if largest is None or itervar > largest : 
        largest = itervar
    print('Loop:', itervar, largest)
print('Largest:', largest)
```
程序执行，输出如下：
```python
Before: None
Loop: 3 3
Loop: 41 41
Loop: 12 41
Loop: 9 41
Loop: 74 74
Loop: 15 74
Largest: 74
```
`largest`变量是"目前我们看到的最大值"，在循环开始之前，赋值`largest`为`None`，`None`是一个特殊的变量，标记这个变量为空。

在循环开始之前，我们还没有看到任何的变量，所以`largest`为None，循环开始执行的时候，如果`largest`是None，我们就将我们看到的第一个值赋给`largest`，这是目前看到的最大值，可以看到，在第一轮循环中，`itervar`为3，由于`largest`是None，所以立即将`largest`的值设为3。

第一轮迭代后，`largest`就不再为None了，所以判断条件的第二部分`itervar > largest`只有在遍历的值大于目前的最大值时才判断为真，然后将最大值赋值给`largest`。从程序的输出可以看出，`largest`的值从3变为41，然后变为74。

循环结束，我们遍历了所有的值，这个时候，`largest`已经是整个列表中的最大值了。

计算最小值的代码仅作微小改动：
```python
smallest = None
print('Before:', smallest)
for itervar in [3, 41, 12, 9, 74, 15]:
    if smallest is None or itervar < smallest: 
        smallest = itervar
    print('Loop:', itervar, smallest)
print('Smallest:', smallest)
```
同样的，smallest的值是循环前，循环中和循环后都是"目前看到的最小值"。循环结束后，smallest值就是整个列表中的最小值。

就像计数和求和有内置函数支持一样，Python内置`max()`和`min()`函数求得列表中的最大值和最小值。

下面是Python内置函数`min()`的简化版代码：
```python
def min(values): 
    smallest = None
    for value in values:
        if smallest is None or value < smallest:
            smallest = value 
    return smallest
````
在这段代码中，我们移除了所有的print语句，所以和Python内置的`min()`函数基本差不多。

