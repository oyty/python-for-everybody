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
这个程序包含了两个自定义函数：`print_lyrics`和`repeat_lyrics`，函数定义会像其它语句一样执行，但它的作用仅仅是创建函数，函数体里面的代码并没有执行，只有函数被调用的时候，函数体才会被执行。