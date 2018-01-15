**习题 4.4**
Python中`def`关键字的作用是什么？
a) 它是一个俚语，表示"下面的代码太酷了！"
b) 它表示函数的开始
c) 它表示接下来的代码的缩进部分稍后会被保存
d) b和c都正确
e) 以上都不正确


**习题 4.5**
下面的Python程序会打印出什么？
```python
def fred():
   print("Zap") 
   
def jane():
   print("ABC")
   
jane()
fred()
jane()
```
a) Zap ABC jane fred jane b) Zap ABC Zap
c) ABC Zap jane
d) ABC Zap ABC
e) Zap Zap Zap


**习题 4.6**
重写之前的工资计算程序，加班时间的工资按原工资的150%计算。创建一个computepay函数，包含两个参数hours和rate。
Enter Hours: 45
Enter Rate: 10
Pay: 475.0


**习题 4.7**
重写之前的分数计算程序，使用computegrade函数，score作为参数，返回一个评分等级的字符串。
Score
>0.9 A 
>0.8 B 
>0.7 C 
>0.6 D 
<= 0.6 F
Program Execution:
Enter score: 0.95
A
Enter score: perfect
Bad score
Enter score: 10.0
Bad score
Enter score: 0.75
C
Enter score: 0.5
F
重复运行该程序，每次输入不同的值来测试输出结果。

