举个例子，为了统计一个数组中的数据项个数，我们可能会写出如下for循环代码：
```python
count = 0
for itervar in [3, 41, 12, 9, 74, 15]:
    count = count + 1
print('Count: ', count)
```
在循环开始前，我们给count变量赋值0，然后我们写了一个for循环去变量数组里面的数字。迭代变量是itervar，虽然我们在循环中没有使用itervar，但是它依然控制着整个循环，让循环体为数组中的每一个值都遍历一次。

在循环体中，列表中的每一个值都会导致count加一，随着循环体的执行，count的值就是我们目前看到的遍历项的个数。

一旦循环完成，count就是遍历项的个数，另一个相似的循环是求出一组数值的总和。
```python
total = 0
for itervar in [3, 41, 12, 9, 74, 15]:
    total = total + itervar
print('Total: ', total)
```
在这个循环中，我们用到了迭代变量。不像在之前的循环中简单地为count加一，而是加上实际的数字（3，41，12等），`total`变量的作用就是记录目前位置遍历的数值的和。自爱循环开始之前，由于还没有开始遍历，所以`total`为0，在循环中累加，`total`最终值是所有数字的总和。

随着循环的进行，total累加了列表各项的和，这样的变量有时候称为**累加器**（accumulator）。

不管是计数程序还是求和程序，在实际使用都用不上，那是因为，这么基础，这么普遍的需求，Python当然提供了内置函数啊，`len()`和`sum()`分别计算列表元素的个数和列表各项的总和。






