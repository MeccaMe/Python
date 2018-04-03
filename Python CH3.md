# Python
Learning Python
### CH3 函数
用递归算法算斐波那契数列第n项
 ```
 #!/usr/bin/python
 # -*- coding:utf8 -*
 import  math
 def Fibonacci(n):
     if n <= 1:
         return 1
     else:
         return (Fibonacci(n-1) + Fibonacci(n-2))
 num = input("请输入项数：")
 if num <= 0:
     print "请输入正数"
 else:
     print "斐波那契数列："
     for i in range(num):
         print(Fibonacci(i))
  ```
 
