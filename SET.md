# 
增强for循环 

标签（空格分隔）： java

---
- 格式
- 增强for循环 原理是Iterator 

```
 for (元素数据类型  变量名: 数组或则Collection集合){
    在此处使用变量即可。
}
```
```
  int [] ss={1,2,34,5,66};
        for (int i:ss ) {
            System.out.println(i); }
```

- ArrayList 底层数据结构是数组，
- LinkList  底层是链表
 方法名| 说明|
---|----|
public void addFirst(E e)| 开头插入数据|
public void addList(E e )| 末尾插入数据|
public E getFirst()|返回例表中第一个元素
public E getLast()|返回例表中最后一个元素
public E removeFirst()|从列表中删除并返回第一个元素
public E removeLast()|从列表中删除并返回最后一个元素|


# SET
- 不含重复元素
- 没有带索引的方法，所以不能使用普通的for循环遍历

# HastSet
  - 底层数据结构是哈希表
  - 不含重复元素
  - 没有带索引的方法，所以不能使用普通的for循环遍历
# 哈希值
 - 是jdk根据对象的地址或者字符串或者数字算出来的int类型的数值
 - Object类中有一个方法可以获取对象的哈希值

# LinkedHashSet集合概述和特点
 - 哈希白哦和链表实现的Set接口，具有可预测的迭代次序
 - 有链表保证元素有序，元素的存储和去除顺序是一致的
 - 由哈希表保证元素唯一，没有重复的元素
 


