# SUPER

标签（空格分隔）： java


---
- super 与this 用法类似
 1. this：代表奔雷对象的应用
 2. super：代表父类存储空间的标识
 | 关键字 | 方位成员变量  | 访问构造方法| 访问成员方法|
| --------  | -----:    | -----:   | :----: |
 |this | this.成员变量 访问本类成员变量|this（） 访问本类构造方法|this.成员方法（）访问本类成员方法|
|super |super.成员变量 访问父类成员变量|super()访问父类构造方法|super.成员方法() 访问父类成员方法|



![此处输入图片的描述][1]

```  java
import java.util.ArrayList;
import java.util.Scanner;

public class demoui1 {
    public static  void  main(String[]  args){
    zi z1=new zi();
    z1.show();
    }
}
class fu{
    int age=10;
}
class zi extends fu{
     int age=1;
     public void zi(){}
public  void  show(){
    System.out.println(this.age);

    System.out.println(super.age);
}
}
```


  [1]: https://github.com/charzhan/php-/blob/master/4.png
  
  
  
  
- 继承中成员方法的访问特点
- 通过子类对象访问一个方法
- 子类成员范围查找
- 父类成员范围查找
- 如果哦都没有就报错（不考虑父类的父类）

# 重写
- 私有方法不能被重写(父类私有成员子类是不能继承的)
- 子类方法访问权限不能更低（public >默认> private）
# 继承
- Java 中类只支持单继承，不支持多继承
- Java 中类支持多层继承

