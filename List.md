# List

标签（空格分隔）: java

---  
- List 有序集合
用户可以精确控制列表中每个元素的插入位置。可盈通过整数索引访问元素，并搜索列表中的元素。
与SEt不同，列表允许重复的元素
```
List<String> list=new ArrayList<String>();
    list.add("hello ");
    list.add("world");
    list.add("charz");
    list.add("charz");
    list.add("charz");
    list.add("charz");
        System.out.println(list);
        Iterator<String> iterator = list.iterator();
        while (iterator.hasNext()){
            System.out.println(iterator.next());
        }

```
- List集合特有方法
方法|说明|
---|---|
void (int index,E element)| 在此集合中的指定位置插入指定的元素|
E remove(int index)|删除指定索引处的元素|
E set||
E get||
```
    List<String> list=new ArrayList<String>();
    list.add("hello ");
    list.add("world");
    list.add("charz");
    list.add("charz");
    list.add("charz");
    list.add("charz");
    list.add(1,"wsw");
        System.out.println(list);
        Iterator<String> iterator = list.iterator();
//        while (iterator.hasNext()){
//            System.out.println(iterator.next());
//        }
        System.out.println(list.remove(1));
        System.out.println(list);
        try {
            list.set(23, "www");
        }catch (Exception e)
        {
            e.printStackTrace();
        }
        System.out.println("set");
        System.out.println(list.set(1,"xxxxx"));
        System.out.println(list);

```



