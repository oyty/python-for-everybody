有时候条件语句有两种以上的可能，那么我们就需要两个以上的分支。链式条件可以处理这种情况。
`elif`是`else if`的缩写。
```python
if x < y:
    print('x is less than y')
elif x > y:
    print('x is greater than y')
else:
    print('x and y are equal')
```

`elif`语句的数量没有限制，`else`语句必须在链式条件的最后，但是`else`语句不是必须的。

```python
if choice == 'a': 
    print('Bad guess')
elif choice == 'b': 
    print('Good guess')
elif choice == 'c':
    print('Close, but not correct')
```



