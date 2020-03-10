# DT FUZZ
## 什么是FUZZ
Generally speaking fuzz is a brute force method which used to break software，就是用大量的测试用例一个一个试，尽可能多的找出有可能出问题的地方。
## Fuzz怎么工作?
现在有无数有名的Fuzz工具，有很多人很多还在写，一般包括四个部分。  

(1)Generate lots of malformed data as test cases，要生成大量的测试用例。这个测试用力是malformed的，一个软件首先要找到输入点，然后把数据丢进去，这个数据有可能是一个文件，有可能是一个数据包，有可能是测试表里面的一个项，有可能是临时文件里面的一个东西，总之是一种数据，要定义malformed这种非正常的数据。  

(2)Drop the test cases into product，把它丢进去，看这个产品怎么反应。  

(3)Monitor and log any crash/exception triggered by malicious input.  

(4)Review the test log, investigated deeply.  

## DT FUZZ的实现能力是什么？



