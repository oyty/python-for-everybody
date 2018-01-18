在赋值语句的左边使用[]运算符，尝试改变字符串中的字符：
```python
>>> greeting = 'Hello, world!'
>>> greeting[0] = 'J'
TypeError: 'str' object does not support item assignment
```
出错原因是字符串是不可变的，也就是说，你不能改变一个已经存在的字符串，最好的办法就是在原有的字符串基础上创建一个新的字符串。
```python
>>> greeting = 'Hello, world!'
>>> new_greeting = 'J' + greeting[1:]
>>> print(new_greeting)
Jello, world!
```
这个例子将新的首字母与greating的切片连接在一起，这不会对原先的字符串造成影响。
