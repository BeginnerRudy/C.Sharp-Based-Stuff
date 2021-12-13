Question

- Fileds vs Property -> [What is the difference between a field and a property?](https://stackoverflow.com/questions/295104/what-is-the-difference-between-a-field-and-a-property)
- Get set
- namespace and access modifier 
- [C# assemblies, whats in an assembly?](https://stackoverflow.com/questions/4447028/c-sharp-assemblies-whats-in-an-assembly)
- 重写调用是如何实现的呢？
- what is delegate
- what is sync and await





我们将一个对象输出到控制台，默认情况下 打印的就是这个对象所在的类的命名空间

类中默认访问修饰符是private

接口中默认访问修饰符是public

## Lambda Expression

You use a *lambda expression* to create an anonymous function. Use the [lambda declaration operator `=>`](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/operators/lambda-operator) to separate the lambda's parameter list from its body. A lambda expression can be of any of the following two forms:

```c#
(input-parameters) => expression

(input-parameters) => { <sequence-of-statements> }
```

If a lambda expression doesn't return a value, it can be converted to one of the `Action` delegate types; otherwise, it can be converted to one of the `Func` delegate types. 

For example, a lambda expression that has two parameters and returns no value can be converted to an [Action](https://docs.microsoft.com/en-us/dotnet/api/system.action-2) delegate. A lambda expression that has one parameter and returns a value can be converted to a [Func](https://docs.microsoft.com/en-us/dotnet/api/system.func-2) delegate. 

![Screen Shot 2021-11-18 at 7.39.00 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-11-18 at 7.39.00 pm.png)

## Delegate

Delegate is a type safe function pointer. [Type safety means that the compiler will validate types while compiling, and throw an error if you try to assign the wrong type to a variable.]

We create a class by class keyword, create struct by struct keyword, we create a delegate with delegate keyword.

```c#
// [access modifier] delegate [return_type] delegateName(arg1, arg2, ..);
public delegate void HelloFunctionDelegate(string msg);

public static void Hello(string str){
    Console.WriteLone(str);
}

// make a delegate points to a function
HelloFunctionDelegate del = new HelloFunctionDelegate(Hello);

del("Hello"); // this would execute the Hello(string str) method


```

我们可以使用delegate从而将函数作为参数传递，这样就可以将业务逻辑抽出来，让软件更加解藕以及灵活。

https://www.youtube.com/watch?v=D2h46fvQX04&ab_channel=kudvenkat

https://www.youtube.com/watch?v=vBOzvNO8lvk&ab_channel=kudvenkat

https://www.youtube.com/watch?v=s0tkKZoMN1Y&ab_channel=kudvenkat

## Data Type

https://www.tutorialsteacher.com/csharp/csharp-data-types

byte, sbyte

char, string

short, ushort, int, uint, long, ulong

float, double, decimal 

bool = True or False;

object

DateTime

## Working with Strings

string phrase = "Hello " + "world";

phrase.Length;

phrase.ToUpeer();

phrase.ToLower();

phrase.Contains("Hello");

string supports indexing: pharse[0] === 'H' ;

phrase.IndexOf("world");

phrase.Substring(5) ==== "world"

phrase.Substring(5, 3) ==== "wor"

phrase.equals("string");

phrase.split();

phrase.replace();



#### string

1. 字符串的不可变性， 指的是重新赋值会创建新的字符串对象
2. string可以像只读char数组来使用，s[i];
3. StringBuilder -> 可变的string，不会新建内存

## Working with Numbers

\+ \- * \ % ++ --

5 / 2 = 2

5 / 2.0 = 2.5

Math.Abs(-5);

Math.Pow(3, 2) = 9;

Math.Sqrt(64) = 8;

Math.Max(6, 7) = 7;

Math.Min(6, 7) = 6;

Math.Round(4.3) = 4

## Getting User Input

string name = Console.ReadLine();

## Arrays

int[] luckNumbers = {4, 8, 15, 16, 23, 42};

string[] friends = new string[3];

Array.Sort();

Array.Reverse();

## 2D Arrays

```c#
int[,] numberGrid = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};
int[,] myArray = new int[2, 3];
// accessing
numberGrid[2, 2] == 9
```

## Methods

和java一样的写法

### Return Statement

和java一样的写法

## If Statement

和java一样的写法

if 

else if

else

## Switch Statement

和java一样的写法

```c#
switch(expression) {
  case x:
    // code block
    break;
  case y:
    // code block
    break;
  default:
    // code block
}
```

## Loop

和java一样的写法

## Comment

line comment -> //

block comment -> 

/*

comment line 1

comment line 2

*/

## Exception Handling

```c#
try {
   // statements causing exception
} catch( ExceptionName e1 ) {
   // error handling code
} catch( ExceptionName e2 ) {
   // error handling code
} catch( ExceptionName eN ) {
   // error handling code
} finally {
   // statements to be executed
}
```

## OOP

### Access Modifier

![Screen Shot 2021-11-16 at 1.17.33 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-11-16 at 1.17.33 pm.png)

assembly -> 一个ddl文件

protected -> 可以在该类的内部以及其子类中访问



interal -> 只能在当前程序集/项目中访问

public , interal 可以用于修饰类，在同一个项目中public等于internal

==子类的访问权限不能高于父类的访问权限== 

==方法不加访问修饰符默认的是 private 类不加访问修饰答默认的是 internal==

### Classes & Objects

和java一样

### Constructors

和java一样

### Object Methods

首字母大写，其他和java一样

### Getters & Setters

==不一样==

property lower case

setter and getter Upper case

```c#
public class Date
{
    private int month = 7;  // Backing store
    public int Month{
        get {return rating};
        set{
            if ((value > 0) && (value < 13)){
                month = value;
            }
        }
    }
}
```
### Static Class Attributes

和java一样

释放资源 -> Garbage Collector 

### Static Methods & Classes

static method -> 和java一样

a static class cannot be instantiated,  because there is no instance variable.

### this keyword

1. 代表当前类的实例
2.  在类当中显示的调用本类的构造函数 :this()

### Destructor (析构函数)

如，声明 String 类的**析构函数**： ~String() 。

*析构*方法则是在垃圾回收、释放资源时使用的。

### Inheritance

```c#
class derived-class : base-class  
{  
   // methods and fields  
   .
   .
}  
```

#### Overriding

```c#
class base_class
{
    public virtual void gfg();
}

class derived_class : base_class
{
    public override void gfg();
}
```

### Inheritance

#### namespace

namespace, 用于解决类的重复名问题，类似于类的文件夹

##### 不同项目之间的引用

1. 添加引用
2. 引用命名空间 -> using namespace; 

#### 值类型与引用类型

 区别

1. 值类型和引用类型在内存上存储的地方不一样
   1. 值类型 - 存储在内存的栈中
   2. 引用类型 - 存储在内存的堆中
2. 在传递值类型和传递引用的时候，传递的方式不一样。
   1. 值类型我们称之为值传递，引用类型我们称之为引用传递。

![Screen Shot 2021-11-18 at 10.20.20 am](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-11-18 at 10.20.20 am.png)



传参

- 对于引用类型传参，传递的是引用，修改会反应到对象上。类似于浅拷贝。

### 序列化和反序列化

目的：用于传输数据

序列化

1. 将这个类标记为序列化 -> 类上加上 [Serializable]

2. ```c#
   using FileStream fsWrite = new FileStream(filepath){
       BinaryFormatter bf = new BinaryFormatter();
       bf.Serialize(fsWrite, obj);
   }
   ```

反序列化

```c#
using FileStream fsRead = new FileStream(filepath, FileMode.OpenOrCreate, FileAccess.Read){
	BinaryFormatter bf = new BinaryFormatter();
    obj = (Obj) bf.Deserialize(fsread);
}
```

#### inheritance

```c#
<acess-specifier> class <base_class> {
   ...
}

class <derived_class> : <base_class> {
   ...
}
```

- 子类 不能 使用父类的私有字段
- 子类 继承 父类的构造器么？ 不继承，只能调用
  - 子类初始化时，会去调父类的无参构造函数
- 子类调用父类构造函数 :base(arg1, arg2)
- object 是所有类的基类
- new修饰符 显式隐藏从基类继承的成员或者方法

##### 里氏转换

1. 子类可以赋值给父类
2. 如果父类中装的是子类对象，那么可以将这个父类强转为子类对象

==重点==Parent[] parents -> 放的都是子类，他的行为方式取决于是否override还是简单隐藏

### Polymorphism

同一操作作用于不同的对象，可以有不同的解释，产生不同的执行结果，这就是多态性。简单的说:就是用基类的引用指向子类的对象。==重点==Parent[] parents -> 放的都是子类，多态指的是调用每个对象的方法所表现的都是子类的行为。

1. 虚方法 -> 抽象出来的父类，并且需要实例化父类，可以实现方法，使用虚方法
2. 抽象类 -> 抽象出来的父类，但是父类中的方法写不出来，使用抽象类
3. 接口 -> 抽象不出来父类，所以用接口

#### virtual method

1. 将父类的方法标记为虚方法, virtual
2. 将子类的方法标记为override

virtual不一定需要override

#### abstract class

父类中的函数不知道如何去实现的时候，可以将父类写成抽象类，将方法写成抽象方法。

abstract

1. 子类继承抽象类必须重写所有方法和属性

#### interface

接口支持多继承

接口只能继承于接口，不可以继承于类

一个类可以同时继承一个类并且实现多个接口，如果一个子类同时继承了父类A，并且实现了接口IA，那么语法上A必须写在IA的前面。

```c#
public interface IDunkable{
	// 抽象方法
    // 自动属性
    // 不允许有访问修饰符，默认为public
}
```

##### 显示实现接口

为了解决方法的重命名问题 -> 加上接口名，如下所示

Interface.method(){

}

### 设计模式

#### 简单工厂

把创造逻辑抽出来，单独管理

### 部分类

partial关键字 

在同一个namespace下，写多个同名的类，只需要添加partial关键字

### 密封类

sealed 关键字。

不能够被其他类继承，但是可以继承于其他类。

### File Manipulation 

#### Path

```c#
Path.GetFileName(filepath); // 快速获得路径下的文件名
Path.GetFileNameWithoutExtension(filepath); // 快速获得路径下的文件名不包含扩展名
Path.GetExtension(filepath); // 获得文件的扩展名
Path.GetDirectoryName(filepath);  // 获得文件夹的名字

	
```



#### File

```c#
using System.IO;

File.Create(filepath); // 创建文件 
File.Delete(filepath); // 删除文件
File.Copy(targetFilePath, copiedFilePath); // 复制一个文件	
File.Move();
File.ReadAllBytes();
File.WriteAllBytes();
```

#### Encoding

- ASC 128
- ASCII 256
- GB2312 简体字
- Big5 简体字
- unicode解析非常慢
- UTF-8 web :针对Unicode的一种可变长度字符编码；它可以用来表示Unicode标准中的任何字符，而且其编码中的第一个字节仍与ASCII相容，使得原来处理ASCII字符的软件无须或只进行少部份修改后，便可继续使用。

#### FileStream

File会一次性把整个文件读到内存，FileStream用多少读多少到内存中去。

FileStream 是用去操作字节的，所以可以操作所有文件。

File是操作字符的，可以操作文本文件。

```c#
using System.IO;

FileStream fsRead = new FileStream(filepath, FileMode.OpenOrCreate, FileAccess.Read);
byte[] buffer = new byte[1024*1024*5];
int r = fsRead.Read(buffer, 0, buffer.Length); // r 代表每次实际读取到的字节数
string s = Encoding.Default.GetString(buffer, 0, r);
fsRead.Close();
fsRead.Dispose();

using(FileStram fsWrite = new FileStream(filepath, FileMode.OpenOrCreate, FileAccess.Write)){
    string s = "strings";
    byte[] buffer = Encoding.GetBytes(s);
    fsWrite.Write(buffer);
}
```



### Collection

#### ArrayList

用于存储Object的集合，相当于List<Object\>

```c#
using System.Collections;

ArrayList list = new ArrayList();

list.Add(1); // 添加元素
list.Count; // 实际元素个数
list.Capacity; // 最多可包含元素个数
list.AddRange(list); // 添加集合
list.Clear(); //清空所有元素
list.Remove(1); //删除单个指定元素
list.RemoveAt(2); // 根据下标删除元素
list.RemoveRange(0, 3); // 根据下标范围删除元素
list.Sort(); // 升序排列
list.Reverse();
list.Insert(1, "xx"); // 在指定位置插入元素
list.InsertRange(1, new int[]{1, 2}); // 在指定位置插入一个集合
list.Contains(1); // 判断是否包含指定元素

```

#### List

```c#
List<int> list = new List<int>();
list.ToArray();
int[] nums = {1, 2, 3};
nums.toList();
```

#### HashTable

用于存储Object

- var  : 就可以使用VAR 类似 OBJECT 但是效率比OBJECT高点。https://www.cnblogs.com/ggll611928/p/5991401.html
- foreach循环会比for更快

```c#
Hashtable ht = new HashTable();
ht.Add(1, "张三");
ht.Add(2, true);
ht.Add(false, "错误的");

// 用key取值
ht[1]; // "张三"
ht[false]; // "错误的"

// for-each 循环
foreach (var key in ht.Keys){
    Console.WriteLine(ht[key]);
}

// 修改
ht[1] = 123;
```

#### Dictionary

```c#
Dictionary<int, string> dic = new Dictionary<int, string>();
foreach (KeyValuePair<int, string> kv in dic){
    Console.WriteLine("{0}--{1}", kv.Key, kv.Value);
}
```

### Boxing & unboxing 

Boxing -> 数值类型变成引用类型

unboxing -> 引用类型变成数值类型

两者之间存在继承关系则可能发生装箱拆箱

## 什么是.Net

.net platform 

.net framework

- .net CLR（公共语言运行时）
- .Net 类库

## 复杂数据结构

### 常量

const int num = 20;

### 枚举

定义一个固定范围值的基本数据类型集合，比如星期，月份等。

==和java不一样==

https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/enum

```c#
enum ErrorCode : ushort
{
    None = 0,
    Unknown = 1,
    ConnectionLost = 100,
    OutlierReading = 200
}
```

### 结构

struct -> **Structs are value types** while classes are reference types. Structs can be instantiated without using a new operator. A struct cannot inherit from another struct or class, and it cannot be the base of a class.

```c#
public struct Coords
{
    public Coords(double x, double y)
    {
        X = x;
        Y = y;
    }

    public double X { get; }
    public double Y { get; }

    public override string ToString() => $"({X}, {Y})";
}
```

## 函数

### 方法参数

#### params

params: By using the `params` keyword, you can specify a [method parameter](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/method-parameters) that takes a variable number of arguments. 

```c#
public class MyClass
{
    public static void UseParams(params int[] list)
    {
        for (int i = 0; i < list.Length; i++)
        {
            Console.Write(list[i] + " ");
        }
        Console.WriteLine();
    }

    public static void UseParams2(params object[] list)
    {
        for (int i = 0; i < list.Length; i++)
        {
            Console.Write(list[i] + " ");
        }
        Console.WriteLine();
    }

    static void Main()
    {
        // You can send a comma-separated list of arguments of the
        // specified type.
        UseParams(1, 2, 3, 4);
        UseParams2(1, 'a', "test");

        // A params parameter accepts zero or more arguments.
        // The following calling statement displays only a blank line.
        UseParams2();

        // An array argument can be passed, as long as the array
        // type matches the parameter type of the method being called.
        int[] myIntArray = { 5, 6, 7, 8, 9 };
        UseParams(myIntArray);

        object[] myObjArray = { 2, 'b', "test", "again" };
        UseParams2(myObjArray);

        // The following call causes a compiler error because the object
        // array cannot be converted into an integer array.
        //UseParams(myObjArray);

        // The following call does not cause an error, but the entire
        // integer array becomes the first element of the params array.
        UseParams2(myIntArray);
    }
}
/*
Output:
    1 2 3 4
    1 a test

    5 6 7 8 9
    2 b test again
    System.Int32[]
*/
```

#### out

out: The `out` keyword causes arguments to be passed by reference. out参数要求在传参之前可以不要w初始化，并且在方法的内部必须为其赋值。

一般用于获得函数内的不同类型的值的结果，就是在调用的函数中赋值。

```c#
int initializeInMethod;
OutArgExample(out initializeInMethod);
Console.WriteLine(initializeInMethod);     // value is now 44

void OutArgExample(out int number){
    number = 44;
}
```



#### ref

ref: The `ref` keyword indicates that a value is passed by reference. ref能够将一个方法带入方法中，然后在方法中修改，而且反应在外部参数。传入的参数必须初始化。

- Method signature return
- parameters
- structs

#### in

in: The `in` keyword causes arguments to be passed by reference but ensures the argument is not modified. 

> `in` arguments cannot be modified by the called method. Whereas `ref` arguments may be modified, `out` arguments must be modified by the called method, and those modifications are observable in the calling context.

```c#
int readonlyArgument = 44;
InArgExample(readonlyArgument);
Console.WriteLine(readonlyArgument);     // value is still 44

void InArgExample(in int number)
{
    // Uncomment the following line to see error CS8331
    //number = 19;
}
```

[Why would one ever use the "in" parameter modifier in C#?](https://stackoverflow.com/questions/52820372/why-would-one-ever-use-the-in-parameter-modifier-in-c)

#### 重载

和java一样

#### 递归

和java一样

### Extention Method

Extension methods enable you to "add" methods to existing types without creating a new derived type, recompiling, or otherwise modifying the original type. Extension methods are static methods, but they're called as if they were instance methods on the extended type. For client code written in C#, F# and Visual Basic, there's no apparent difference between calling an extension method and the methods defined in a type.

可以在那些系统类的基础上增加功能并且像扩展一样直接使用

```c#
namespace ExtensionMethods
{
    public static class MyExtensions
    {
        public static int WordCount(this String str)
        {
            return str.Split(new char[] { ' ', '.', '?' },
                             StringSplitOptions.RemoveEmptyEntries).Length;
        }
    }
}	
```

之后，这个WordCount就可以直接在string里面用了

```c#
string s = "Hello Extension Methods";
int i = s.WordCount();
```



## Asynchronous programming with async and await

https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/async/

如果程序调用某个方法，等待其执行全部处理后才能继续执行，我们称其为**同步**的。相反，在处理完成之前就返回调用方法则是**异步**的。
我们在编程语言的流程中添加了异步控制的部分，这部分的编程可以称之为**异步编程**。

对应不同的需求，有很多种多线程执行方法的。async/await只是其中的一种，这种方法叫做异步调用。举个栗子吧，你的老板让你搬走一千箱货，你叫来一千个民工每人搬1箱，不管他搬没搬到指定地点，这个是Task.Run()。你让人搬到指定地点领根签子回来找你领钱，这个就是async/await。为啥要await？因为你要等着收回签子发钱啊，把应发的钱发完这事才算完呢。如果你只需一声令下：搬走！然后就可以拍拍屁股走人的话，就不要和人说什么要领签子回来换钱的话嘛。

- ==异步是基于多线程的技术==
- 调用异步方法的线程叫调用者线程，运行异步方法中阻塞性操作的线程叫后台线程。



## 网络编程

Socket = ip + port

## 多线程