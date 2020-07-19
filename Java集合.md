# 集合

- ##### Collection接口

  1. 集合可以理解为一个动态对象数组，不同的集合中的对象内容可以任意扩充
  2. 集合的特点
     1. 性能高
     2. 容易扩展和修改
  3. Collection的常用子类
     1. List
     2. Set
     3. Queue

- ##### List接口

  1. List可以存放任意的数据，而且在List接口中的内容是可以重复的
  2. List接口常用类
     1. `ArrayList`
     2. `Vector`
  3. 常用操作：
     1. 判断集合是否为空：`public boolean isEmpty()`
     2. 查找指定对象是否存在：`public int indexOf(Object o)`

  ```java
  public class ListDemo01 {
      public static void main(String[] args) {
          List<String> lists = null;
          lists = new ArrayList<String>();
          lists.add("A");
          lists.add("b");
          lists.add("b");
          for (int i = 0; i < lists.size(); i++) {
              System.out.print(lists.get(i)+"\t");
          }
  
          lists.remove(0);
          System.out.println();
  
          for (int i = 0; i < lists.size(); i++) {
              System.out.print(lists.get(i)+"\t");
          }
          System.out.println();
          System.out.println(lists.isEmpty());
  
          System.out.println(lists.contains("b"));
  
          System.out.println(lists.indexOf("A"));
  
  
      }
  }
  ```

  

- ##### Set接口

  1. Set接口中不能加入重复元素，但是可以排序
  2. Set接口常用子类：
     - 散列存放：`HashSet`
     - 有序存放：`TreeSet`🍕

- ##### Iterator接口

  1. 集合输出的标准操作：
     - 标准做法使用`Iterator`接口
  2. 操作原理：
     - `Iterator`是专门的迭代输出接口，迭代输出就是将元素一个个进行判断，判断其是否有内容，如果有则把内容取出
     - ![image-20200615165332286](D:\Record\Image\image-20200615165332286.png)

- ##### Map接口

  1. 保存形式：
     - key-value方式保存
  2. 常用子类：
     - `HashMap`无序存放，key不允许重复
     - `HashTable`无序存放，key不允许重复

