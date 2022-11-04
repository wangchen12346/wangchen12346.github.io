---
title: python-def
tags: TeXt
article_header:
  type: cover
---
#encoding: utf-8
# def()
# 将一些语句集合在一起的部件，能够不止一次地在程序中运行。具体来说，函数能够计算出一个返回值，
# 并能够改变作为函数输入的参数，而这些参数在代码运行时也许每次都不相同。
# 它是代码最大程度的重用和最小化代码冗余而提供的最基本的程序结构，也是一种将系统分割为定义好的不同部分的工具。
# def test():
#     print('1')
# test()
# 标准库和第三方库函数，通过 import 导入模块时，会执行模块中的 def 语句

# (1)圆括号内是形式参数列表，有多个参数则使用逗号隔开
# (2)形式参数不需要声明类型，也不需要指定函数返回值类型
# (3)无参数，也必须保留空的圆括号
# (4)实参列表必须与形参列表一一对应
# 4.形式参数是在定义函数时使用的。
# 在调用函数时， 传递的参数称为“ 实际参数” ， 简称“ 实参”

# def test_01(a,b):
#     return a+b
# c = test_01(3,5)
# print(c)

# return语句就是把执行结果返回到调用的地方，并把程序的控制权一起返回
# def test_return(x):
#     if x > 0:
#         return x
#     else:
#         return 0
# print(test_return(3))


# def test_01(a,b,c=1,d=2):
#     print(a+b+c+d)
# c = test_01(3,5,2,3)

# def test_01(a,b,*c):
#     print(a,b,c)
# c = test_01(1,2,3,4,5,6)
#
#
# def test_01(a,b,**c):
#     print(a,b,c)
# c = test_01(1,2,name = "cora",age = 18)

# 对于一个嵌套定义的函数，外层的函数的返回值是内层函数，而在内层函数中又引用了外层函数的局部变量，

# 在外层函数执行后，其局部变量并非被回收，而会同返回的内层函数一同存在，而这一现象被称为闭包(closure)。
# def test(a,b,c):
#     print(a*b+c)
# test(1,1,2)
# test(1,1,3)
# 对于一个嵌套定义的函数，外层的函数的返回值是内层函数，而在内层函数中又引用了外层函数的局部变量，
#
# def test(a, b):
#     def test_in(c):
#         print(a * b + c)
#     return test_in
# num = test(1, 1)
# num(2)
# num(3)

# def fuc():
#     print('aaa')
# def fuc2():
#     print('bbb')
