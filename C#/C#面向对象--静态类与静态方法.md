# 静态成员
标识为staticr的字段，方法，属性，构造函数，事件就是静态成员
```
class Dog
{
    static int Num;
}
```
静态成员被所有的实例共享，所有实例都访问同一内存位置

静态成员可以通过类名来访问
```
Dog.Num+=1;
```

# 静态函数
静态函数也独立于任何实例，没有实例也可以调用

静态函数不能访问实例成员，只能访问其他静态成员

实例成员可以访问静态成员
```
class Dog
{
    static int Num;
    static public void PrintNum()
    {
        Console.WriteLine("Num = +"Num);
    }
}
```
# 静态构造函数
用于初始化静态字段
在引用任何静态成员之前，和创建任何实例前调用
与类同名，使用static,无参数，无访问修饰符
```
class Dog
{
    static int Num;
    static Dog()
    //静态构造函数
    {
        Num=0;
    }
    
    static public void PrintNum()
    {
        Console.WriteLine("Num = +"Num);
    }
}
```

# 静态类
只包含静态方法和属性，且标识为static
静态类不能创建实例，不能被继承
可以有静态构造函数

静态类表作用：
- 基础类库的实现，如Math类
- 扩展方法

```
static class PetGuide
{
    public static void HowtoFeedDog(this Dog dog)
    // Dog类，dog实例，this关键字都不可少
    // dog为形参？
    {
        Do sth;
    }
}

Dog dog = new Dog();
dog.HowtoFeedDog();// 扩展后的就像使用原来存在的方法一样
```
