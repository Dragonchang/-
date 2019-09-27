## 1.Handler, Looper,MessageQueue的理解  
https://github.com/Dragonchang/ZflThreadPool   
  （1）.应用卡顿的时候在loop加systrace，检查UI线程中有哪些消息执行时间过长。  
  （2）.加history message机制，检查app发生ANR时候是什么消息比较耗时。  
2.Touch事件机制
3.Android动画的原理
4.Android跨进程通讯的方式
5.Binder的理解
6.View的绘制流程
7.四大组件
  7.1.bindservice startservice
7.2.Activity 四大启动模式
8.ANR是什么？怎样避免和解决ANR? 
9.Android内存泄露研究
10.DB
  10.1 Onupgrade
  10.2 Connectionpool block
11.NetWork okhttp
12.android permission
13.packageManager
14.屏幕适配  
15.android签名和验证  
16.apk热修复  
17.apk防止反编译  
18.窗口管理  
20.进程保活  
21.设计模式  
  21.1 单列模式
  public class Singleton {  
private volatile static Singleton singleton;  //静态变量 加volatile 保证
                                //singleton = new Singleton() 执行指令不会被重排
    private Singleton (){}  //私有构造函数
    public static Singleton getInstance() {  
      if (singleton == null) {  //第一层校验
          synchronized (Singleton.class) {  
          if (singleton == null) {  //第二层校验
              singleton = new Singleton();  
              //指令重排：分配内存、调用构造函数、为变量赋值
              //3步早于2步会导致其它线程获取的变量不是构造好的变量。
          }  
        }  
      }  
    return singleton;  
    }  
} 
21.2 观察者模式

22.消息push  
 轮询、sms、长连接  
  
