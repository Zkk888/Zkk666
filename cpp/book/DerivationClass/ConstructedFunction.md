#派生类的构造函数
*****
```java
#include<iostream>
using namespace std;
class Base1{
public:
    Base1(int i){cout<<"Constructing Base1"<<i<<endl;}
};
class Base2{
public:
    Base2(int j){cout<<"Constructing Base2"<<j<<endl;}
};
class Base3{
public:
    Base3{cout<<"Constructing Base3"<<endl;}    
};



class Derived:public Base2,public Base1,public Base3{
public:
    Derived(int a,int b,int c,int d):Base1(a),member2(d),member1(c),Base2(b)
    {}
private:
    Base1 menber1;
    Base2 member2;
    Base3 member3;
};



int main(){
    Derived obj(1,2,3,4);
    return 0;
        }
```

###派生类的构造函数作用是初始化基类和内嵌对象成员<br>
###对基类初始化的时候，需要调用基类的带有形参表的构造函数的时候，派生类就必须声明构造函数（即当基类构造函数有显式形参时派生类需要声明构造函数）<br>
###派生类先调用基类构造函数再调用内嵌对象（派生类新增成员对象）的构造函数
###派生类调用基类构造函数顺序是派生类定义时给出的继承基类的顺序，调用内嵌对象构造函数顺序是成员在类中声明的顺序（与初始化列表无关）
##New:既是初始化基类（基类构造函数有显式形参的时候）
