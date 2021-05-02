#顺序容器
***
##vector deque list
###  #include\<vector>
###  #include\<list>
###  #include\<deque>
```aidl
p1,p2 顾左不顾右
构造函数
S s(n,t);
S s(n);
S s(q1,q2);
赋值函数
s.assign(n,t);
s.assign(n);
s.assign(q1,q2);
插入元素
s.insert(p1,t); 在p1和p1-1之间插入
s.insert(p1,n,t); 插入n个元素
s.insert(p1,q1,q2)
删除元素
s1.erase(p1)
s1.erase(p1,p2)    返回被删元素的下一个迭代器
改变容器大小
s.resize(n)
```
```aidl
首尾元素直接访问
s.front()
s.back()   获得的是首尾元素的引用
尾部插入删除元素       头部插入删除元素
s.push_back()          s.push_front()
s.pop_back()           s.pop_front()
```
##迭代器 S=顺序容器\<T> 
###include\<iterator>
```aidl
S s1
s1 op s2
s1.begin()     s1.rbegin()
s2.end()       s2.rend()  最后元素的下一个位置||首个元素的前一个位置
s1.clear()
s1.empty()    返回布尔值，判断是否为空
s1.size()     返回元素个数
s1.swap(s2)

 S::iterator               S::reverse_iterator
 S::const_iterator         S::const_reverse_iterator

copy(s1.rbegin(),r.rend(),ostream_iterator<int>(cout,""));
 复制到输出迭代器（函数模板）中
```
##vector
```aidl
s.capacity()
s.reverse(n)  容量小于n则扩充至n，大于等于n则什么也不做
```
##list
```aidl
s1.splice(p,s2)
s1.splice(p,s2,q1)
s1.splice(p,s2,q1,q2)
```
##顺序容器的容器适配器
#stack   queue
#priority_queue
```aidl
每次弹出容器中最大的元素
不支持比较操作，有top函数获得下一个即将被弹出对象的引用
```