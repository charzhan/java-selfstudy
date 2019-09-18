# String
+ 字符串不可变，只在创建后不能被更改
+  虽然String 的值不变，但是可以被共享
+  字符串效果相当于字符数组，底层原理是字节数组(jdk 8 及以前是字符数组，后面是字节数组

1. 通过new创建的字符串对象，每一次new 都申请一个内存空间，虽然内容相同，但是地址不同。
2. 通过“”给出到字符窜，只要字符序列相同，（顺序和大小写），无论在程序代码中代码中出现几次，jvm只会创建一个String对象，并在字符窜池中维护。
+ 字符串的比较
  1. 基本类型： 比较数据值是否相同
  2. 引用类型： 地址值是否相同
+ StringBuilder 
  1. 可以改变，可以反转，重新返回所在对象。append 
+ StringBuilder和String 相互转换
  1. SB to String toString
  2. String to SB StringBuilder
+ ArrayList 
  1. ArrayList.add
  2. ArrayList.size
``` java  
import java.util.ArrayList;
import java.util.Scanner;

public class demoui1 {
    public static  void  main(String[]  args){
        ArrayList<student> studentArrayList = new ArrayList<>();
        student charzhan = new student("charzhan", 12);
        student charzhan1 = new student("charzhan1", 12);
        student charzhan2 = new student("charzhan2", 12);
        studentArrayList.add(charzhan);
        studentArrayList.add(charzhan1);
        studentArrayList.add(charzhan2);
        for (student s:studentArrayList
             ) {
            System.out.println("name: "+s.getName()+" age: "+s.getAge());
        }
    }
}

class  student{
    private String name;
    private  Integer age;
    public student(){}
    public student(String name,Integer age){
        this.age=age;
        this.name=name;

    }
    public String getName() {
        return name;
    }

    public Integer getAge() {
        return age;
    }
    }

``` 