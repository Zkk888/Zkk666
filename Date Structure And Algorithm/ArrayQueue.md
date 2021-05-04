#数组模拟队列
***
```java
class ArrayQueue{
    private int maxSize;
    private int front;
    private int rear;
    private int[] arr;  //四要素
    
    //构造函数
    public ArrayQueue(int arrMaxSize){
        maxSize= arrMaxSize;
        arr= new int[maxSize];
        front= -1;
        rear= -1;    //构造函数中直接操作数据成员
    }
    //成员函数实现队列的功能
    public boolean isFull(){
        return rear == maxSize-1;
    }
    public  boolean isEmpty(){
        return rear == front;
    }
    public void addQueue(int n){
        if(isFull()){
            System.out.println("队列满，不能添加数据");
            return;
        }
        rear++;
        arr[rear]= n;  //经典队列添加数据的方法（从队尾加）
    }
    public int getQueue(){
        if(isEmpty()){
            throw new RuntimeException("队列空，不能取数据");
        }   //常用抛出异常
        fornt++;
        return arr[front];  //经典队列取出数据的方法（从队头取）
    }
    public void showQueue(){
        if(isEmpty()){
            System.out.println("队列空，没有数据");
            return;
        }
        for(int i= 0;i<arr.length;i++){
            System.out.printf("arr[%d]= %d]\n",i,arr[i]);
        }
    }
    public int headQueue(){  //显示不取出队头数据
        if(isEmpty()){
            throw new RuntimeException("队列空，没有数据");
        }
        return arr[front+1];
    }
}
```
##举例应用

```java
package com.Zkk666.queue;

import java.lang.reflect.Array;
import java.util.Scanner;

public class ArrayQueueDemo() {
    public static void main(String[] args) {

        ArrayQueue queue = new ArrayQueue(3);
        char key = "";  //用来接受扫描器扫描到的输入
        Scanner scanner = new Scanner(System.in);
        boolean loop = true;  //经典菜单写法
        while (loop) {
            System.out.println("s(show): 显示队列");
            System.out.println("e(exit): 推出程序");
            System.out.println("a(add): 添加数据到队列");
            System.out.println("g(get): 从队列取出数据");
            System.out.println("h(head): 查看队列头的数据");
            key = scanner.next().charAt(0);//接受一个字符
            switch (key) {
                case 's':
                    queue.showQueue();
                    break;
                case 'a':
                    System.out.println("添加的数据是：");
                    int value = scanner.nextInt();
                    queue.addQueue(value);
                    break;
                case 'g':
                    try {
                        int res = queue.getQueue();
                        System.out.printf("取出的数据是%d\n", res);
                    } catch (Exception e) {
                        System.out.println(e.getMessage());
                    }
                    break;  //经典try-catch
                case 'h':
                    try {
                        int res = queue.headQueue();
                        System.out.printf("队列头的数据是%d\n", res);
                    } catch (Exception e) {
                        System.out.println(e.getMessage());
                    }
                    break;
                case 'e':
                    scanner.close();
                    loop = false;
                    break;
                default:
                    break;
            }
        }
        System.out.println("程序退出");
    }
}
```