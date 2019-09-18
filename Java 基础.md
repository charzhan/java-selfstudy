# Java 基础

标签（空格分隔）： API

- 装箱： 把基本数据类型转换为相对应的包装类型
- 拆箱：把包装类类型转换为对应的基本数据类型
``` java
public class demoui1 {
    public static  void  main(String[]  args){
        Integer i=Integer.valueOf(100);
        Integer ii=100;// Integer.valueOf(100);
        //拆箱
        ii=ii.intValue()+12;
    }
}
```
date
public long getTime() 股偶去从1970年1月1日 0点 到现在的毫秒值
``` java
public class demoui1 {
    public static  void  main(String[]  args){
    Date d= new Date();
    String s=dateUtiles.dateToString(d,"yyyy年MM月dd日 HH:mm:ss");
        System.out.println(s);
    String ss="2018-8-9 12:12:33";
        Date d1= null;
        try {
            d1 = dateUtiles.stringToDate(ss,"yyyy-MM-dd HH:mm:ss");
        } catch (ParseException e) {
            e.printStackTrace();
        }
        System.out.println(d1);
    }

}
class dateUtiles{
    private dateUtiles() {}
    public static  String dateToString(Date data , String format){
        SimpleDateFormat sdf= new SimpleDateFormat(format);
        String s=sdf.format(data);
        return  s;
    }
    public static  Date stringToDate(String s,String format) throws ParseException {
        SimpleDateFormat sdf= new SimpleDateFormat(format);
        Date d=sdf.parse(s);
        return  d;
    }

}

```







