 #Python
 ### CH4
 
```
# #实验一
# # 定义一个复数类Complex使得下边代码可以工作
# # c1 = Complex(2,3) //用复数2+3i初始化c1  等同于Java的new 构造方法
# # c2 = Complex c2(8,-1) //用复数8-i初始化c2
# # c1.add(c2)
# # c1.show()
#!/usr/bin/python
# -*- coding:utf8 -*
 class Complex:
     def __init__(self,p1,p2):
         self._p1 = p1
         self._p2 = p2
         self._result = self.getResult()
     def getResult(self):
         self._result = str(self._p1)+"+"+str(self._p2)+"i"
         return self._result
     def getP1(self):
         return self._p1
     def getP2(self):
         return self._p2
     def add(self,comp):
         self._p1 += comp.getP1()
         self._p2 += comp.getP2()
         self._result = self.getResult()
     def show(self):
         print(self._result)

# # 测试
# c1 = Complex(2,3)
# c2 = Complex(8,-1)
# c1.add(c2)
# c1.show()

# # 实验二
# # 定义一个抽象基类Shape，Shape不需要编写数据成员和方法：
# class Shape(Object):
#     pass
# 在Shape类上派生出子类Rectangle和Circle，并在Rectangle类上派生出子类Square
# 三者都有获取周长和面积的方法getCircumference() 和getArea()
class Shape:
    pass #无内容用pass
class Rectangle(Shape):
    def __init__(self,width,height):
        self.width = width
        self.height = height
    def getCircumference(self):
        self.circumference = 2 * (self.width+self.height)
        return self.circumference
    def getArea(self):
        self.area = self.height*self.width
        return self.area
class Circle(Shape):
    def __init__(self,pi,r):
        self.pi = pi
        self.r = r
    def getCircumference(self):
        self.circumference = 2*(self.pi*self.r)
        return self.circumference
    def getArea(self):
        self.area = self.pi*self.r*self.r
        return self.area
class Square(Rectangle):
    def __init__(self,side):
        self.width = side
        self.height = side

# 测试
r1 = Rectangle(3,4)
print r1.getCircumference()
print r1.getArea()
s1 = Square(2)
print s1.getCircumference()
print s1.getArea()
c1 = Circle(3,3)
print c1.getCircumference()
print c1.getArea()

