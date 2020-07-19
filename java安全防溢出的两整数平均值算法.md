# java安全防溢出的两整数平均值算法

一般求两整数平均值大家可能会有如下写法

```java
public static int mean(int a, int b){
    return (a + b) / 2;
}
```

好一些的会这样写

```java

public static int mean(int a, int b){
    return (a + b) >> 1;
}
//或
public static int mean(int a, int b){
    return (a + b) >>> 1;
}
```

这样的确能够求出两个数的平均值，但是，当两数为a=0xffff,b=0001时，由于结果溢出，产生错误，平均值计算为0。

下面给大家一种安全的防溢出算法：

1、将相同的位进行相加，结果等于两数按位与的结果的两倍；
2、将不同的位进行相加，其结果等于按位异或的结果。

代码如下：

```java
public static int mean(int a, int b){
    return (x & y) + ((x ^ y) >> 1);
}
```

