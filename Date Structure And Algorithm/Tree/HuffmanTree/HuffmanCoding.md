1.创建Node类<br/>
2.创建getnodes<br/>
3.创建createhuffmantree<br/>
4.getcodes<br/>
5.zip<br/>
6.封装函数<br/>
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
        System.out.println(content.length());
        //测试getNodes()
        List<Node> nodes = getNodes(contentBytes);
        System.out.println("nodes=" + nodes);
        //测试createHuffmanTree()
        
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
        Map<Byte, Integer> counts = new HashMap<>();
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
            Node rightNode= nodes.get(1);
            Node parent= new Node(null,leftNode.weight,rightNode.weight);
            parent.left= leftNode;
            parent.right= rightNode;
            nodes.add(parent);
        }
        return nodes.get(0);
    }
```
