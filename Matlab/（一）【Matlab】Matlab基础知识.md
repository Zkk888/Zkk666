

[toc]



# A MATLAB系统环境
## A.a MATLAB操作界面的组成
1 Matlab主窗口
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225164148733.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
* 功能区：提供三个选项卡（主页，绘图，应用程序），各自有不同的工具可供使用。
* 快速访问工具栏：包含一些常用按钮
* 当前文件夹工具栏：用于实现当前文件夹的操作
***
2 命令行窗口
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225164656339.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
命令行窗口用于输入命令并显示命令的执行结果。在命令提示符$>>$后输入命令并按下回车键，Matlab就会解释执行输入的命令并显示结果
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225165313252.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***
3 当前文件夹窗口
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225165444784.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225165545892.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
注意：一定要先建立文件夹，再将文件夹设为当前文件夹。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225165715889.png)

***
4 工作区窗口
是Matlab用于存储各种变量和结果的空间，可用于变量的显示和操作。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225165949976.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
在工作区以表格形式显示变量a与x的名称，取值等信息。在工作区还可以对变量进行保存、编辑、删除等操作。

***
## A.b MATLAB的搜索路径

1 用户在命令行窗口输入一条命令后，MATLAB将按照一定顺序依次寻找命令对象。
顺序（当以下都同名时）：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225170539698.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
如（clear清楚工作区的全部变量）：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225170658693.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
所以定义变量名时要避免与文件名和函数名重复。
***
2 设置文件搜索路径
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225171150978.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)

在命令行输入文件名后，MATLAB是在当前文件夹与搜索路径文件夹中寻找这个文件并执行文件内容的，所以要执行的文件必须放在这两类文件夹中。
如果两个文件夹种有同名的M文件，在命令行输入这个文件名执行顺序：当前文件夹>搜索路径文件夹
***
# B MATLAB数值数据
## B.a 数值数据类型的分类(class)
1 整形：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225173043805.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225173117852.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***
2 浮点型
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225173216509.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
class函数可以得到参数的数据类型。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225173308488.png)
***
3 复数型
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225173359365.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)

```bash
real() %求复数的实部
imag() %求复数的虚部
```

***
## B.b 数值数据的输出格式(format)
```bash
format 格式符  % 设置数据的输出格式
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225173742228.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
不同的格式符输出不同的数据格式。
注意：format命令只是影响数据输出的格式，而不影响数据的计算和存储。
***
## B.c 常用数学函数
### B.c.a 函数的调用格式

```ba
函数名（函数自变量的值）
```
函数的自变量规定为矩阵变量（标量本身是矩阵的一种特例）。
**函数在运算时是将函数逐项作用于矩阵的每个元素上**，所以最后运算的结果就是一个与自变量同型的矩阵。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225174501225.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)

***
### B.c.b 常用函数的应用(sin,sind;abs;取整)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225174641778.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225174828815.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225175107125.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)

```bash
rem(m,n)   %求m/n的余数
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225175522721.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)

