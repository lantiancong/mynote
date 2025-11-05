## 数组

长度确定,类型相同

## 内存分析

![1](..\img\5-1.png)

声明和创建的过程![1](..\img\5-2.png)

```
静态初始化
动态初始化>默认初始化
```

## 数组的使用

for-each循环

## 多维数组

![1](..\img\5-3.png)

![1](..\img\5-4.png)

![1](..\img\5-5.png)

## Arrays类

含有很多对数组的操作方法

Arrays.toString()源码用append拼接

![1](..\img\5-6.png)

![1](..\img\5-7.png)

## 冒泡排序

## *稀疏数组*



![1](..\img\5-8.png)

```java
        int[][] a=new int[11][11];
        a[1][2]=1;
        a[2][3]=2;
        for(int i=0;i<a.length;i++){
            for(int j=0;j<a[i].length;j++){
                System.out.print(a[i][j]+" ");
            }
            System.out.println();
        }
        System.out.println("=================");
        int num=0;
        for(int i=0;i<a.length;i++){
            for(int j=0;j<a[i].length;j++){
                if(a[i][j]!=0){
                    num++;
                }
            }
        }
//        System.out.println("num="+num);
        int[][] b=new int[num+1][3];
        b[0][0]=11;
        b[0][1]=11;
        b[0][2]=num;
        for(int i=0;i<a.length;i++){
            for(int j=0;j<a[i].length;j++){
                if(a[i][j]!=0){
                    b[i][0]=i;
                    b[i][1]=j;
                    b[i][2]=a[i][j];
                }
            }
        }
        for(int i=0;i<b.length;i++){
            for(int j=0;j<b[i].length;j++){
                System.out.print(b[i][j]+" ");
            }
            System.out.println();
        }
        int[][] c=new int[b[0][0]][b[0][1]];
        for(int i=1;i<b.length;i++){
            c[b[i][0]][b[i][1]]=b[i][2];
        }
        System.out.println("=================");
        for(int i=0;i<c.length;i++){
            for(int j=0;j<c[i].length;j++){
                System.out.print(c[i][j]+" ");
            }
            System.out.println();
        }
```

