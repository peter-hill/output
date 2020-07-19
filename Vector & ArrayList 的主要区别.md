# **Vector & ArrayList 的主要区别**

链接：https://www.nowcoder.com/questionTerminal/0953369f92054cbfbf1024a1e723e04f
来源：牛客网

1. 同步性:Vector是线程安全的，也就是说是同步的  ，而ArrayList  是线程序不安全的，不是同步的 数2。  
2. 数据增长:当需要增长时,Vector默认增长为原来一倍  ，而ArrayList却是原来的50%，这样,ArrayList就有利于节约内存空间。如果涉及到堆栈，队列等操作，应该考虑用Vector，如果需要快速随机访问元素，应该使用ArrayList 。

**扩展知识**： 

  **1. Hashtable & HashMap ** 

Hashtable和HashMap它们的性能方面的比较类似  Vector和ArrayList，比如Hashtable的方法是同步的,而HashMap的不是。 
  **2. ArrayList & LinkedList**

  ArrayList的内部实现是基于内部数组Object[],所以从概念上讲,它更象数组，但LinkedList的内部实现是基于一组连接的记录，所以，它更象一个链表结构，所以，它们在性能上有很大的差别：  
       从上面的分析可知,在ArrayList的前面或中间插入数据时,你必须将其后的所有数据相应的后移,这样必然要花费较多时间，所以,当你的操作是在一列数据的后面添加数据而不是在前面或中间,并且需要随机地访问其中的元素时,使用ArrayList会提供比较好的性能；  而访问链表中的某个元素时,就必须从链表的一端开始沿着连接方向一个一个元素地去查找,直到找到所需的元素为止，所以,当你的操作是在一列数据的前面或中间添加或删除数据，并且按照顺序访问其中的元素时，就应该使用LinkedList了。

<img src="https://uploadfiles.nowcoder.com/images/20180712/3807435_1531362399713_36FE3E05DDE36FB17977429DFD791149" alt="img" style="zoom:200%;" />

![img](https://uploadfiles.nowcoder.com/images/20180316/2718698_1521135731730_FB875A3EE3AA63005BF9494DA115E60D)

链接：https://www.nowcoder.com/questionTerminal/0953369f92054cbfbf1024a1e723e04f
来源：牛客网



Vector在Java早期就出现了，ArrayList是在Java1.2才开始出现的。 

  它们的相同点是，都是数组实现的，所以都维护着插入的顺序，初始默认长度都是10. 

  它们的不同点有： 

  1.Vector是线程安全的，ArrayList是线程不安全的，所有Vector的效率要比ArrayList的效率要低。 

  2.Vector的增加长度时，变为原来的2倍，ArrayList变为原来的1.5倍，如果1.5倍以后长度还是不够，就会设置长度为所需的空间。 

  3.Vector其实并不常用，ArrayList更加使用，为了获得线程安全的集合可以使用Collections里的sychronizedCollection（Collection c）获得

链接：https://www.nowcoder.com/questionTerminal/0953369f92054cbfbf1024a1e723e04f
来源：牛客网



**ArrayList Vector LinkedList三者的区别与联系：** 

  **ArrayList:**（1）底层数据结构是数组，查询快，增删慢；（2）线程不安全，效率高。 

  **Vector:（**1）底层数据结构是数组，查询快，增删慢；（2）线程安全，效率低； 

  **LinkedList:（**1）底层数据结构是链表，查询慢，增删快；（2）线程不安全，效率高； 

  LinkedList比ArrayList更占内存，因为LinkedList为每一个节点存储了两个引用，一个是指向前一个元素，另一个是指向后一个元素。 

  
 

  以上是个人的观点，能力有限，不足之处还忘见谅。