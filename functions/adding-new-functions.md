目前为止，我们只是使用了Python的内置函数，我们也可以定义添加自己的新函数。通过定义函数名和一组语句序列来定义一个新函数，然后在执行时调用这个函数，一旦定义了一个函数，程序中就可以重复使用。
```python

def print_lyrics():
    print("I'm a lumberjack, and I'm okay.") 
    print('I sleep all night and I work all day.')
```
`def`是定义函数的关键字，这个函数的名称是`print_lyrics`，函数命名和变量名命名的规则基本上是一样的：字母、数字以及一些符号，然后函数名的第一个字符不能是数字，不能使用保留关键字命名函数，也要避免函数名和变量名相同。

函数名后面的空括号表明这个函数没有指定参数，一会儿，我们定义有参数的函数。

函数定义的第一行叫做`标题（header）`，剩下的叫做`函数体（body）`，标题需要以冒号结尾，内容需要缩进。按照约定，缩进一般都是四个空格，内容部分可以包含任意数量的语句。

输出语句中的字符串是以双引号包裹的，单引号和双引号都可以，效果是一样的，很多人习惯用单引号，但是有一种情况例外，必须使用双引号，就是字符串中出现单引号的时候，比如第一个输出语句。

如果你在命令行下定义函数，Python解释器会输出`虚点(...)`告诉你，函数定义还没有完成。
```python
>>> def print_lyrics():
...     print("I'm a lumberjack, and I'm okay.")
...     print('I sleep all night and I work all day.')
...
```
函数定义的结束方式是输入一个空行（当然了，这在程序文件中不是必须的）。

定义函数同时也会创建一个和函数名相同的变量名：
```python
>>> print(print_lyrics)
<function print_lyrics at 0xb7e99e9c> >>> print(type(print_lyrics))
<class 'function'>
```
print_lyrics的值是一个函数对象，对象的值是函数在内存中的地址，类型是函数。

调用自定义函数和调用内建函数是一样的：
```python
>>> print_lyrics()
I'm a lumberjack, and I'm okay.
I sleep all night and I work all day.
```
一旦你定义了一个函数，你可以在另一个函数中调用这个函数，比如为了重复调用之前的函数，你可以写一个repeat_lyrics的函数：
```python
def repeat_lyrics(): 
    print_lyrics() 
    print_lyrics()
```
然后调用这个函数：
```python

>>> repeat_lyrics()
I'm a lumberjack, and I'm okay.
I sleep all night and I work all day.
I'm a lumberjack, and I'm okay.
I sleep all night and I work all day.
```




