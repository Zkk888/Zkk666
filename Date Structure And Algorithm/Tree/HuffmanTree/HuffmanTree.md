#赫夫曼树
###WPL(所有叶子结点的带权路径长度之和)最小的二叉树
***
####先创建节点类

```java
class Node implements Comparable<Node> {
    int value;
    Node left;
    Node right;

    public Node(int value) {
        this.value = value;
    }

    public void setLeft(Node left) {
        this.left = left;
    }

    public void setRight(Node right) {
        this.right = right;
    }

    public Node getRight() {
        return right;
    }

    public Node getLeft() {
        return left;
    }

    public void setValue(int value) {
        this.value = value;
    }

    public int getValue() {
        return value;
    }

    @Override
    public String toString() {
        return "Node[value="+value+"]";
    }
    @Override
    public int compareTo(Node o){
        return this.value-o.value;//从小到大排序
    }
    //来一个前序遍历
    public void preOrder(){
        System.out.println(this);
        if(this.left!=null){
            this.left.preOrder();
        }
        if(this.right!=null){
            this.right.preOrder();
        }
    }
}
```
****
####再创键赫夫曼树

```java
package com.Zkk666.HuffmanTree;

import java.util.ArrayList;
import java.util.Collection;
import java.util.Collections;
import java.util.List;

public class HuffmanTree {
    public static Node createHuffmanTree(int[] arr) {
        List<Node> Nodes = new ArrayList<Node>();
        //ArrayList中存放的是链表(Node只是一个节点（最小链表！！！)
        for (int value : arr) {
            Nodes.add(value);
        }
        while (Nodes.size() > 1) {
            Collections.sort(Nodes);
            System.out.println("Nodes= "+Nodes);
            Node leftNode= Nodes.get(0);
            Node rightNode= Nodes.get(1);
            Node parent = new Node(leftNode.value+rightNode.value);
            parent.left= leftNode;
            parent.right= rightNode;
            Nodes.remove(leftNode);
            Nodes.remove(rightNode);
            Nodes.add(parent);
        }
        return Nodes.get(0);
    
    }
    
    
    //前序遍历接口；
    public static void preOrder(Node root){
        if(root!=null){
            root.preOreder();
        }else{
            System.out.println("空树不能遍历");
        }
    }
    
}
```
