[【Matlab】](https://blog.csdn.net/weixin_44378835/category_9711268.html)

[toc]

# A Simulink 仿真基础

## A.a Simulink的启动
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228152418624.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228152530179.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228152818220.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
## A.b 系统仿真模型的创建
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228153023490.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
Simulink的模块库分为两类：一类是基本模块库（Simulink模块库），另一类是专业模块库

>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228153350883.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228153434579.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228153511536.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)

>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228153549872.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)

>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228153656951.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
## A.c 仿真参数的设置
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228153816918.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228153958861.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228155309622.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228155335151.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228155531899.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)

# B 子系统的创建与封装
## B.a 子系统的创建
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228155836685.png)
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228160125725.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
双击它进入子模块
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228160315278.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228160629736.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)


>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228160721818.png)
选择系统的所有模块，再选择相关命令（或者Ctrl+G）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228160843904.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
所选模块，将被一个子系统取代
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228160933136.png)
***
## B.b 子系统的封装
所谓子系统的封装，就是对子系统定制对话框和图标。使得子系统本身有一个独立的操作界面。把子系统中多模块的参数设置合成在一个对话框内，这样使子系统使用更加方便。
>**先点击子系统图标**再选择命令
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228170723404.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020022816231234.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228162417227.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
重点介绍第二个选项卡
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228164247243.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
双击Edit在中间的Parameter中可以设置相应控件名的提示信息。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228164953204.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
双击子系统图标，设置参数的值
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228171009762.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228171100303.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***

## B.c 条件执行子系统
子系统的执行，依赖于其他信号，这个信号，称为控制信号.受控制信号控制的子系统，称为条件执行子系统。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228171646914.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)

>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228172024923.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
例子：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228172546812.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)



>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228172655334.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228173005307.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228173318899.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
例子：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228173940334.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020022817392722.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228174130289.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228175259899.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)

>![在这里插入图片描述](https://img-blog.csdnimg.cn/2020022817534266.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***
显示多个坐标轴:https://www.ilovematlab.cn/thread-553146-1-1.html
显示组件名:https://www.cnblogs.com/luxiaoguogege/p/11410605.html

# C S函数的设计与应用
## C.a 什么加S函数
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228180152346.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)

## C.b 用M文件编写S函数的方法
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228180348932.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
## C.c 在仿真模型中使用S函数的方法
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228180646241.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
输入参数还可以包括自定义参数；sys取决于flag的值；如果系统没有状态变量，x0为一个空阵。ts为列矩阵，一列是状态变量的采样周期，另一列是相应的采样时间的偏移量，对于连续系统，都应置为0。如果取采样周期为-1，则将继承输入信号的采样周期。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228180745349.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
flag4，9很少用；子函数不一定会全使用
***
## C.d S函数的应用
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228192000326.png)
* 主函数：timekb.m

```bash
function [sys,x0,str,ts]=timekb(t,x,u,flag,k,b)
% t:仿真时间
% x:状态向量
% u:输入向量
% flag：子函数调用标志
% sys:一种返回参数
% x0：初始状态值
% k,b:自定义变量
    switch flag
        case 0
            [sys,x0,str,ts]=mdlInitializeSizes; % flag=0时，调用初始化自函数
        case 3
            sys=mdlOutputs(t,x,u,k,b);           % flag=0时，调用输出子函数
        case {1,2,4,9}
            sys=[];
        otherwise
            error(num2str(flag))                % 出错处理
    end
```
***
* 初始化自函数mdlInitializeSize.m，定义S函数的参数，如采样时间、输入量，输出量、状态变量的个数以及其他特征。

```bash
function [sys,x0,str,ts]=mdlInitializeSizes()
    sizes=simsizes;   % 返回一个结构，为Simulink提供初始化相关信息
    % 连续状态变量个数，离散状态变量个数，输出变量个数，输入个数。
    %这四个值可以置为-1，使其大小可以动态改变。
    sizes.NumContStates=0;    % 无连续状态
    sizes.NumDiscStates=0;    % 无离散状态
    sizes.NumOutputs=1;       % 有一个输出量
    sizes.NumInputs=1;        % 有一个输入信号
    % 输入信号是否在输出端出现；模块采样周期个数，一般取1
    sizes.DirFeedthrough=1;   % 输出量中含有输入量
    sizes.NumSampleTimes=1;   % 单个采样周期
    % 给返回参数赋值
    sys=simsizes(sizes);
    x0=[];                    % 设置初始状态为零状态
    str=[];                   % 将str变量设置为空字符串
    ts=[-1,0];                % 假定继承输入信号的采样周期

```
* 输出子函数：mdlOutputs.m

```bash
function sys=mdlOutputs(t,x,u,k,b)
    sys=k*u+b;
```
以上函数，用各自函数名分别存盘，这样S函数就建好了

***
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228195753862.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
双击S-Function模块
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228200006681.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
点击S-Function模块，打开封装编辑器。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228200213629.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
双击S-Function模块
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228200331124.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)运行结果
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228204030408.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***
>图片来源：
>https://www.icourse163.org/search.htm?search=%E4%B8%AD%E5%8D%97%E5%A4%A7%E5%AD%A6%20Matlab#/

