#斐波那契（黄金分割）查找算法
##(前提有序)
*******
###注意是将一组数按斐波那契数分割
###f(n)-1=[f(n-1)-1]+[f(n-2)-1]+1
*******
####一共有f(n)-1 个数，黄金分割点前有[f(n-1)-1]个数，黄金分割点后有[f(n-2)-1]
####每一次都是和黄金分割点处的数比较
*******
####mid= low + 一共有多少个数 
###但是注意！！是斐波那契形式的共有多少数三种情况：
####总：f(n)-1  左：[f(n-1)-1]  右：[f(n-2)-1]
```java
package com.Zkk666.FibonacciSearch;
import java.util.Arrays;
public class FibonacciSearch{
    public static int[] fib(){
        int[] f= new int[maxSize];
        f[0]= 1;
        f[1]= 1;
        for(int i= 2;i<maxSize;i++){
            f[i]= f[i-1]+f[i-2];
        }
        return f;     //f是一个数组！！！！！！！
    }
    
    
    
    public static int fibSearch(int[] a,int key){
        int low= 0;
        int high= a.length-1;
        int k= 0;  //斐波那契分割数值的下标！！！下标！！！
        int mid= 0;
        int f[]= fib();   //  用一个数组接受函数返回值，因为函数返回值的返回类型就是数组
        while (high>f[k]-1){
            k++;
        }
        int[] temp = Arrays.copyOf(a,f[k]);//复制f[k]个a到temp中，不够f[k]用0填充
        for(int i=high+1;i<temp.length;i++){
            temp[i]= a[high];
        }
        while (low<high){
            mid= low+ f[k-1]-1;
            if(key<temp[mid]){
                high= mid-1;
                k--;     //mid= low + 一共有多少个数 
                         //但是注意！！是斐波那契形式的共有多少数三种情况：
                         //总：f(n)-1  左：[f(n-1)-1]  右：[f(n-2)-1]
            }else if(key>temp[mid]){
                low=mid+1;
                k-=2;    //mid= low + 一共有多少个数 
                         //但是注意！！是斐波那契形式的共有多少数三种情况：
                         //总：f(n)-1  左：[f(n-1)-1]  右：[f(n-2)-1]
            }else {
                if(mid<=high){
                    return mid;
                }else {
                    return high;   //用最大数填充的影响
                }
            }
        }
        return -1;
    }
}

```