```bash
isprime(n) # 判断n是否是素数，是返回1，否返回0.
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225180657183.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***
# C 变量及其操作
计算机处理的数据都是存放在内存单元中的，而每一个内存单元都有一个唯一的地址，程序就是通过这个地址来访问对应内存单元的。
在如Matlab这种高级语言中，只需要给每个内存单元取一个名字，然后通过这个名字就能访问每个内存单元了。
## C.a 变量与赋值语句
* 变量本质上讲是内存单元的一个抽象
* 在Matlab中，变量名是以字母开头，后接字母、数字或下划线的字母序列，最多63个字符。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225185102476.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
* 变量名区分大小写
* 标准函数名以及命令名必须用小写字母
***

赋值语句两种格式
```bash
变量=表达式        % 变量结果会在命令行中显示出来
变量=表达式；	  % 变量结果不会在命令行中显示出来
```
例子：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225185751144.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***
## C.b 预定义变量
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225190113487.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***
## C.c 变量的管理
### C.c.a 变量的删除和修改（who,whos）
在工作区选择变量右击即可进行删除和修改。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225190331526.png)
who命令和whos命令：
who命令只显示已存在变量的名称。而whos显示信息更多。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225190517955.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***
### C.c.b 内存变量文件(save,load)
用于保存Matlab工作区变量的文件叫做内存变量文件，其扩展名为.mat，也叫MAT文件，是一种标准的二进制格式文件。
save命令：创建内存变量文件
load命令：载入内存变量文件

```bash
save mydata a x   % 将a x保存在mydata.mat文件中
load mydata       % 载入mydata.mat中的变量
```

# D MATLAB矩阵表示
## D.a 矩阵的建立
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225192208567.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225192454699.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***
## D.b 冒号表达式(linspace)
1 用冒号产生行向量t：
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020022519264856.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***
2 用linspace函数产生行向量x:
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225192806840.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
## D.c结构矩阵和单元矩阵
### D.c.a 结构矩阵：

   在实际应用中，经常会遇到不同类型的数据项组成的实体，例如一个学生的数据实体就包括了年龄，姓名，学号，这些数据是相互联系的。结构数据类型就可以把这些数据类型不同但逻辑上相关的数据组成一个有机的整体。


```bash
结构矩阵元素.成员名=表达式
```

   例如： 学生这个结构数据包含三个成员，分别是年龄，姓名，学号，由结构数据构成的矩阵就是结构矩阵。结构矩阵里的每个元素都是结构数据类型的。即结构矩阵相当于一个班级，结构矩阵里的元素就是这个班级的学生，每个学生有年龄，姓名，学号三个信息（成员）。

 ![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225195123796.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
### D.c.b 单元矩阵
单元数据类型，也是把不同的数据放在一个变量中，但与结构矩阵所不同的是，结构矩阵的各个元素下还有成员，每个成员都有自己的名字，而单元矩阵的各个元素就是不同类型的数据，每个元素直接由不同类型的数据组成。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225200109661.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
# E 矩阵元素的引用
## E.a 矩阵元素的引用方式(sub2ind,ind2sub)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225201212298.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/202002252008579.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
如果给出的行下标和列下标大于矩阵的行数和列数，Matlab将自动扩展原来的矩阵，并将扩展后没有赋值的元素赋值为0。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225200943309.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225201114187.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225201258314.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225202516110.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225203322435.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***
## E.b 利用冒号表达式获得子矩阵(end)
子矩阵是指由矩阵中一部分元素构成的矩阵。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225203609383.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
例子:
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020022520395972.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225204124604.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***
## E.c利用空矩阵删除矩阵的元素
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225204212560.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225204254928.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***
## E.d改变矩阵的形状(reshape)
在矩阵**总元素保持不变**的前提下，将矩阵A重新排成$m*n$的二维矩阵。
```bash
reshape(A,m,n)
```
注意：reshape函数只是改变原矩阵的行数和列数，但并不改变原矩阵元素个数及其存储顺序。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225204803537.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***


![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225204859210.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)

```bash
A(:)等价于reshape(A,6,1)
```

# F MATLAB基本运算
## F.a算术运算
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225205324727.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225205433194.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)

>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225205539131.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)

>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225205645610.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225205811959.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)

>A^2=A*A![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225205913897.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020022521004121.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
例子：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225210215622.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
例题：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225210349514.png)

***
## F.b 关系运算
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225210731220.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
例题：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225210834666.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***
## F.c 逻辑运算(&,|,~)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225210947381.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
例子：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225211054779.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225211309602.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)

***

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225211400528.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
例题：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225211611641.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***
# G 字符串处理
## G.a 字符串的表示
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225213621487.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225213714464.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)

>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225213839358.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
要求各行字符数要相等（列数相同）。如果不等，就要用空格调节各行长度，使之数目相等。


>例题：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225214246795.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)

## G.b字符串的操作(strcmp;findstr;strrep)
将字符串内容作为MATLAB的命令执行
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020022521453133.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225214652808.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225215346623.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225215325522.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)


***
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200225215655578.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***

>图片来源（一个讲的不错的MATLAB课程）：
>https://www.icourse163.org/search.htm?search=%E4%B8%AD%E5%8D%97%E5%A4%A7%E5%AD%A6%20Matlab#/
