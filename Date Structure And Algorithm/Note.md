#稀疏数组
***
```bash
package com.guigu.sparsearray;

public class SparseArray{
    public static void main(String[] args)
    {
    int chessArr1[][]= new int[11][11];
    chessArr[2][4]= 5;
    chessArr[1][5]= 8;
    chessArr[3][1]= 2;
    System.out.println("原始的二维数组为：");
    for(int[] row:chessArr1){
        for(int data:row){
                System.out.printf("%d\t",data);
            }
        System.out.println();
    } 
    
    }

}