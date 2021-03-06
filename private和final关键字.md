## 1.private

　　private是私有的意思，在Java中可以用来修饰类里面的成员变量或者成员方法（注：不能修饰一个类，因为一个类如果外部无法访问的话，面向对象的编程思想将毫无意义），顾名思义，被private修饰的成员变量或者成员方法将无法被外部访问，编程的时候如果有一些数据不希望被人随意篡改，private是一个极佳的选择，但是随之而来的问题也很显然，被private修饰的成员变量如果只能一成不变，那也是一件很苦恼的事情，这个时候可以选择在类的内部为想要修改的成员变量定义一套getter和setter方法，在方法内部，我们可以自己定义一套逻辑，来实现让这些成员变量既可以被修改，又避免被随意篡改。这样一来，程序的安全性将会有一个质的飞跃。

```java
public class car{

　　　　　　private String brand；

　　　　　　private double price；

 

　　　　　　public String getBrand（）{

　　　　　　　　return brand；}

　　　　　　public void setBrand（String brand）{  //当然通常情况下汽车的牌子是不会改变的。。。

　　　　　　　　this.brand = brand；}

}
```



## 2.final

final在Java中意思类似于“不可修改的”，可以在声明类、变量或者方法的时候使用。如果一个类被声明为final，则这个类将不会有子类，也就是说这个类不能被别的类继承；如果一个方法被声明为final，则这个方法不能被重载，也就是第一次定义的时候设定了哪些参数，用的时候就必须传入对应的参数；如果一个变量被声明为final，则这个变量在使用中不能被改变，且必须在声明的时候赋予初值，后续的使用中只能读取不能修改。
