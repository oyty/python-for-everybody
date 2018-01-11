Python也内建了一些类型转换函数，如果可以的话，`int`函数能把任何其它类型的值转换成整数型，如果不能的话就会报错：
```python
>>> int('32')
32
>>> int('Hello')
ValueError: invalid literal for int() with base 10: 'Hello'
```

int函数可以将浮点型转换成整数型，但是它不进行四舍五入，而是直接去掉小数部分：
```python
>>> int(3.99999)
3
>>> int(-2.3)
-2
```

`float`函数能够将整数型和字符串型转换成浮点型：
```python
>>> float(32)
32.0
>>> float('3.14159')
3.14159
```

`str`也能够将传入的参数转换成字符串型：
```python
>>> str(32)
'32'
>>> str(3.14159) 
'3.14159'
```

