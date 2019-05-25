# java的快速排序法

## 插入排序（直接插入排序、希尔排序）
```java
package test;
import java.util.*;
class InsertSort {
    ArrayList al;
    public InsertSort(int num,int mod){
        al = new ArrayList(num);
        Random rand = new Random();
        System.out.println("The ArrayList Sort Before:");
        for (int i=0;i<num ;i++ ){
            al.add(new Integer(Math.abs(rand.nextInt()) % mod + 1));
            System.out.println("al["+i+"]="+al.get(i));
        }
    }
    public void SortIt(){
        Integer tempInt;
        int MaxSize=1;
        for(int i=1;i<al.size();i++){
            tempInt = (Integer)al.remove(i);
            if(tempInt.intValue()>=((Integer)al.get(MaxSize-1)).intValue()){
                al.add(MaxSize,tempInt);
                MaxSize++;
                System.out.println(al.toString());
            } else {
                for (int j=0;j<MaxSize ;j++ )
            {
            if(((Integer)al.get(j)).intValue()>=tempInt.intValue()){
                al.add(j,tempInt);
                MaxSize++;
                System.out.println(al.toString());
                break;
            }
        }
    }

    System.out.println("The ArrayList Sort After:");
    for(int i=0;i<al.size();i++){
        System.out.println("al["+i+"]="+al.get(i));
    }

    public static void main(String[] args){
        InsertSort is = new InsertSort(10,100);
        is.SortIt();
    }
}
```

## 交换排序（冒泡排序、快速排序）

<!-- TODO -->

## 选择排序（直接选择排序、堆排序）

<!-- TODO -->

## 归并排序

<!-- TODO -->

## 分配排序（箱排序、基数排序）

<!-- TODO -->

## 快速排序的伪代码

<!-- TODO -->

# [返回](../README.md)