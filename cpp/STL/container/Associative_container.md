#关联容器
```
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
```aidl
构造函数
S s(q1,q2)
插入元素
s.insert(t)
s.insert(p1,t)
s.insert(q1,q2)
删除元素
s.erase(p1)
s.erase(p1,p2)
s.erase(k)   删除所有键为k的元素，返回被删元素的个数
基于键的查找和计数
s.find(k)  返回键为k的元素的迭代器，不存在则返回s.end()
```
****
##关联容器元素顺序按键的取值升序排列
```aidl
s.lower_bound(k)  返回第一个键不小于k的元素的迭代器
s.upper_bound(k)  返回第一个键大于k的元素的迭代器
s.equal_range(k)  
得到pair<S::iterator,S::iterator>记作[p1,p2)
p1==s.lower_bound(k)
p2==s.upper_bound(k)
s.count(k) 得到键为k的元素个数
```
****
9