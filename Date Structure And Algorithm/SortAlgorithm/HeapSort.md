#堆排序
###以树的形式操作数组
####（临时变量和辅助指针）
****
```java

public class HeapSort {
    //调整*******局部*******树为大顶堆的方法
    //i是从最后一个非叶子节点开始的非叶子节点
    public static void adjustHeap(int[] arr, int i, int lengh) {
        int temp = arr[i];//先取出用临时变量保存，
        for(int k=i*2+1;K<lengh;k=k*2+1){ //交换头部有用
     //因为调整局部只for一次的原因就是怕
     //先调整上面再调整下面，如果后调整的下面出现了比先调整的上面更大的值没法赋值到上面
            //！！！****！！！！
            //这个for只用一次，因为不能从上往下走，因为如果下面有更大的只能赋值给局部树的父节点
            // 应该从下往上！！！***i的妙取***！！！
            if(k+1<lengh&&arr[k]<arr[k+1]) {
                k++;
            }
            if(arr[k]>temp){
                arr[i]= arr[k];
                i= k;
            }else {
                break; //体现了只for一次(局部)
            }
            arr[k]= temp;//就可以满足后面调整头部时将和头部交换的最小节点值for到正确的地方
                          //这里是从上而下，因为局部树都是大顶堆（下面肯定比上面小）
        }
        //arr[k]= temp;  //体现了只for一次(局部)
    }
    
    //开始堆排序（前提就是排序对象已经经过多次局部调整为了大顶堆）
    public static void heapSort(int[] arr){
        int temp= 0;//临时变量
        System.out.println("堆排序!");
        /*
                分步完成
                adjustHeap(arr,1,arr.length);
                System.out.println("第一次"+Arrays.toString(arr));
                adjiusHeap(arr,0,arr.length);
                System.out.println("第二次"+Arrays.toString(arr));
         */ //for一步到位
        for(int i= arr.length/2-1;i>0;i--){
            adjustHeap(arr,i,arr.length);
        }
        for(int j=arr.length-1;j>0;j--){
            temp=arr[j];
            arr[j]= arr[0];
            arr[0]= temp;
            adjustHeap(arr,0,j); //每次都从0开始是因为就是头儿有变化
        }
        System.out.println("数组="+Arrays.toString(arr));
    }
}
```
##Demo
****

```java
import java.text.SimpleDateFormat;
import java.util.Date;
import java.util.SimpleTimeZone;

public class HeapSort {
    public static void main(String[] args) {
        int[] arr = new int[8000000];
        for (int i = 0; i < 8000000; i++) {
            arr[i] = (int) (Math.random() * 8000000);
        }
        System.out.println("排序前");
        Date date1 = new Date();
        SimpleDateFormat simpleDateFormat= new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
        String data1Str=simpleDateFormat(date1);
        System.out.println("排序前的时间是= "+data1Str);
        heapSort(arr);
        Date date2 = new Date();
        String data2Str= simpleDateFormat(date1);
        System.out.println("排序后的时间是= "+data2Str);
        //先创建一个Date对象表示当前时间
        //再创建一个SimpleDateFormat对象按想要的格式格式化Date对象
        //再输出即可
    }
}
```