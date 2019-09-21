# JVM

标签（空格分隔）： JAVA

---
# 线程 
- 线程同步
- 并行
- 并发
getName()
setName()
yield()  释放当前cpu线程
join()  等待，让其他线程加入
getProiorty


```
import java.util.*;

import static java.lang.Thread.sleep;

public class demoui1   extends Thread{
    public static void main(String[] args) {
        mThread t1 = new mThread();
        mThread t2 = new mThread();
        t1.setName("t1 Thread");
        t2.setName("t2 Thread");
        t1.start();
        t1.setPriority(Thread.MAX_PRIORITY);
        t2.setPriority(Thread.MIN_PRIORITY);
        Thread.currentThread().setName("main Thread");

        for (int num = 0; num < 100; num++) {
            if(num%2!=0) System.out.println(Thread.currentThread().getName()+
                    num+"**************Main()*******");
            try {
                t1.join();
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }t2.start();
    }

}
class method extends  Thread{
    public void method1(){
        System.out.println("I'm thread1");
    }

    @Override
    public void run() {
        super.run();
    }
}
class mThread  extends Thread  {
    @Override
    public void run() {
        for (int num = 0; num < 100; num++) {
            if(num%2==0) System.out.println(Thread.currentThread().getName()+":"+num);
            try {
                sleep(1);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }

        }
    }
}

```
# 创建多线程的方式二、

    ```
    public class demoui1   extends Thread{
    public static void main(String[] args) {
        window w1= new window();
        Thread t1 = new Thread(w1);
        Thread t2 = new Thread(w1);
        Thread t3 = new Thread(w1);
        t1.setName("window1: ");
        t2.setName("window2: ");
        t3.setName("window3: ");
        t1.start();
        t2.start();
        t3.start();   }

}
class window implements Runnable{
    private  int ti=100;
    @Override
    public void run() {
        while (true){
            if(ti>0)
            {  System.out.println(Thread.currentThread().getName()+ti);
                ti--;
            }else break;
        }
    }
}
    ```

- 开发中优先使用Runnalbe接口的方式
实现方式没有类的单继承性的局限性
实现的方式更适合处理多个线程由共享的数据的情况
# 线程状态
- 新建
- 就绪
- 运行
- 阻塞
- 死亡