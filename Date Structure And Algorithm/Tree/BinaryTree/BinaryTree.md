#二叉树
****
##创建HeroNode节点
****

```java
import java.util.HashMap;

class HeroNode {
    private int no;
    private String name;
    private HeroNode left;
    //默认null
    private HeroNode right;
    //默认null

    public HeroNode(int no, String name) {
        this.no = no;
        this.name = name;
    }

    public int getNo() {
        return no;
    }

    public void setNo(int no) {
        this.no = no;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public HeroNode getLeft() {
        return left;
    }

    public void setLeft(HeroNode left) {
        this.left = left;
    }

    public HeroNode getRight() {
        return right;
    }

    public void setRight(HeroNode right) {
        this.right = right;
    }

    @Override
    public String toString() {
        return "HeroNode [no=" + no + ", name=" + name + "]";
    }
//**************************************************************
    //编写前中后序遍历的方法（递归）

    public void preOrder() {
        System.out.println(this);
        if (this.left != null) {
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
        System.out.println(this);//把每一个节点当做该部分树的父节点
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
        System.out.println(this);//把每一个节点当做该部分树的父节点
    }

//***********************************************************
    //前中后序查找遍历的方法（递归）
    public HeroNode preOrderSearch(int no) {
        System.out.println("进入前序遍历查找");
        if (this.no == no) {
            return this;  //操作对象是节点
        }
        HeroNode resNode = null;   //辅助指针
        if (this.left != null) {
            resNode = this.left.preOrderSearch(no);
            //一直有两个指针this和resNode
        }
        if (resNode != null) {
            return resNode;
        }
        if (this.right != null) {
            resNode = this.right.preOrderSearch(no);
        }
        if (resNode != null) {
            return resNode;
        }
    }

    public HeroNode infixOrderSearch(int no) {
        System.out.println("进入中序遍历查找");
        HeroNode resNode = null;
        if (this.left != null) {
            resNode = this.left.infixOrderSearch(no);
        }
        if (resNode != null) {
            return resNode;
        }
        //递归完最后回这查找
        if (this.no == no) {
            return this;
        }
        if (this.right != null) {
            resNode = this.right.infixOrderSearch(no);
        }
        if (resNode != null) {
            return resNode;
        }
    }

    public HeroNode postOrderSearch(int no) {
        System.out.println("进入后序遍历查找");
        HeroNode resNode= null;
        if(this.left!=null){
            resNode= this.left.postOrderSearch(no);
        }
        if(resNode!=null){
            return resNode;
        }
        if(this.right!=null){
            resNode= this.right.postOrderSearch(no);
        }
        if(resNode!=null){
            return resNode;
        }
        //最后回这儿查找
        if(this.no==no){
            return this;
        }
        return resNode; //找到的节点的父节点
    }
//***************************************************************
    //删除的是叶子节点
    //单向树，只能找到要删除节点的父节点，然后将其删除
//**** 因为只有父节点有指针!!!要删除的节点只有this**********
    public void delNode(int no){  
        if(this.left!=null&&this.left.no==no){
            this.left= null;
            return;
        }
        if(this.right!=null&&this.right.no==no){
            this.right= null;
            return;
        }
 //如果是子树就得递归把子树的所有节点都删除
        if(this.left!=null){
            this.left.delNode(no);
        }
        if(this.right!=null){
            this.right.delNode(no);
        }
    }
}

```
****
##创建二叉树
```java
class BinaryTree {
    private HeroNode root;

    public void setRoot(HeroNode root) {
        this.root = root;
    }
 //*************************************************************

    //前中后序遍历的树类接口
    public void preOrder() {
        if (this.root != null) {
            this.root.preOrder(); //接口给一个root节点
        } else {
            System.out.println("二叉树为空，无法遍历");
        }
    }

    public void infixOrder() {
        if (this.root != null) {
            this.root.infixOrder();
        } else {
            System.out.println("二叉树为空，无法遍历");
        }
    }

    public void postOrder() {
        if (this.root != null) {
            this.root.postOrder();
        } else {
            System.out.println("二叉树为空，无法遍历");
        }
    }
 //*********************************************************


    //前中后序遍历查找的树接口
    public HeroNode preOrdeSearch(int no) {
        if (root != null) {
            return root.preOrderSearch(no);
        } else {
            return null;
        }
    }
    public HeroNode infixOrderSearch(int no){
        if(root!=null){
            return root.infixOrderSearch(no);
        }else {
            return null;
        }
    }
    public HeroNode postOrderSearch(int no){
        if(root!=null){
            return root.postOrderSearch(no);
        }else {
            return null;
        }
    }
//*****************************************************    
    
}
```
****
##二叉树应用

```java
package com.Zkk666.tree;
public class BinaryTreeDemo {
    public static void main(String[] args) {
        BinaryTree binaryTree = new BinaryTree();
        HeroNode root= new HeroNode(1,"宋江");
        HeroNode node2= new HeroNode(2,"吴用");
        HeroNode node3= new HeroNode(3,"卢俊义");
        HeroNode node4 = new HeroNode(4, "林冲");
        HeroNode node5 = new HeroNode(5, "关胜");
        root.setLeft(node2);
        root.setRight(node3);
        node3.setRight(node4);
        node3.setLeft(node5); 
        binaryTree.setRoot(root);  //把链表'树'起来
        //测试 
        System.out.println("前序遍历");// 1,2,3,5,4 
        binaryTree.preOrder(); 
        //测试 
        System.out.println("中序遍历"); 
        binaryTree.infixOrder();// 2,1,5,3,4
        //测试
        System.out.println("后序遍历"); 
        binaryTree.postOrder(); // 2,5,4,3,1
 //******************************************************  
        //返回resNode，就定义一个resNode接受
        //前序遍历
        // 前序遍历的次数 ：4 
        System.out.println("前序遍历方式~~~");
        HeroNode resNode = binaryTree.preOrderSearch(5);
        if (resNode != null) {
            System.out.printf("找到了，信息为 no=%d name=%s", resNode.getNo(), resNode.getName());
        } else {
            System.out.printf("没有找到 no = %d 的英雄", 5);
        }
        //中序遍历查找 
        //中序遍历 3 次 
        System.out.println("中序遍历方式~~~");
        HeroNode resNode = binaryTree.infixOrderSearch(5);
        if (resNode != null) {
            System.out.printf("找到了，信息为 no=%d name=%s", resNode.getNo(), resNode.getName());
        } else {
            System.out.printf("没有找到 no = %d 的英雄", 5);
        }
        //后序遍历查找 
        //后序遍历查找的次数 2 次 
        System.out.println("后序遍历方式~~~");
        HeroNode resNode = binaryTree.postOrderSearch(5);
        if (resNode != null) {
            System.out.printf("找到了，信息为 no=%d name=%s", resNode.getNo(), resNode.getName());
        } else {
            System.out.printf("没有找到 no = %d 的英雄", 5);
        }
    }

}
```

