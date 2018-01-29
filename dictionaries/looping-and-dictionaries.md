如果你把字典作为序列用在for循环中，它遍历的是字典的键，下面的循环打印出每一个key和对应的value。
```python
counts = { 'chuck' : 1 , 'annie' : 42, 'jan': 100} 
for key in counts:
    print(key, counts[key])
```
下面是可能的输出：
```python
jan 100
chuck 1
annie 42
```
再强调一次，字典里面的键并没有特定的顺序。

我们可以将这种模式应用到之前介绍的各种常用的循环中，例如，如果你想找出一个字典中所有的值大于10的键值对，我们可以写出如下代码：
```python
counts = { 'chuck' : 1 , 'annie' : 42, 'jan': 100} 
for key in counts:
    if counts[key] > 10 : 
        print(key, counts[key])
```
for循环迭代了字典的键，所以我们使用索引操作符来检索键对应的值，下面是可能的输出：
```
jan 100
annie 42
```
我们只看到了值大于10的键值对。

如果你想按照字母顺序输出字典的键，首先使用字典方法中的`keys`方法来获得包含所有键的一个列表，然后对这个列表进行排序，遍历列表，打印出排序后的键值对：
```python
counts = { 'chuck' : 1 , 'annie' : 42, 'jan': 100}
lst = list(counts.keys())
print(lst)
lst.sort()
for key in lst:
    print(key, counts[key])
```
下面是可能的输出：
```
['jan', 'chuck', 'annie']
annie 42
chuck 1
jan 100
```
首先输出的是从`keys`方法获取的没有排序的键的列表，然后通过for循环输出有序的键值对。


