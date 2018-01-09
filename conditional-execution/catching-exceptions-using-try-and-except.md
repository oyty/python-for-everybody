之前我们看到过一段代码，使用`raw_input`和`int`函数读取和解析用户输入的整数，直接这样做呢会有潜在的危险：
```python
>>> prompt = "What...is the airspeed velocity of an unladen swallow?\n"
>>> speed = input(prompt)
What...is the airspeed velocity of an unladen swallow?
What do you mean, an African or a European swallow?
>>> int(speed)
ValueError: invalid literal for int() with base 10: 
>>>
```
当我们在命令行中执行上面代码的时候，Python解释器会提示错误，然后另起一行。

如果上面代码是在Python的脚本文件中，当错误发生时，程序就会立即停止执行，并返回错误信息，后面的语句会不会被执行了。

```python
inp = input('Enter Fahrenheit Temperature: ')
fahr = float(inp)
cel = (fahr - 32.0) * 5.0 / 9.0
print(cel)
```
如果我们执行上面程序，然后输入一个不合法的数值：
```python
python fahren.py
Enter Fahrenheit Temperature:72
22.22222222222222

python fahren.py
Enter Fahrenheit Temperature:fred
Traceback (most recent call last):
  File "fahren.py", line 2, in <module>
    fahr = float(inp)
ValueError: could not convert string to float: 'fred'
```

Python内置了`try/except`条件执行结构，用来捕获意料之中和意料之外的异常。如果你觉得某一段程序可能出现问题，并希望在出现这种问题的时候做一些异常处理，那么`try/except`就派上用场了。如果程序没有出错，那么`except`里面的语句块就会被忽略掉。
你可以把`try/except`功能看作是程序的保险单。

here we are:
```python
inp = input('Enter Fahrenheit Temperature:') try:
    fahr = float(inp)
    cel = (fahr - 32.0) * 5.0 / 9.0
    print(cel)
except:
    print('Please enter a number')
```
Python首先执行`try`语句块，如果一切顺利，它就会跳过`except`语句块，如果在`try`语句块里面发生意外，Python就会跳出`try`语句块，执行`except`语句块。

```python
python fahren2.py
Enter Fahrenheit Temperature:72
22.22222222222222

python fahren2.py
Enter Fahrenheit Temperature:fred
Please enter a number
```
用`try`语句处理异常的行为成为异常捕获，这个示例中，`except`语句打印了一条错误提示信息，一般来说，捕获到异常，就是给你一个机会去解决它，或者重新走一遍逻辑，至少程序能正常执行，结束。






