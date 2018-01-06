一般情况下，大家起名字一定要见名知义，什么意思呢，就是你为某一个变量起的名字，你一眼看上去就知道它是干嘛的，最好别人一眼看上去也知道是干嘛的，还有呢，给一个建议吧，千万不要用拼音起名字，太low了是不是，你用有道查个单词，还能学个单词，一劳永逸的事儿，多好！

一个变量的名字可以是任意长度，可以包含字母和数字，但是不能以数字开头，用大写字母也是合法的，但是呢，好的习惯是用一个小写字母开头（原因后面会说）。

在变量名中也可以出现下划线字符（`_`），它经常出现在有多个单词的变量名中，比如`my_name`，`airspeed_of_unladen_swallow`。变量名也可以以一个下划线字符开头，但一般情况下我们避免这样做，除非你写的代码要以库（`library`）的形式给别人用。

如果变量名不合法，会有语法错误：
```python
>>> 76trombones = 'big parade' 
SyntaxError: invalid syntax
>>> more@ = 1000000
SyntaxError: invalid syntax
>>> class = 'Advanced Theoretical Zymurgy' 
SyntaxError: invalid syntax
```

`76trombones`就是不合法的，因为它以数字开头，`more@`也是不合法的，因为它包含一个不合法的字符@，但是`class`为什么也是不合法的呢？
那是因为`class`是Python的一个关键词，解释器要用到关键词去识别程序的结构，所以它们不能用作变量名。
Python中有33个关键词：
del       from       elif      global       else      
if        except     import    False        in
None      True       nonlocal  try          not
while     or         with      pass         yield
and       as         assert    break        class
continue  finally    is        raise        def
for       lambda     return

你应该把这些关键词保存在手边，如果解释器对你的一个变量名报语法错误，但是你又不知道为什么，或许你应该检查检查你的关键词列表。
