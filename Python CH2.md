 #Python
 ### CH2
  ```
 

# # 实验一 冒泡排序SList
# # 用户输入？
# # SList = []
# # for i in range(5):
# #      SList = input("请输入SList：")
# # print SList
#!/usr/bin/python
# -*- coding:utf8 -*
 SList=[5,2,1,8,4,7,3,6,9]
 for i in range(0,len(SList)-1):#  i in range(3)[::-1] #从2到0倒序遍历
     for j in range(len(SList)-i-1):
         if SList[j] > SList[j+1]:
             temp = SList[j]
             SList[j] = SList[j+1]
             SList[j+1] = temp
             # SList[j],SList[j+1] = SList[j+1],SList[j] #Python中可不用临时变量
 print SList

# # 实验二 节假日字典 json序列化并保存
# import json
#
# May = {}
# for i in range(1,32):
#     if i ==1 or i==4 or i==5:
#         print 1
#         May['date' + str(i)] = str(160500+i)
#     else:
#         May['date'+str(i)] = str(160500+i)
#         print 0;
# print(May)
#
# x = May
# print '原始字典内容：',x
# y = json.dumps(x)
# print '序列化后的字典内容：',y
#
# f=open('../json/Date.json','w')
# json.dump(x,f)
# f.close()
#
# f=open('../json/Date.json','r')
# print '从文件读取到的json：',json.load(f)
# f.close()


？？？

# 实验三 txt文件数据读取
import os
data = []
dataArr = []
dataLast = []
fr = open('E:\PyCharm2017\doc\data\horseColic.txt')
for line in fr.readlines():
    # line = line.split(' ')[:-1]
    line = line.strip()  # 去掉换行符
    data_line = line.split('\t')
    dataLast.append(data_line[21])
    for i in range(21):
        dataArr.append(data_line[i])
    data.append(dataArr)
    dataArr = []
print dataLast
print data

fr.close()
# 方法2：
fd = open('E:\PyCharm2017\doc\data\horseColic.txt')
dataArr = []
labelArr = []
dt = fd.readline()
while dt:
    tmp = dt.split('\t')  #返回的就是一个列表
    dataArr.append(tmp[0:21]) # 取前21个数据
    labelArr.append(tmp[-1].strip("\n")) # 换行符在最后
    dt = fd.readline()
fd.close()
# 以上为实验三；以下打印元素，用for循环按行进行，二维列表：每一个元素都是一个列表，label打印在了最后一行
for a in dataArr:
    print(a)
    print(labelArr)

  ```
