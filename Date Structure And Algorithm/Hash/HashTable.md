#哈希表
##数组加链表（节点）
***
```java
//先创建雇员节点
class Emp{
    public int id;
    public String name;
    public Emp next;
    public Emp(int id,String name){
        super();
        this.id= id;
        this.name= name;
    }
}
```
###链表操作的基本步骤：
1.  while ---注意退出条件
2.  if<br>
3.  Emp curemp= head;<br>
4.  curemp=curemp.next;<br>
```java
//再创建链表
class EmpLinkedList{
    private Emp head;
    //链表的基本添加操作
    public void add(Emp emp){    //添加到哪条链表是用取模法
        if(head==null){
            head=emp;
            return;
        }
        Emp curTmp= head;
        //这个循环好！！！！
        while (true){
            if(curTmp.next== null){
                break;
            }
            curTmp= curTmp.next;
        //**************
        }
        curTmp.next= emp;
    }
    //链表的基本遍历操作
    public void list(int no){     //no就是遍历的哪条链表
        if(head==null){
            System.out.println("第"+(no+1)+" 链表为空");
            return;
        }
        System.out.println("第 "+(no+1)+" 链表的信息为");
        Emp curEmp=head;
        while (true){
            System.out.printf("=>id=%d name=%s\t",curEmp.id,curEmp.name);
            if(curEmp.next==null){
                break; //退出条件别忘了
            }
            curEmp= curEmp.next;
        }
     System.out.println();   
    }
    //链表的基本查找操作
    public Emp findEmpById(int id){
        if(head==null){
            System.out.println("链表为空");
            return null;  //因为函数有返回值类型，所以不能return;！！！！！！！！！！
        }
        Emp curemp= head;
        while (true){
            if(curemp.id==id){
                break;
            }
            if(curemp.next==null){
                curemp=null;
                break;
            }
            curemp = curemp.next;
        }
        return curemp;
    }
}
```
##创建哈希表(散列)
*****

```java
class HashTab {
    private EmpLinkedList[] empLinkedListArray;
    private int size;

    public HashTab(int size) {
        this.size = size;
        empLinkedListArray = new EmpLinkedList[size]; //注意对象数组动态分配内存用的是[]
        for (int i = 0; i < size; i++) {
            empLinkedListArray[i] = new EmpLinkedList();//必须初始化每条链表
            //回想动态创建二维数组都得初始化每个一维数组
        }
    }

    //取模法
    public int hashFun(int id) {
        return id % size;
    }

    //开始定义接口（回想树） 树是节点类定义函数，链表类定义接口
    public void add(Emp emp) {
        int empLinkedListNO = hashFun(emp.id);
        empLinkedListArray[empLinkedListNO].add(emp);
    }
    public void list(){
        for(int i=0;i<size;i++){
            empLinkedListArray[i].list(i);  //在定义链表时已经list(no);
        }
    }
    public void findEmpById(int id){
        int empLinkedListNO= hashFun(id);
        Emp emp= empLinkedListArray[empLinkedListNO].findEmpById(id);
        if(emp!=null){
            System.out.printf("在第%d 条链表中找到 雇员 id = %d\n", (empLinkedListNO + 1), id);
        }else {
            System.out.println("在哈希表中，没有找到该雇员~");
        }
    }
}
```
##接口函数都没有返回值！！！！！！！！！
##Demo

```java
package com.Zkk666.hashTab;
import java.util.Scanner;

public class HashTabDemo {
    public static void main(String[] args) {
        HashTab hashTab = new HashTab(7);

        //菜单的经典写法
        String key = "";
        Scanner scanner = new Scanner(System.in);
        while (true){
            System.out.println("add: 添加雇员");
            System.out.println("list: 显示雇员");
            System.out.println("find: 查找雇员");
            System.out.println("exit: 退出系统");
            key= scanner.next();
            switch (key){
                case"add":     //这里是字符就用单引号，字符串就用双引号
                    System.out.println("输入id");
                    int id= scanner.nextInt();
                    System.out.println("输入名字");
                    String name= scanner.next();
                    Emp emp = new Emp(id,name);
                    hashTab.add(emp);
                    break;
                case "list":
                    hashTab.list();
                    break;
                case "find":
                    System.out.println("请输入要查找的 id");
                    id = scanner.nextInt(); 
                    hashTab.findEmpById(id); 
                    break; 
                case "exit":
                    scanner.close();
                    System.exit(0);
                default:
                    break;    
            }
        }
    }
}
```