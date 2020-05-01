# 学习java-奥利给！





## 使用命令行运行java程序

- 在xxx.java文件当前目录下打开命令行终端，或者在命令行中进入xxx.java文件目录
- 输入	

```java
javac xxx.java

java xxx
```

- javac程序是一个java编译器。它将xxx.java编译成xxx.class。
- java程序启动java虚拟机。虚拟机执行编译器放在class文件中的字节码。





**注意**

- 如果手工输入源程序，一定要注意大小写。尤其是类名为Welcome,而不是welcome或WELCOME
- 编译器需要一个文件名（Welcome.java）,而运行程序时，只需要指定类名（Welcome），不要带扩展名.java或.class





## java的基本程序设计结构



### 一个简单的java应用程序

```java
public class FirstSample
{
	public static void main(String[] args)
	{
		System.out.println("We will not use 'Hello World!'");
	}
}
```

- 源代码的文件名必须与公共类的名字相同，并用.java作为扩展名。
- java区分大小写。如果出现大小写拼写错误（将main拼写成Main），程序将无法运行。
- 关键字public称为访问修饰符（access modifier)，这些修饰符用于控制程序的其他部分对这段代码的访问级别。
- 根据java语言规范，main方法必须声明为public。java中的main方法必须是静态的。
- 关键字void表示这个方法没有返回值，与C/C++不同的是，main方法没有为操作系统返回“退出代码”。如果main方法正常退出，那么java应用程序的退出代码为0，表示成功地运行了程序。如果希望在终止程序时返回其他的代码，需要调用System.exit方法。
- 关键字class表明java程序中的全部内容都包含在类中。这里，只需要将类作为一个加载程序逻辑的容器，程序逻辑定义了应用程序的行为。
- 类是构建所有java应用程序和applet的构建块。java应用程序中的全部内容都必须放置在类中。
- 关键字class后面紧跟类名。java中定义类名的规则宽松。名字必须以字母开头，后面可以跟字母和数字的任意组合。长度基本没有限制。但不能使用java保留字（public，class等）作为类名。
- 标准的命名规范为：类名是以大写字母开头的名词。如果名字由多个单词组成，每个单词的第一个字母都应该大写（骆驼命名法）。
- java中的所有函数都属于某个类的方法（标准术语称其为方法，而不是成员函数），因此，java中的main方法必须有一个外壳类。
- java中，每个句子必须用分号结束，回车不是语句的结束标志，因此如果需要可以将一条语句写在多行上。
- 这里使用了System.out对象并调用了它的println方法。注意，点号( . )用于调用方法。java使用的通用语法是 *object.method(parameters)* 这等价于函数调用。
- 每次调用println都会在末尾添加换行。
- System.out还有一个print方法，它在输出后不换行。





### 注释

注释不会出现在可执行程序中。

有三种标记注释的方式

```java
// 其注释内容从//开始到本行结尾。

/* */ 当需要长篇的注释时，可以使用/**/将一段比较长的注释概括起来。

以/**开始，以*/结束。用来自动地生成文档。
```