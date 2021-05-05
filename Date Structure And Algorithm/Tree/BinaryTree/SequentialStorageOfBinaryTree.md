#给一个数组，以树的前中后序遍历方式遍历
*****
```java
//前序遍历
class ArrBinaryTree{
    private int[] arr;
    public ArrBinaryTree(int[] arr){
        this.arr= arr;
    }
    public void preOrder(int index){
        if(arr==null||arr.length==0){
            System.out.println("数组为空，不能前序遍历");
        }
        System.out.println(arr[index]);
        if((index*2+1)<arr.length){
            this.preOrder(2*index+1);
        }
        if((index*2+2)<arr.length){
            preOrder(2*index+2); //因为作用对象就是this,
                                 // 不是this.root啥的，
                                 // 所以可以省略this
        }
    }
    public void preOrder(){
        this.preOrder(0);
    }
}
```
*****

```java
//Demo
package com.Zkk666.tree;

import java.net.PortUnreachableException;

public class ArrBinaryTreeDemo {
    public static void main(String[] args){
        int[] arr= {1,2,3,4,5,6,7};
        ArrBinaryTree arrbinarytree= new ArrBinaryTree(arr);
        //arrbinarytree.preOrder(0);
        arrbinarytree.preOrder();
        //重写preOreder()，将传参写入函数中，可以避免每次使用函数都传参
    }
}
```