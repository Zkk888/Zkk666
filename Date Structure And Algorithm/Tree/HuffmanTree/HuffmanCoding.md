1.创建Node类<br/>
2.创建getnodes<br/>获得data对应的byte和字频
3.创建createHuffmanTree<br/>
4.getcodes<br/>
5.zip<br/>
6.封装函数<br/>
##收获：可以封装函数，再在主函数里定义变量接受函数的返回值
1.主函数：byte[] contentBytes = content.getBytes();<br/>
2.Node类：Comparable重写compareTo函数、Byte类<br/>
3.getNodes()：ArrayList、Map、<br/>for (Map.Entry<Byte, Integer> entry : counts.entrySet()) {
nodes.add(new Node(entry.getKey(), entry.getValue()));分别为data和weight<br/>
4.createHuffmanTree；Collection.sort(nodes);<br/>
5.getCodes()：StringBuilder stringBuilder2= new StringBuilder(stringBuilder);
stringBuilder2.append(code);<br/>
6.zip：stringBuilder.substring()<br/>
huffmanCodeBytes[index] = (byte)Integer.parseInt(strByte,2);
****
##Nodes类

```java
package com.Zkk666.Huffmancoding;

import javax.xml.stream.events.NotationDeclaration;
import java.nio.charset.StandardCharsets;
import java.util.*;

public class Huffmancode {
    public static void main(String[] args) {
        String content = "i like like like java do you like a java";
        byte[] contentBytes = content.getBytes();
        //大封装后
        byte[] huffmanCodeBytes = huffmanZip(contentBytes);
        
        
        
        
        
        
        //大封装前
        System.out.println(content.length());
        //测试getNodes()
        List<Node> nodes = getNodes(contentBytes);
        System.out.println("nodes=" + nodes);
        //测试createHuffmanTree()
        System.out.println("赫夫曼树");
        Node huffmanTreeRoot= creatHuffmanTree(nodes);
        System.out.println("前序遍历");
        huffmanTreeRoot.preOrder();
        //测试huffmanCodes和stringbuilder
        /*getCodes(huffmanTreeRoot,"",stringBUilder);
        System.out.println("生成的赫夫曼编码表"+huffmanCodes);
        */
        //测试重载getCodes
        Map<Byte,String> huffmanCodes= getCodes(huffmanTreeRoot);
        System.out.println("生成的赫夫曼编码表"+huffmanCodes);
        //测试压缩第一步
        zip(contentBytes,huffmanCodes);
        //测试压缩第二步
        System.out.println("huffmanCodeBytes= " + Arrays.toString(huffmanCodeBytes));
    }
}
//*****************************************************

class Node implements Comparable<Node> {
    Byte data;
    int weight;
    Node left;
    Node right;

    public Node(Byte data, int weight) {
        this.data = data;
        this.weight = weight;
    }

    @Override
    public int compareTo(Node o) {
        return this.weight - o.weight;
    }

    public String toString() {
        return "Node[data=" + data + "weight=" + weight + "]";
    }

    public void preOrder() {
        System.out.println(this);
        if (this.left != null) {
            this.left.preOrder();
        }
        if (this.right != null) {
            this.right.preOrder();
        }
    }

    //__________________________________________________________________

    private static List<Node> getNodes(byte[] bytes) {
        ArrayList<Node> nodes = new ArrayList<Node>();
        Map<Byte, Integer> counts = new HashMap<>(); //存放data和字频
        for (byte b : bytes) {
            Integer count = counts.get(b);
            if (count = null) {
                counts.get(b, 1);
            } else {
                counts.get(b, count + 1);
            }
        }
        for (Map.Entry<Byte, Integer> entry : counts.entrySet()) {
            nodes.add(new Node(entry.getKey(), entry.getValue()));
        }
        return nodes;
    }

    // _________________________________________________________________
    private static Node createHuffmanTree(List<Node> nodes) {
        while (nodes.size() > 1) {
            Collection.sort(nodes);
            Node leftNode = nodes.get(0);
            Node rightNode = nodes.get(1);
            Node parent = new Node(null, leftNode.weight, rightNode.weight);
            parent.left = leftNode;
            parent.right = rightNode;
            nodes.add(parent);
        }
        return nodes.get(0);
    }
    //__________________________________________________________________
    static Map<Byte,String> huffmanCodes= new HashMap<Byte,String>(); //存放data和Codes（每个节点的Codes用stringbuilder存储）
    static StringBuilder stringBuilder=new StringBuilder();
    private static getCodes(Node node,String code,StringBuilder stringBuider){
        StringBuilder stringBuilder2= new StringBuilder(stringBuilder);
        stringBuilder2.append(code);
        if(node!=null){
            getCodes(node.left,"0",stringBuilder2);
            getCodes(node.right,"1",stringBuilder2);// 因为要递归所以得有stringbuilder参数
        }else {
            huffmanCodes.put(node.data,stringBuilder2.toString());
        }
    }
    //重载getCodes
    private static Map<Byte,String> getCodes(Node root){
        if(root==null){
            return null;
        }
        getCodes(root.left,"0",stringBuilder);
        getCodes(root.right,"1",stringBuilder);
        return huffmanCodes;
    }
    //通过赫夫曼编码表将字符串对应的byte[]数组压缩
    //原码补码反码
    /*正整数全部一样，
            负整数原码除符号位每位二进制取反得反码，反码最低位加1得补码
     */
    private static void zip(byte[] bytes,Map<Byte,String> huffmancodes){
        StringBuilder stringBuilder = new StringBuilder();
        for(byte b:bytes){  //用byte类型去遍历 注意
            stringBuilder.append(huffmancodes.get(b));
        }
        System.out.println("测试stringBuilder=" + stringBuilder.toString());
        int len;
        //一句话len=( stringBuilder.length()+7 )/ 8;
        if(stringBuilder.length() % 8 == 0){
            len= stringBuilder.length()/8;
        }else {
            len= stringBuilder.length()/8+1;
        }
        byte[] huffmanCodeBytes = new byte[len];
        int index= 0;
        for(int i= 0;i<stringBuilder.length();i+=8){
            String strByte;
            if(i+8 > stringBuilder.length()){
                strByte = stringBuilder.substring(i);//从第i个到最后一个
            }else {
                strByte = stringBuilder.substring(i,i+8);
            }
            huffmanCodeBytes[index] = (byte)Integer.parseInt(strByte,2);
            index++;
        }
        return; huffmanCodeBytes;
    }
    //大封装！！！
    private static byte[] huffmanZip(byte[] bytes){
        List<Node> nodes = getNodes(bytes);//把Map放入List中
        Node huffmanTreeRoot = createHuffmanTree(nodes);
        Map<Byte,String> huffmanCodes= getCodes(huffmanTreeRoot);
        byte[] huffmanCodeBytes = zip(bytes,huffmanCodes);
        return huffmanCodes;
    }
    
}
```
