比较运算符也适用于字符串，判断两个字符串是否相等：
```python
if word == 'banana':
    print('All right, bananas.')
```

其它比较运算符适用于字母排序：
```python
if word < 'banana':
    print('Your word,' + word + ', comes before banana.')
elif word > 'banana':
    print('Your word,' + word + ', comes after banana.')
else:
    print('All right, bananas.')
```

Python并不能像人一样区分大小写字母，所有大写字母都在小写之母之前，所以：
```python
Your word, Pineapple, comes before banana.
```
如果你要按字母顺序比较，可以将他们都转换成一种格式，都是大写或都是小写，其实更深层次的原因是ASCII编码问题，大小比较一目了然。
![](/assets/AA1A93B8-F130-4CFD-A34B-B47671907779.png)


