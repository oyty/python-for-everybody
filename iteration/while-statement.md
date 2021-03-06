计算机经常要执行一些重复性的任务，对于计算机来说，执行相同或相似的任务而不出错，这很简单，但是人就很难做到。因为迭代(也可叫做遍历)很常见，所以Python提供了一些功能语句，让这类任务变得更加简单。

其中一种迭代形式是`while`语句，下面是一个简单的程序，从5开始倒数，然后打印"Blastoff"：
```python
n=5
while n > 0:
    print(n)
    n=n-1 
print('Blastoff!')
```
你几乎可以像读英文一样读出这条语句，它的意思是：当n大于0时，显示n的值，然后n减1.当n等于0的时候，打印"Blastoff"。

严格来说，`while`语句的执行流程如下：
+ 计算条件表达式的值，判断是`True`还是`False`。
+ 如果为False，结束while语句，然后执行下一条语句。
+ 如果为True，执行语句体，然后继续执行步骤一。

这类执行流程称为循环，，每执行一次循环体，称为一次迭代，上面的流程，我们可以说"它进行了5次迭代"，表示循环体被执行了5次。

循环体会改变一个或多个变量的值，这样判断条件不满足时，循环结束。有一种变量在每次循环执行时其值都会改变，并控制循环什么时候结束，这种变量成为迭代变量。如果没有迭代变量，循环就会一直执行下去，导致无限循环。



