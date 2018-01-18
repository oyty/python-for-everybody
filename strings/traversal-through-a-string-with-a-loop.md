一次处理一个字符的方式处理字符串需要花费大量的计算，通常是从字符串头部开始，然后逐个选择每个字符，对其进行操作，然后继续下一个，直到结束：
```python
index = 0
while index < len(fruit):
    letter = fruit[index]
    print(letter)
    index = index + 1
```
这个循环遍历了整个字符串，每行显示一个字母，循环的条件是`index < len(fruit)`，所以当`index`等于字符串的长度时，判断条件为`False`，循环体就不再执行，字符串的最后一个字母的索引是`len(fruit) - 1`。


**习题 6.1**
写一个`while`循环，从字符串的最后一个字母开始，反向遍历，直到第一个字母，打印出每一个字母。

遍历的另一种写法是`for`循环。
```python
for char in fruit:
    print(char)
```
循环中的每一次迭代，字符串中的下一个字符都被赋值给变量`char`，直到遍历完所有字符。

