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