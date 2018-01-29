当你把一个列表传递给一个函数时，这个函数就获得了这个列表的引用。如果函数改变了这个列表参数，那么列表本身就会被改变。例如，`delete_head`删除了列表的第一个元素：
```python
def delete_head(t): 
    del t[0]
```
下面是它的用法：
```python
>>> letters = ['a', 'b', 'c']
>>> delete_head(letters)
>>> print(letters)
['b', 'c']
```
上面的参数`t`和变量`letters`是同一个对象的别名。

一定要区分那些操作是修改列表，那些是新建列表。比如，下面的示例中，`append`方法修改了列表，`+`运算符新建了一个列表：
```python
>>> t1 = [1, 2]
>>> t2 = t1.append(3)
>>> print(t1)
[1, 2, 3]
>>> print(t2)
None

>>> t3 = t1 + [3]
>>> print(t3)
[1, 2, 3]
>>> t2 is t3
False
```

在你编写修改列表的函数时，这种区别就很重要了，比如，下面的方法就没有删除列表的头部：
```python
def bad_delete_head(t):
    t = t[1:] # WRONG!
```
因为切片操作符实际上是创建了一个新的列表，赋值语句将t作为这个新列表的引用，但是作为参数传递给这个方法的列表并没有什么改变。

另一种可行的办法是编写一个函数，创建并返回一个新的列表。例如，`tail`函数返回一个新的列表，是参数列表除第一个元素外的其它所有元素。
```python
def tail(t): 
    return t[1:]
```
这个函数并不会改变原始的列表，下面是它的用法：
```python
>>> letters = ['a', 'b', 'c']
>>> rest = tail(letters)
>>> print(rest)
['b', 'c']
```

**习题 8.1**
编写chop函数，传递一个列表参数，并且修改它-删除列表的第一个和最后一个元素，返回None。

然后编写middle函数，返回一个新的列表，包含除参数列表第一个和最后一个元素的所有元素。