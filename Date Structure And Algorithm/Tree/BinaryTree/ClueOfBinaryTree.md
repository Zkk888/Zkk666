##先创建节点
***

```java
import java.awt.*;

class HeroNode {
    private int no;
    private String name;
    private HeroNode left;  //默认null
    private HeroNode right; //默认null
    private int lefttype;   //默认0是左子树，1是前驱节点
    private int righttype;  //默认1是右子树，1是后继节点

    //*************************************************  
    //基本
    public HeroNode(int no, String name) {
        this.no = no;
        this.name = name;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getNo() {
        return no;
    }

    public void setNo(int no) {
        this.no = no;
    }

    public void setLefttype(int lefttype) {
        this.lefttype = lefttype;
    }

    public int getLefttype() {
        return lefttype;
    }

    public void setRighttype(int righttype) {
        this.righttype = righttype;
    }

    public int getRighttype() {
        return righttype;
    }

    public HeroNode getRight() {
        return right;
    }

    public HeroNode getLeft() {
        return left;
    }

    public void setRight(HeroNode right) {
        this.right = right;
    }

    public void setLeft(HeroNode left) {
        this.left = left;
    }

    //***********************************************
    //删除
    @Override
    public String toString() {
        return "HeroNode [no=" + no + ", name=" + name + "]";
    }

    public void delNode(int no) {
        if (this.left != null && this.left.no == no) {
            this.left = null;
            return;  //就return就行（JAVA特点）
        }
        if (this.righ != null && this.right.no == no) {
            this.right = null;
            return;
        }
        if (this.right != null) {
            this.right.delNode(no);
        }
        if (this.left != null) {
            this.left.delNode(no);
        }
    }

    //*****************************************************
    //遍历
    public void preOrder() {
        System.out.println(this);
        if (this.left != null) {             //经典遍历
            this.left.preOrder();
        }
        if (this.right != null) {
            this.right.preOrder();
        }
    }

    public void infixOrder() {
        if (this.left != null) {
            this.left.infixOrder();
        }
        System.out.println(this);
        if (this.right != null) {
            this.right.infixOrder();
        }
    }

    public void postOrder() {
        if (this.left != null) {
            this.left.postOrder();
        }
        if (this.right != null) {
            this.right.postOrder();
        }
        System.out.println(this);
    }

    //***********************************************    
    //查找
    public HeroNode preOrderSearch(int no) {
        System.out.println("进入前序遍历查找");
        if (this.no == no) {
            return this;
        }
        HeroNode resNode = null;  //函数返回值类型是当前类，所以定义一个当前类对象
        if (this.left != null) {     //用当前类对象接受递归
            resNode = this.left.preOrderSearch(no);
        }
        return resNode;
        if (this.right != null) {
            resNode = this.right.preOrderSearch(no);
        }
        return resNode;
    }

    public HereNode indexOrderSearch(int no){
        System.out.println("进入中序遍历查找");
        HeroNode resNode= null;
        if(this.left!=null){
            resNode= this.left.indexOrderSearch(no);
        }
        return resNode; //记得return
        if(this.no==no){
            return this;
        }
        if(this.right!=null){
            resNode= this.right.indexOrderSearch(no);
        }
        return resNode;
    }
    public HeroNode postOrderSearch(int no){
        System.out.println("进入后序遍历");
        HeroNode resNode= null;
        if(this.left!=null){
            resNode= this.left.postOrderSearch(no);
        }
        return  resNode;
        if(this.right!=null){
            resNode= this.right.postOrderSearch(no);
        }
        return resNode;
        if(this.no==no){
            return this;
        }
        return resNode;//返回当前节点的父节点
    }
//**************************************************
        
}
```
*******
##中序线索化及其中序遍历线索化二叉树
###（从左往右，从下往上）
```java
class ThreadedBinaryTree{
    private HeroNode root;
    private HeroNode pre= null;
    //线索化的思路
    //让当前节点的左指针（pre）指向前驱节点
    // （一开始左指针指向空，再指向自己）这样指向自己就成为了辅助指针
    //再通过pre的辅助指针再遍历下一个节点的时候将下一个节点设置为上一个节点的后继节点
    //node辅助指针通过回溯不断向左向上走
    //处理完当前节点后，让当前节点成为下一个节点的前驱节点（这是pre指针向左向右走的方法）
    private void setRoot(HeroNode root){
        this.root= root;
    }
    //先中序线索化
    public void threadedNodes(HeroNode node){
        if(node==null){
            return;
        }
        threadedNodes(node.getLeft());
        //*********处理当前节点*******************
        if(node.getLeft==null){
           node.setLeft(pre);//线索化第一个节点时pre=null（线索化的第一个节点是最左最下的节点）
           node.setLeftType(1);
        }
        if(pre!=null&&node.getRight()==null){ //pre!=null就是先不处理第一个节点
            pre.setRight(node);
            node.setRigtType(1);
        }
        pre= node;
        //*********处理当前节点*******************
        threadedNodes(node.getRight);
    }
    //遍历中序线索化树（怎么样线索化就怎么样遍历）
    public void threadedList(){
        HeroNode node= root;// 辅助指针
        while(node!=null){
            while(node.getLeftType==0){
                node= node.getLeft();//最左最下
            }
            System.out.println(node);
            while (node.getRightType()==1){
                node= node.getRight();
                System.out.println(node);
            }
            node= node.getRight();//碰到左右指针类型是0的父节点，直接打印再继续
        }
    }
}
```
##Demo
******
```java
package com.atguigu.tree.threadedbinarytree; 
import java.util.concurrent.SynchronousQueue;
    public class ThreadedBinaryTreeDemo {
    public static void main(String[] args) {
    //测试一把中序线索二叉树的功能 
        HeroNode root = new HeroNode(1, "tom");
        HeroNode node2 = new HeroNode(3, "jack");
        HeroNode node3 = new HeroNode(6, "smith");
        HeroNode node4 = new HeroNode(8, "mary");
        HeroNode node5 = new HeroNode(10, "king");
        HeroNode node6 = new HeroNode(14, "dim");
        //二叉树，后面我们要递归创建, 现在简单处理使用手动创建
        root.setLeft(node2);
        root.setRight(node3);
        node2.setLeft(node4);
        node2.setRight(node5);
        node3.setLeft(node6); 
        //测试中序线索化
        ThreadedBinaryTree threadedBinaryTree = new ThreadedBinaryTree();
        threadedBinaryTree.setRoot(root);
        threadedBinaryTree.threadedNodes();
        //测试: 以 10 号节点测试 
        HeroNode leftNode = node5.getLeft();
        HeroNode rightNode = node5.getRight();
        System.out.println("10 号结点的前驱结点是 =" + leftNode);
        System.out.println("10 号结点的后继结点是=" + rightNode);
        //当线索化二叉树后，能在使用原来的遍历方法 
        threadedBinaryTree.infixOrder();
        System.out.println("使用线索化的方式遍历 线索化二叉树");
        threadedBinaryTree.threadedList();
        // 8, 3, 10, 1, 14, 6
```