#稀疏数组
***
```bash
package com.guigu.sparsearray;
               //输出原数组
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
    //将二维数组转化为稀疏数组（什么是稀疏数组）
    
    
    遍历原数组，获得sum（有多少个值）
    int sum= 0;
    for(int i= 0;i<11;i++){
        for(int j=0;j<11;j++){
            if(chess[i][j]!=0){
                sum++;
            }
        }
    }
  
  
    用行数，列数，sum创建稀疏数组
    int sparseArr[][]= new int[sum+1][3];
    sparseArr[0][0]= 11;
    sparseArr[0][1]= 11;
    sparesArr[0][2]= sum;
    
    
    //遍历二维数组，将非 0 的值存放到 sparseArr 中
    int count= 0; //用来记录第几个数据
    for(int i=0;i<11;i++){
        for(int j=0;j<11;j++){
            if(chessArr[i][j]!=0){
                count++;
                sparseArr[count][0]= i;
                sparseArr[count][1]= j;
                sparseArr[count][2]= chessArr[i][j];
                //count展现稀疏数组的特点
            }
        }
    }
  
    
    //输出稀疏数组
    System.out.println();
    System.out.println("得到的稀疏数组为~~~");
    for(int i=0;i<sparseArr.length;i++){
        System.out.printf("%d\t%d\t%d\t\n",sparseArr[i][0],sparseArr[i][1],sparseArr[i][2]);
    }
    System.out.println();
    
    
    //稀疏数组转换为原始数组
    
    int chessArr2[][]= new int[sparseArr[0][0]][sparseArr[0][1]];
    for(int i = 1;i<sparseArr.length;i++){
        chessArr2[sparseArr[i][0]][sparseArr[i][1]]= sparseArr[i][2];
    }
    System.out.println();
    System.out.println("恢复后的二维数组：");
    for(int[] row;chessArr2){
        for(int data;row){
            System.out.printf("%d\t",data);
        }
        System.out.println();
    }
    }
}