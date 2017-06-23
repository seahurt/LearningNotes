# 目录
-  继承
-  隐藏方法
-  虚方法与多态
-  构造函数
-  抽象方法与抽象类
-  密闭类
-  接口
-  



## 继承

```
class ChildClass:ParentClass
{
    ...
}

```
>**object 类是所有类的基类**


## 隐藏方法
>在子类中定义同名及相同参数列表的函数来隐藏父类中的相对应方法。

    //要在定义的方法前加上new关键字
    new public void PrintName()
    {
        ...
    }
    //new关键字为推荐的用法，非必需

## 虚方法与多态
>父类中的虚方法可以在子类中用override来进行重写
```
public class Father
{
    virtual public void PrintName()
    // 一个虚方法
    {
        do sth;
    }
}
public class Child:Father
{
    override public void PrintName()
    //在子类中重写的方法
    {
        do sth else;
    }
}
```
> 虚方法：声明为virtual的方法就是虚方法。基类的虚方法可以在派生类中使用override进行重写。

> 多态：通过指向派生类的基类引用，调用虚函数，会根据引用所指向的派生类的实际类型，调用派生类中的同名重写函数，便是多态。

## 构造函数

> 定义：与类同名的函数，通过传入不同的参数来初始化不同的实例。一个类中可以有不止一个构造函数，通过传入不同数量及类型的参数来实现不同实例的初始化

> 构造函数中的变量要在构造函数外部声明
> 属性比方法更早的加载

## 抽象方法与抽象类
> **抽象方法** 用abstract来声明，没有函数体，只能在实例中被override来重写

> **抽象类** 是包含抽象方法的类，用abstract来声明，不能被实例化，只能被继承。

## 密闭类与密闭方法
- **密闭类** 声明为sealed的类

- **密闭方法** 声明为sealed的方法

> **密闭类**无法被继承; **密闭方法**无法被重写

> 基类中的方法可以通过不添加virtual来实现密闭;

> 派生类中方法不希望被子类重写，同是该方法是override重写得到的，可以使用sealed机制

> 如果是派生类中新添加的方法，则不需要用sealed，只要不添加virtual就可以实现密闭，与基类一样。
```
sealed override public void Speak()
{
    ...
}
```
## 接口

接口指定义一组函数成员，而不实现它们的引用类型。
只有定义没有实现。
用interface来声明
> 接口的定义
```
interface ICatchMice //用I开头表明是接口类型
{
    void CatchMice();
    void CatchABigMouse();
    //默认public，不能添加任何访问修饰符;同时没有函数体
}
```

> 接口的实现
```
public class Cat:Pet,ICatchMice,IClimbTree
//接口的实现类似于类的继承
{
    public void CatchMice()
    //实现接口函数
    {
        do sth;
    }
    
}
```

>接口方法的使用可以用类的实例方法来使用;也可以把一个实例强制转换成接口类型,然后使用该接口方法

```
Cat c = new Cat();//新建实例
c.CatchMice();//用类的实例来使用接口函数
ICatchMice CatchM = (ICatchMice)c;//将实例强制转换成接口类型的实例
CatchM.CatchMice();//使用接口方法
```










