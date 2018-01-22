遍历列表元素最常用的方式就是使用for循环，和遍历字符串语法相同：
```python
for cheese in cheeses: 
    print(cheese)
```

如果你只需要比那里列表元素，上面就ok了，但是如果你想写入或更新元素，就需要用到索引了，常见的方式是`range`和`len`方法结合使用：
```python
for i in range(len(numbers)): 
    numbers[i] = numbers[i] * 2
```
这个循环遍历并更新列表的每个元素。len函数返回列表中元素的个数，range函数返回一个索引列表（从0到n-1，n是列表的长度），每一次循环，i就被赋值为下一个元素的索引，函数体中，使用索引i读取元素的旧值，然后再赋值为新值。

对于空列表来说，循环体是不会执行的。
```python
for x in empty:
    print('This never happens.')
```

尽管一个列表可以嵌套另一个列表，但是被嵌套的列表只是被看作一个元素，所以下面列表的长度为4。
```python
['spam', 1, ['Brie', 'Roquefort', 'Pol le Veq'], [1, 2, 3]]
```


