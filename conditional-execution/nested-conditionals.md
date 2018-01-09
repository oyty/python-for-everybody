一个条件语句也可以嵌套到另一个条件语句下，我们可以写出如下的三个分支的条件语句：
```python
if x == y:
    print('x and y are equal')
else:
    if x < y:
        print('x is less than y') 
    else:
        print('x is greater than y')
```