[【Matlab】](https://blog.csdn.net/weixin_44378835/category_9711268.html)

[toc]



# A 二维曲线
## A.a plot
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020022700323181.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
例子：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227003319572.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)



![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227003721579.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
图形的横坐标，是x元素的索引
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020022700385824.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227004019187.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
例子：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227004144782.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227004220857.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227004259745.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227004333235.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
例子：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227004452934.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227004645117.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
例子：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227004916472.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***
## A.b fplot
**x往往采取等间隔采样，如果在函数随着自变量的变化未知或者在不同区间的函数频率特性差别大，如果采用`plot`函数时自变量的采样间隔设置不合理，则无法反映函数的变化趋势。例如：**
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227005748457.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
如何解决这个问题呢？**——`fplot`可根据参数函数的变化特性，自适应地设置采样间隔。**
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227010039147.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
例子：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227010124555.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020022701015035.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
例子：
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020022701033143.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***
# B 绘制图形的辅助操作
## B.a 给图形添加标注
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227011336291.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
### B.a.a title函数
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227011510121.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227011541135.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227011710359.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
[LaTeX](https://blog.csdn.net/weixin_44378835/category_9689412.html)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227011918376.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***

### B.a.b xlabel函数和ylabel函数
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227012052715.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***

### B.a.c text函数和gtext函数
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227012218957.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
`gtext`函数没有坐标参数，执行命令时，十字光标跟随鼠标移动，单击鼠标，即可将说明放置在十字光标处。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227012946648.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***

### B.a.d legend函数
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227013103964.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
## B.b 坐标控制
### B.b.a axis函数
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227013158817.png)
例子：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227013343860.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227013422509.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
例子：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227015546979.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020022701571747.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
`axis equal`后，如：x轴0到1长度等于y轴0到1长度。消除因为x轴和y轴刻度长不等带来的图像变形。
ps:整个过程图形没有关闭。
***


### B.b.b 给坐标系加网格和边框(grid)

 ![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227112512666.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
grid on:控制显示网格线
grid off:控制不显示网格线
grid：在两种状态之间进行切换
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227112838366.png)  
用法同grid

***
## B.c 图形保持(hold)
在已经存在的图形叠加图形

```bash
hold on   % 控制保持原有图形
hold off  % 控制刷新图形窗口
hold      % 两种模式间切换
```
例子：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227113245355.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)

***
## B.d 图形窗口的分割(subplot)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227113441599.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
例子（显示一个子图的代码）：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227113609133.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
例子：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227114124651.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
# C 其他形式的二维图形
## C.a 其他坐标系下的二维曲线图
### C.a.a 对数坐标图(semilogx;semilogy;loglog)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227114705389.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
semilogx: x使用常用对数刻度,y为线性刻度
semilogy: y使用常用对数刻度,x为线性刻度
loglog:x,y都使用常用对数刻度
例子：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227115300724.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***
### C.a.b 极坐标图(polar)


![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227115345279.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227115455143.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***
## C.b 统计图
### C.b.a 条形类图形（bar、barh；hist、rose）
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020022711561492.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
bar:竖直条形图
barh:水平条形图
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227115755187.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
例子：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227115955138.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227120058406.png)
例题：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227120147137.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227120202432.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227120425695.png)
hist:直角坐标系
rose:极坐标系
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227120522772.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
x:用于设置统计区间的划分方式，若统计数据为标量，则统计数据均分为x个小区间，若x是向量，则x中的每一个数指定分组的中心值，元素的个数为数据分组数，x缺省时，默认按10个等分区间进行统计。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227121356310.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227121514170.png)
theta:是一个向量，绘图时将圆划分为若干个角度相等的扇形区域，每个扇形高度为落入这个扇形区域的theta个数。如果x是标量，则将0到2pi划分为x个扇形区域，默认20。
例子：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227122007908.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***

### C.b.b 面积类图形（pie;area）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227122038969.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227125938614.png)
例子：
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020022713000326.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
**`area(x, y)`：该函数以参数x和y绘制面积图。如果x和y为向量，则相当于函数plot(x, y)，并将0到y之间进行了填充。如果参数y为矩阵，则将y的每一列绘制面积图并进行叠加**。
例子：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227132909108.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)

### C.b.c 散点类图形（scatter;stairs;stem）

用法与plot类似。


![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227130115462.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227133605356.png)
**filed:填充数据点标记**
例子：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227133650504.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***

**stairs：**
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227140929123.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)


**stem：**
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227141357242.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)


## C.c 矢量图形(compass;feather;quiver)
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020022713420024.png)

**compass：**
`compass(x,y)`：x,y是n维向量，显示n个箭头，箭头的起点为原点，箭头位置为（x(i),y(i)）.
`compazz(z)`:参量z为n维复数向量，命令显示n个箭头，箭头起点为原点，箭头位置为（real(z),image(z)）。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227144435457.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)



**feather：**
feather(x,y) :函数绘制由向量参量x与y构成的速度向量，沿水平轴方向，从均匀间隔点以箭头发射出来；'
feather(z) :函数绘制羽毛图。参量z是一个复数，则feather(z)相当于compass(real(z)，imag(z))；
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227144811388.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)


![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227134229403.png)
例子：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200227134339240.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM3ODgzNQ==,size_16,color_FFFFFF,t_70)
***

[Matlab绘图(2)](https://blog.csdn.net/weixin_44378835/article/details/104535084)

>部分图片来源：
>https://www.icourse163.org/search.htm?search=%E4%B8%AD%E5%8D%97%E5%A4%A7%E5%AD%A6%20Matlab#/

