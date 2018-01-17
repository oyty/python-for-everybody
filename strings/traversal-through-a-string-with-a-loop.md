一次处理一个字符的方式处理字符串需要花费大量的计算，通常是从字符串头部开始，然后逐个选择每个字符，对其进行操作，然后继续下一个，直到结束：
```python
index = 0
while index < len(fruit):
    letter = fruit[index]
    print(letter)
    index = index + 1
```