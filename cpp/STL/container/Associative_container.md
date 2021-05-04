#关联容器
### #include\<set>
### #include\<map>  
##只有这两个
```bash
简单关联容器（set  multiset）:
尖括号中的类型参数只有一个，该类型是键类型也是容器类型
二元关联容器（map  multimap）:
尖括号中的类型参数有两个，前一个是键类型，
后一个是附加数据的类型（值类型）；
元素类型是其二组合，用二元组（pair）表示。
```
##pair在\<utility>中
eg：map<int,double>的元素类型是 pair<int,double>


##set map multimap multiset（都有键类型）
##(multi后可有相同键类型的元素)
```bash
构造函数
S s(q1,q2)
单重关联容器：具有相同键元素，只有第一个元素被加入
多重关联容器：全部无条件加入
插入元素
s.insert(t)
s.insert(p1,t)
s.insert(q1,q2)
单重关联容器：不存在相同键时才成功插入，返回pair<S::iterator,bool>
                                                    类型
    成功则返回被插入元素的迭代器和true
    不成功返回与t键相同元素的迭代器和false
 ！！！pair<set<double>::iterator,bool>r = s.insert(v) !!!
      !!!  二元组访问  r.first;r.second !!!
多重关联容器：总会成功，返回插入元素的迭代器
删除元素
s.erase(p1)
s.erase(p1,p2)
s.erase(k)   删除所有键为k的元素，返回被删元素的个数
基于键的查找和计数
s.find(k)  返回键为k的元素的迭代器，不存在则返回s.end()
```
****
##关联容器元素顺序按键的取值升序排列
```bash
s.lower_bound(k)  返回第一个键不小于k的元素的迭代器
s.upper_bound(k)  返回第一个键大于k的元素的迭代器
s.equal_range(k)  :
        得到pair<S::iterator,S::iterator>记作[p1,p2)
        p1==s.lower_bound(k)
        p2==s.upper_bound(k)
s.count(k) 得到键为k的元素个数
```
****
##集合：有序、唯一
```aidl
可以用[]运算符
```
****
##映射：
```bash
s.insert(pair<string,int>("CSAPP",3))
s.insert(make_pair("CSAPP",3))  不用显式给出数据类型
可以用[]运算符   
     s[k]  查找键为k的元素，存在则返回对应附加数据的引用，不存在则插入
                   一个新元素并返回附加数据的引用
```


***********
##多重关联容器
```bash
常用：
s.equal_range(k)
s.count(k)
```
