### 一、面向对像
- C#中主程序入口为一个称为Main的Class
- 所有的数据结构也都是对象,

### 二、数组
#### 一维数组的四种声明方式
```
int[] array_name = new int[100]
char[] array_name = new char[3]{'a','b','c'}
char[] array_name = {''a','b','c'}
char[] array_name = new char[]{'a','b','c'}
```
#### 二维数组的声明及引用
```
int[,] arr = new int[2,3]
arr[1,2] = 100;
Console.Write(arr[1,2]);
```
#### 数组的属性
- `array_name.Length`
- 
#### 数组的遍历
- for循环
```
for(int i=0;i<array_name.Length;i++)
        {using array_name[i] do sth;}
```

- foreach
```
foreach(int x in num) {using x to do sth;}
 //x不能被赋值
```
### 输出
- `Console.WriteLine(A+B+C)`
- `Console.WriteLine("{0}{1}{1}",A,B,C)`
- 

### 输入
- `Console.ReadLine()`
- `Console.ReadKey()`
- 