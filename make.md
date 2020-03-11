#编译

##编译的依赖关系



## gcc编译选项
-I：指定头文件路径；如 gcc -I./include
-D：定义一个宏；如 gcc -DHAVE_CONFIG_H，定义宏HAVE_CONFIG_H
-Wall：开启所有错误提示，可理解为warinig all
-g：编译过程中保留调试信息，以便gdb能够调试
-O2：指定编译优化等级为2，optimization
-pipe：指定编译过程中不同阶段的通信使用pipe管道(有些编译器无法读取管道，目前GNU编译器是ok的)
-Wp,-D_FORTIFY_SOURCE=2：将逗号分隔的选项传递给预处理器，其中FORTIFY_SOURCE选项用于指定在编译时检查缓冲区溢出的等级
-fexceptions：启用异常处理，会产生额外的代码用于处理异常，会占用一定量的数据空间(gcc默认为C++打开该选项，为C关闭该选项)
-fstack-protector：开启栈保护检测，防止缓冲区异常
--param=ssp-buffer-size=4：--param用于控制一些用于优化的常量，比如内联函数的指令数量限制等，
ssp-buffer-size用于控制预防堆栈溢出的缓冲区的下限值，和-fstack-protector选项一同使用
-m64：指定生成64位的x86-64架构代码
-mtune=generic：为指定的CPU架构优化代码
-fPIC：生成位置无关的代码，适用于动态链接
-fPIE：为可执行文件生成位置无关代码
  
 
gcc在4.2版本中添加了-fstack-protector和-fstack-protector-all编译参数以支持栈保护功能，4.9新增了-fstack-protector-strong编译参数让保护的范围更广。
fstack-protector 4.2 只为局部变量中包含长度超过8Byte（含）的char数组的函数插入保护代码  
fstack-protector 4.9 满足一下三个条件都会插入保护代码：1.局部变量的地址作为赋值语句的右值或函数参数；2.局部变量包含数组类型的局部变量，不管数组的长度；3.带register声明的局部变量
