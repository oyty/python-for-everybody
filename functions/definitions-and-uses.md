将前面的代码片段合在一起，完整程序如下：
```python
def print_lyrics():
    print("I'm a lumberjack, and I'm okay.") 
    print('I sleep all night and I work all day.')
    
def repeat_lyrics(): 
    print_lyrics() 
    print_lyrics()
    
repeat_lyrics()
```
这个程序包含了两个自定义函数：`print_lyrics`和`repeat_lyrics`，函数定义会像其它语句一样执行，但它的作用仅仅是创建函数，函数体里面的代码并没有执行，只有函数被调用的时候，函数体才会被执行。也就是说你必须在函数第一次被调用之前就定义好函数。


**习题 4.2**
将上面程序的最后一行移到最上面，这样函数调用就在函数定义之前了，运行程序，观察出错信息。


**习题 4.3**
将函数调用移到最底部，将函数`print_lyrics`定义放在函数`repeat_lyrics`后面，看看会产生什么结果。