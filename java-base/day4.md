![](https://cdn.jsdelivr.net/gh/wmyskxz/img/img/「MoreThanJava」Day4：面向对象基础/7f300125-846f-4440-95f4-3fb397d7478e.png)

- **「MoreThanJava」** 宣扬的是 **「学习，不止 CODE」**，本系列 Java 基础教程是自己在结合各方面的知识之后，对 Java 基础的一个总回顾，旨在 **「帮助新朋友快速高质量的学习」**。
- 当然 **不论新老朋友** 我相信您都可以 **从中获益**。如果觉得 **「不错」** 的朋友，欢迎 **「关注 + 留言 + 分享」**，文末有完整的获取链接，您的支持是我前进的最大的动力！

# Part 1. 面向对象设计概述

![](https://cdn.jsdelivr.net/gh/wmyskxz/img/img/「MoreThanJava」Day4：面向对象基础/5b68f16b-c095-4300-8bb4-4180760f9695.png)

面向对象程序设计 *(Object-Oriented Programming, OOP)* 是当今主流的程序设计范型，它取代了 `20` 世纪 `70` 年代的 "结构化" 或过程式编程技术。由于 Java 是面向对象的，所以必须熟悉 OOP 才能够很好地使用 Java。

## 了解抽象

**抽象的作用是将复杂的机制隐藏在一个对象中，仅保留我们与之交互所必须的信息**。

为了说明这一点，我们可以想象平时使用 **「电梯」** 的场景。

![熟悉的早晨等电梯！](https://cdn.jsdelivr.net/gh/wmyskxz/img/img/「MoreThanJava」Day4：面向对象基础/bd4d9df6-9894-48cb-8db5-c6193bab8df8.png)

如果您在办公楼工作，这可能是您日常工作的一部分。你按下向上或向下按钮，然后等待门滑开。完成操作后，您进入一个 "盒子"，该 "盒子" 的一面墙上有一个按钮面板，然后按下所需的按钮。当电梯到达您要去到的楼层后，您会挤过其他人然后走出去。

**要使用电梯，您只需要了解如何按下正确的按钮就可以达到目的。**

而隐藏在电梯背后的支持它工作的一系列东西 —— 滑轮系统、机械、电线、减震器、安全系统等等... 您可以完全不知道也完全不必操心...

![我完全不知道他们在做什么...](https://cdn.jsdelivr.net/gh/wmyskxz/img/img/「MoreThanJava」Day4：面向对象基础/3d83e081-0ad5-4d2a-a569-48c441a78dbc.png)

电梯这个 "铁盒子" 以及相应的按钮面板，就是对整个「运输系统」成功的抽象 *(事实上电梯背后还包含检修、维护等一系列事情...)*，它隐藏了足够多的细节，也极大地方便了我们的生活。

## 什么是对象

**简单来说，对象是对现实世界的抽象。** *(例如上方对整个运输系统抽象之后，就得到了「电梯」这个对象...)*

什么东西是对象？什么东西不是对象？这是一个困扰哲学家数千年的问题。勒内·笛卡尔 *(17世纪的哲学家)* 观察到，人类是用面向对象的方式看待世界的 *(例如与电梯的交互)*。人类的大脑会从对象的角度认识世界 *(例如鸟类、鱼类)*，我们的思想和记忆也被组织成物体和它们之间的关系 *(例如，鸟吃虫)*。

### 对象像是一种模板

亚里士多德大概是第一个深入研究 **类型** *(type)* 的哲学家，它曾经提出过 **鱼类** 和 **鸟类** 这样的概念。**所有的对象都是唯一的，但同时也是具有相同的特性和行为的对象所归属的类的一部分。**

这就好像我们拿着一个模具，我们可以使用该模具制作出各种各样东西，每个东西都有自己的 "个性"，但它们又都遵循一些相同的基本模式：

![](https://cdn.jsdelivr.net/gh/wmyskxz/img/img/「MoreThanJava」Day4：面向对象基础/e03748fe-fd54-4200-9e79-b81f4b2df0b9.png)


### 对象的特征

我们可以把你的「银行账户」抽象成一个对象，但它不是由物质构成的。*(虽然您和银行可以使用纸张和其他材料来记录您的账户，但您的账户独立于这些材料而存在。)*

![](https://cdn.jsdelivr.net/gh/wmyskxz/img/img/「MoreThanJava」Day4：面向对象基础/4dceb90b-0dfc-4548-9d07-8fce72749155.png)

虽然它不是物质的，但你的账户是有 **属性** 的 *(余额、利率、持有者等..)*，**你可以对它做一些事情** *(存款、取款、查看余额等..,)*，**它自己也可以做一些事情** *(交易收费、积累利息等...)*。

这足够清楚吧。事实上，这些特征它们都有名字：

- 对象具有 **标识 identity**；*(每个对象都是独立的个体)*
- 对象具有 **状态 state**；*(它具有各种可能会改变的属性)*
- 对象具有 **行为 behavior**；*(它可以做事情，也可以让别人对它做事情)*

这就是对一个物体的一般描述。*(上面的列表来自于 `1994` 年 `Grady Booch`/`Addison-Wesley` 出版的《面向对象分析与设计》一书。)* 当你开始编写面向对象的软件时，你会发现这个列表将帮助你决定你的对象应该是什么样。

## 编程语言中的抽象过程

所有编程语言都提供抽象机制。**可以认为，人们所能够解决的问题的复杂性直接取决于抽象的类型和质量**。

所谓的 "类型" 是指 "所抽象的是什么？"。

![](https://cdn.jsdelivr.net/gh/wmyskxz/img/img/「MoreThanJava」Day4：面向对象基础/efecfb0e-7614-4233-95e1-dbefa942f05f.png)

汇编语言是对底层机器语言的轻微抽象，接着出现的许多 "命令式" 语言 *(如 FORTRAN、BASIC、C 等..)* 都是对汇编语言的进一步抽象。

这些语言在汇编语言基础上有了很大幅度的改进，但是它们所作的主要抽象仍要求在解决问题时要基于计算机的结构，而不是基于所要解决的问题的结构来考虑。

> 传统的结构化程序设计通过设计一系列的过程 *(即算法)* 来求解问题。一旦确定了这些过程，就要开始考虑存储数据的适当方式。
>
> 这就是 `Pascal` 语言的设计者 `Niklaus Wirth` 将其著作命名为《算法 + 数据结构 = 程序》*(Algorithms + Data Structures = Programs, Prentice Hall, `1975`)* 的原因。
>
> 需要注意的是，在 `Wirth` 的这个书名中，算法是第一位的，数据结构是第二位的，这就明确的表述了程序员的工作方式。首先要确定如何操作数据，然后再决定如何组织数据的结构，以便于操作数据。
>
> 而 OOP 却调换了这个次序，将数据放在第一位，然后再考虑操作数据的算法。*(在 OOP 中，也有说法是：程序 = 对象 + 交互)*

这使得程序员必须建立起在 **机器模型** *(位于 "解空间" 内，这是你对问题建模的地方，例如计算机)* 和 **实际需要解决问题的模型** *(位于 "问题空间" 内，这是问题存在的地方，例如一项业务)* 之间的 **关联**。

建立这种映射是费力的，而且这不属于编程语言固有的功能，这使得程序难以编写，并且维护代价高昂，同时也产生了作为副产物的整个 "编程方法" 行业。

## 面向对象思想的突破

另一种对机器建模的方式就是针对待解问题建模。

早期的编程语言，例如 `LISP` 和 `APL`，都是选择一些特定的视角来 "解释世界" *(分别敌营 "所有问题最终都是列表" 或者 "所有问题都是算法形式的")*。`PROLOG` 则将所有问题都转换成决策链。此外还产生了基于约束条件编程的语言和专门通过对图形符号操作来实现编程的语言 *(后来被证明限制性过强)*。

这些方式对于它们本身所要解决的 **特定类型的问题** 都是不错的解决方案，但是一旦 **超出** 其特定领域，它们就力不从心了。

**面向对象的方式通过向程序员提供表示问题空间中的元素的工具而更近了一步。**

这种表示方式非常通用，使得程序员不会受限于任何特定类型的问题。我们把问题空间中的一些基本元素进一步抽象成解空间中的 "对象"。**这种思想的实质是：程序可以通过添加新类型的对象使其自身适用于某个特定的问题**。

因此，当你在阅读描述解决方案的代码的同时，也是在阅读问题的表述。相比之前的语言，这是一种更灵活和更强力的语言抽象。所以，OOP 允许根据问题来描述问题，而不是根据运行解决方案的计算机来描述问题。

面向对象软件的最重要的突破之一就是允许我们按照 **自然的面向对象的大脑思维方式相匹配的方式组织软件**。我们希望使用具有属性并能够与其他对象进行交互的对象，而不是直接使用更改主存储器中的 bit 数据的机器指令。当然，在机器层面上什么也没有改变——bit 数据仍是由机器指令操作的，但至少我们不用再考虑机器指令了！

> 对于一些规模较小的问题，将其分解为过程的开发方式比较理想。面向对象更加适合解决规模较大的问题。要想实现一个简单的 Web 浏览器可能需要大约 `2000` 个过程，这些过程可能需要对一组全局数据进行操作。
>
> ![](https://cdn.jsdelivr.net/gh/wmyskxz/img/img/「MoreThanJava」Day4：面向对象基础/26f7288b-2df2-41f1-a410-482a3867c548.png)
>
> 采用面向对象的设计风格，可能只需要大约 `100` 个类，每个类平均包含 `20` 个方法。这明显易于程序员掌握，也容易找到 BUG。*(假设给定对象的数据出错了，在访问这个数据项的 `20` 个方法中查找错误要比在 `2000` 个过程中查找要容易多了)*

## OOP 的起源

正如我们上面描述的那样，面向对象的编程是当今不可回避的。让我们来看看它是如何变成现实的。

时间回到上世纪 `60` 年代，那个时候计算机图形还不存在。当时，美国计算机科学家 `Ivan Edward Sutherland` 实现了能够绘图的应用程序，名叫：**SketchPad**。

它是专门为设计人员开发的，它允许设计人员使用手写笔通过计算机绘制简单的几何形状，例如三角形、正方形、圆形等。该项目也是 **计算机辅助设计 CAD** 的起点。

![SketchPad](https://cdn.jsdelivr.net/gh/wmyskxz/img/img/「MoreThanJava」Day4：面向对象基础/c83e1ee3-dc92-4076-a30f-466d8e689fbb.png)


这成为了面向对象编程的 **奠基典范** 之一。

因为在 Ivan 的程序设计中，使用了我们现在称为 "对象" 的表现形式来描述现实生活中的几何图形，这些图形对于设计人员来说是完全可以理解的！

这其中没有无穷无尽的变量和函数，而是通过具体的几何图形 *(对象形式)* 来描述 *(包括上下文数据，都存储在变量中)* 和操作 *(函数实现)* 进行分组，并以一种关系进行管理这些特定的元素。

这些东西在现在都有确切的名称。*(分别对应 "属性" 和 "方法")*

## OOP 的规范化

Ivan 的项目和其他一些项目在 `1967` 年影响了 **Simula** 编程语言。该语言第一次直接将面向对象的思想引入到了 编程语言中 *(重大更新之后被称为 `Simula-67`)*。 

`1970` 年代，**Xerox** *(负责鼠标和图形界面的发明)* 在个人电脑上工作。他们希望通过操纵 GUI 和鼠标来创建任何人都可以轻松使用的计算机。

![最早的个人计算机之一](https://cdn.jsdelivr.net/gh/wmyskxz/img/img/「MoreThanJava」Day4：面向对象基础/ebee7ece-d2db-48fc-bc92-d40ff6620a6a.png)

为了表示屏幕上的所有元素并支持其显示和操作的逻辑，由艾伦·凯 *(Alan Kay)* 领导的团队创建了 **SmallTalk** 语言，该语言的灵感来自 **Simula**。根据许多资料显示，这标志着我们今天使用的面向对象编程概念的正式确立！ 

## OOP 的普及化

上述这些方法在 `1981` 年开始流行，并成为了伟大的面向对象语言的起点，例如：

- **Objective-C** 是 iOS 本机开发的原始语言。从那以后，Apple 对其进行了改进和增强，它仍然是 iOS 开发人员的常见选择。
- **C ++** 是 C 编程语言的面向对象版本。C 和 C++ 仍被广泛使用，尤其是在非常专业的行业中。 

如我们所见，在编程方面取得了令人难以置信的进步，这是对以下问题的解决方案：**简化软件开发！**

> **面向对象设计的特殊效率从何而来？**
>
> - 部分影响来自于更清晰的表达复杂系统的方式；
> - 也许最重要的原因 *（也是从操作系统体系结构派生而来的）* 是，当您给某人一个结构时，您很少希望他们拥有无限的特权。仅仅进行类型匹配甚至还不能满足需求。保护某些对象而不保护某些对象也不是非常合理有用。
>
> 正确执行封装不仅是对状态抽象的承诺，而且是消除编程中面向状态的隐喻的一种承诺。

# Part 2. 类与对象概述

![](https://cdn.jsdelivr.net/gh/wmyskxz/img/img/「MoreThanJava」Day4：面向对象基础/19a4aac1-863c-4786-adf5-8350b166ed7f.png)

- 图片来源：https://javatutorial.net/java-oop

**简单的说，类是对象的蓝图或模板，而对象是类的实例。**

这个解释虽然有点像用概念在解释概念，但是从这句话我们至少可以看出，**类是抽象的概念，而对象是具体的东西**。

在面向对象编程的世界中，一切皆为对象，对象都有属性和行为，每个对象都是独一无二的，而且对象一定属于某个类 *(型)*。当我们把一大堆拥有共同特征的对象的静态特征 *(属性)* 和动态特征 *(行为)* 都抽取出来后，就可以定义出一个叫做 **“类”** 的东西。

## 定义类

使用类几乎可以模拟任何东西。假设我们要编写一个表示小狗 Dog 的简单类 —— 它表示的不是特定的小狗，而是任何小狗。

对于大多数宠物狗，我们都知道些什么呢？—— 它们都有名字和年龄，还会叫、会吃东西。由于大多数的小狗都具备上述两项信息 *(名字和年龄)* 和两种行为 *(叫和吃东西)*，所以我们的 Dog 类将包含它们，这个类看上去会是这样：

![](https://cdn.jsdelivr.net/gh/wmyskxz/img/img/「MoreThanJava」Day4：面向对象基础/a1b36ab3-0c58-451d-be4a-d280bc338f44.png)

代码实现起来大概会像这样：

```java
public class Dog {

    // 参数
    private String name;
    private Integer age;

    // 构造器
    public Dog(String name, Integer age) {
        this.name = name;
        this.age = age;
    }

    // 字段访问器
    public String getName() {
        return name;
    }

    // 字段访问器
    public Integer getAge() {
        return age;
    }

    // 方法 - 叫
    void bark() {
        System.out.println("汪汪汪！");
    }

    // 方法 - 吃东西
    void eat() {
        System.out.println("一只" + age + "岁大的名叫 " + name + " 的狗正在吃东西！");
    }
}

```

### 剖析 Dog 类

下面各个部分我们将对上面描述的 Dog 类进行剖析。首先从这个类的方法开始吧，上述源码我们看到，这个类包含一个构造器和四个方法：

```java
public Dog(String name, Integer age)
public String getName()
public Integer getAge()
public void bark()
public void eat()
```

这个类的所有方法都被标记为 `public`。关键字 `public` 意味着任何类的任何方法都可以调用这些方法 *(共有四种访问级别，将在之后介绍到)*

接下来，还需要注意 Dog 类实例中有 `2` 个实例字段用来存放将要操作的数据：

```java
private String name;
private Integer age;
```

关键字 `private` 确保只有 Dog 类自身的方法能够访问到这些实例字段，而其他类的方法不能够读写这些字段。*(这也是 Private 私有本身的含义)*

> **注意**：虽然可以用 `public` 标记实例字段，但这是一种很不好的做法。`public` 修饰数据字段后，程序中的任何方法都可以对其进行读取和修改，这就完全破坏了 **封装**。*(这会使程序非常不可控)* 强烈建议将实力字段标记为 `private`

最后，请注意，**这两个实例字段本身也是对象**：`name` 字段是 `String` 类型的对象，`age` 是 `Integer` 类型的对象。这种情况十分常见：类包含的实例字段通常属于某个类类型。

### 从构造器开始

这个与类名相同且权限为 `public` 的方法 `Dog()` 我们把它称为 **构造器**，让我们来看看它：

```java
public Dog(String name, Integer age) {
    this.name = name;
    this.age = age;
}
```

在构造 Dog 类对象的时候，构造器会运行，从而将实例字段初始化为所希望的初始状态。

例如，当时用下面这条代码创建 Dog 类时：

```java
new Dog("大黄", 1)
```

将会把数据设置为：

```text
name = "大黄"
age = 1
```

构造器与其他方法有一个重要的不同。构造器总是结合 `new` 关键字来调用。不能对一个已经存在的对象调用构造器来达到重新设置属性的目的。例如 *(下方代码将产生编译错误)*：

```java
dogInstance.Dog("小黄", 2);  // ERROR
```

有关构造器还有很多可以说的地方，现在只需要记住：

- 构造器与类同名；
- 每个类可以有一个以上的构造器；
- 构造器可以有 `0` 个、`1` 个或多个参数；
- 构造器没有返回值；
- 构造器总是伴随着 `new` 操作符一起调用。

### 封装的优点

最后仔细看一下非常简单的 `getName`/`getAge` 方法。

```java
public String getName() {
    return name;
}
public Integer getAge() {
    return age;
}
```

这些都是典型的访问器方法。由于它们只返回实例字段值，因此又称为 **字段访问器**。

如果将 `name`、`age` 字段标记为 `public`，允许任意方法访问，而不是编写单独的访问其方法，难道不是更容易一些嘛？

上面的例子似乎并不明显 *(而且 `name` 还是一个只读字段)*，所以为了说明这一点，我们来举一个更加有趣的例子。

![](https://cdn.jsdelivr.net/gh/wmyskxz/img/img/「MoreThanJava」Day4：面向对象基础/c0dcc95b-b595-4c3e-803b-f4771eb1b1c0.png)

假设我们有两个类，男人正在辛苦挣钱并时不时地查看余额，而此时来了一个小偷，专门偷男人的钱，**逮着一个偷一个**，而被偷了之后男人抓到了小偷，此时由于小偷的钱是私有的，**男人抓着小偷咬牙切齿却没有丝毫办法可以把钱拿回来！**

![](https://cdn.jsdelivr.net/gh/wmyskxz/img/img/「MoreThanJava」Day4：面向对象基础/5dcf13d6-6dff-4432-8da5-33788c151311.gif)

封装不仅仅帮助我们提高安全性，更可以简化操作和提高 **内聚性**。

假设你写了一个很庞大的系统，一开始你的定义是这样的：

```java
public int age;
```

你的程序里大概有 `100` 条类似于这样的语句：

```java
instance.age = 10;
```

此时突然要求你把数据类型变一下或者对这个字段其他一些什么统一的处理，需要修改 `100` 处的你，是不是傻了？

**封装的另一个好处是模块化**。这方便我们把散落在各处的代码收拢并做统一的处理。

> 设计模式器大原则之一的 **迪米特法则** 就是对于封装的具体要求，即 A 模块使用 B 模块的某个接口行为，对 B 模块中除此行为之外的其他信息知道得尽可能少。
>
> 比如：耳塞的插孔就是提供声音输出的行为接口，只需要关心这个插孔是否有相应的耳塞标记，是否是圆形，有没有声音即可，至于内部 CPU 如何运算音频信息，以及各个电容如何协同工作，根本不需要关注，这使得模块之间的协作只需忠于接口、忠于功能实现即可。

## 创建和使用类

定义了 `class` 只是定义了对象模板，而要根据模板创建出真正的对象实例，必须使用 `new` 关键字，并调用对象的构造函数才行：

```java
Dog dog = new Dog("大黄", 1);
```

上述代码创建了一个 `Dog` 类型的实例，并通过变量 `dog` 指向它。*(下面我们将详细说明是怎么 "指向" 它的...)*

第一个 `Dog` 表明了 `dog` 变量的类型，第二个 `Dog` 则是调用了 `Dog` 类的构造函数。在 **Java 10** 中，如果可以从变量的初始值推导出它们的类型，那么可以用 `var` 关键字来声明局部变量，而无须指定类型。例如：

```java
var dog = new Dog("大黄", 1);
```

这一点很好，因为可以避免重复写类型名 `Dog`。但是参数和字段的类型还是必须显式地声明，该用法仅能用于方法中的局部变量。

要想使用类中公用方法，我们可以直接使用 `.` *(英文句号)* 来连接类中的方法并调用：

```java
dog.eat();  // 调用该实例的 eat() 方法
```

## Java 使用引用来操纵对象

每种编程语言都有自己的操纵内存中元素的方式。有时候，程序员必须注意将要处理的数据是什么类型。你是直接操纵元素，还是用某种基于特殊语法的间接表示 *(例如 C 和 C++ 里的指针)* 来操纵对象？

**在 Java 中一切都被视为对象**，这使得我们可以使用固定的语法。尽管这一切都看作对象，但操纵的标识符 *(例如上面的 `dog` 变量)* 实际上是 **对象的一个 "引用"** *(reference)*。

![](https://cdn.jsdelivr.net/gh/wmyskxz/img/img/「MoreThanJava」Day4：面向对象基础/d319dcdb-166a-4804-b16c-785721d07b06.png)

只要握住这个遥控器，就能保持与电视机的连接。当有人想改变频道或减小音量时，实际操纵的是遥控器 *(引用)*，再由控制器来调控电视机 *(对象)*。

如果想在房间里四处走走，同时仍能调控电视机，那么只需要携带遥控器就可以了，而不是背着电视机...

**此外，即使没有电视机，遥控器也可以独立存在**。

也就是说，你拥有一个引用，并不一定需要有一个对象与它关联。因此，如果你想操纵一个词或者一个句子，则可以创建一个 **String** 对象：

```java
String s;
```

但是这里创建的只是引用，并不是对象。如果此时向 `s` 发送一个消息，就会返回一个运行时错误。这是因为此时 `s` 实际上没有与任何事物相关联 *(即没有电视机)*。

**因此，一种安全的做法是：创建一个引用的同时便进行初始化。**

```java
String s = "abcd";
```

这里运用到了 Java 语言的一个特性：字符串可以直接使用带引号的文本进行初始化 *(其他对象需要使用 `new`)*。

### null 引用

上面我们已经了解到，一个对象变量包含一个对象的引用。当引用没有关联对象时，实际上指向了一个特殊的值 `null`，这表示它没有引用任何对象。*(可以理解为 `String s;` 等同于 `String s = null;`)*

听上去这是一种处理特殊情况的便捷机制，如未知的名字。但使用 `null` 值需要非常小心！如果对 `null` 值应用一个方法，那么就会产生一个 `NullPointException` 异常。

```java
String s = null;
System.out.println(s.length());  // NullPointException
```

这是一个很严重的错误！如果你的程序没有 "捕获" *(理解为手动检测和处理)* 异常，程序就会终止！正常情况下，程序并不会捕获这些异常，而是依赖于程序员从一开始就不要带来异常。*(这显然很难..)*

定义一个类时，最好清楚的知道哪些字段可能为 `null`。在我们的例子中 *(Dog 类)*，我们不希望 `name` 和 `age` 字段为 `null`。

对此我们有两种解决方法。

**"宽容型" 方法** 是把 `null` 参数转换为一个适当的非 `null` 值：

```java
if (n == null) {
    name = "unknow";
} else {
    name = n; 
}
```

在 **Java 9** 中，`Objects` 类 *(JDK 自带的工具类)* 对此提供了一个便利方法：

```java
name = Objects.requireNonNullElse(n, "unknow");  // 效果与上面代码等同
```

**"严格型" 方法** 则是干脆拒绝 `null` 参数：

```java
name = Objects.requireNonNull(n, "The name cannot be null!");
```

如果把上述代码添加进 `Dog` 类的构造函数，并且有人用 `null` 名字构造了一个 `Dog` 类，就会产生一个 `NullPointerException` 异常。乍看上去，这种做法似乎不太好，但有以下几个好处：

1. 异常报告会提供这个问题的描述；*(也就是 `The name cannot be null!`)*
2. 异常报告会准确地支出问题所在的位置，否则异常可能在其他地方出现，而很难追踪到真正导致问题的这个构造器参数；

# Part 3. 面向对象的四大特性

![](https://cdn.jsdelivr.net/gh/wmyskxz/img/img/「MoreThanJava」Day4：面向对象基础/cfeaa75b-ab0f-493d-8173-20e49cbcac1b.png)

- 图片来源：https://flashgene.com/archives/51547.html

面向对象有三大特性：**封装**、**继承**、**多态**。有的地方支持把 **"抽象"** 也归纳进来，合并称为面向对象的四大特性。我觉得也无可厚非。

*(关于继承和多态会在后续章节里面详细说明, 这里只作简单描述用于简单理解..)*

## 抽象

抽象是面相对象思想最基础的能力之一，正确而严谨的业务抽象和建模分析能力是后续的封装、继承、多态的基础，是软件大厦的基石。*(上面有专门的一节描述，这里不再展开)*

## 封装

正如我们上面 **男人与小偷** 的例子，封装不仅能提高我们的安全性、帮助我们把实现细节隐藏起来，还是一种对象功能内聚的表现形式，这有助于让模块之间的耦合度变低，也更具有维护性。*(封装的优点上方有介绍，这里也不再展开)*

封装使面向对象的世界变得单纯，对象之间的关系变得简单，"自扫门前雪" 就行了。特别是当今智能化的时代，对封装的要求越来越高了，例如 **小爱同学** 好了，对外的唯一接口就是语音输入，隐藏了指令内部的细节实现和相关数据，这大大降低了使用成本，也有效地保护了内部数据安全。

![](https://cdn.jsdelivr.net/gh/wmyskxz/img/img/「MoreThanJava」Day4：面向对象基础/5edae3e9-dbd8-4562-8fab-945b36eb68d4.png)

## 继承

继承允许创建 **具有逻辑等级结构的类体系**，形成一个继承树。就拿我们上面创建的 **Dog** 类来说明吧，不是只有狗拥有那些属性和方法，猫也有！*(可能猫叫不能用 `bark` 表示，但本质都是叫)* 自然界中，有许多动物 *(动物是对这些生物的自然抽象)* 都有这样的行为，那么好了，我们往上再抽象一个 `Animal` 对象：

![](https://cdn.jsdelivr.net/gh/wmyskxz/img/img/「MoreThanJava」Day4：面向对象基础/f4970969-e654-4bed-957b-fe5a3881cbc4.png)

只要继承自 `Animal` 类，那么就会拥有 `Animal` 这个父类所描述的属性和方法 *(子类当然可以有自己的实现，这一点我们在后续章节中详细描述)*。这让软件在业务多变的客观条件下，某些基础模块可以被直接复用、间接复用或增强复用。

**继承把枯燥的代码世界变得更有层次感，更具有扩展性，为多态打下了语法基础。**

不过继承也有几个 **缺点**：

1. 继承是一种 **强耦合** 的关系，父类如果做出一定改变，那么子类也必然会改变；
2. 继承 **破坏了封装**，对于子类而言，它的实现对子类来说都是透明的；

## 多态

**多态是以上述的三个面向对象特征为基础**，根据运行时的实际对象类型，同一个方法产生不同的运行结果，使同一个行为具有不同的表现形式。

太学术化了一点，举个例子可能明白点。比如，有一杯水，我不知道它是温的、冰的还是烫的，但是我一摸我就知道了，我摸水杯的这个动作 *(方法)*，对于不同温度的水 *(运行时不同的对象类型)*，就会得到不同的结果，这就是多态。

![](https://cdn.jsdelivr.net/gh/wmyskxz/img/img/「MoreThanJava」Day4：面向对象基础/ae55c7cc-ea6e-45f6-8014-307eb774bb38.png)

自然界中最典型的例子就是碳家族。如果你告诉你的女朋友将在她的生日晚会上送她一块碳，女朋友当然不高兴了，可事实上却是 5 克拉的钻石。钻石就是碳元素在不断进化过程中的一种多态表现。

严格意义来说，多态并不是面向对象的一种特质，而是一种由继承行为衍生而来的进化能力而已。

(完)

# 要点回顾

1. 类和对象 - 什么是类 / 什么是对象 / OOP 起源和发展 / 面向对象其他相关概念
2. 定义类 - 基本结构 / 属性和方法 / 构造器
3. 使用对象 - 创建对象 / 给对象发消息
4. 面向对象的四大支柱 - 抽象 / 封装 / 继承 / 多态的简单介绍
5. 基础练习 - 定义 Dog 类 / 定义时钟类 / 定义图形类 *(下方)*

# 练习

## 练习 1：定义一个类描述数字时钟

参考答案：

```java
public class Clock {

    private Integer hour;
    private Integer minute;
    private Integer second;

    public Clock(Integer hour, Integer minute, Integer second) {
        this.hour = hour;
        this.minute = minute;
        this.second = second;
    }

    /**
     * 时钟走字(走1s)
     */
    public void run() {
        second += 1;
        if (second.equals(60)) {
            second = 0;
            minute += 1;
            if (minute.equals(60)) {
                minute = 0;
                hour += 1;
                if (hour.equals(24)) {
                    hour = 0;
                }
            }
        }
    }

    /**
     * 显示当前时间
     * @return
     */
    public String showCurrentTime() {
        return String.format("当前时间是：%d时:%d分:%d秒", hour, minute, second);
    }

    /**
     * 内部测试
     * @throws InterruptedException - 使用 Thread.sleep() 需要手动检测该异常, 这里节约篇幅直接抛出
     */
    public static void main(String[] args) throws InterruptedException {
        Clock clock = new Clock(23, 59, 58);
        while (true) {
            clock.run();
            System.out.println(clock.showCurrentTime());
            // 让当前线程睡 1s
            Thread.sleep(1000);
        }
    }
}
```

## 练习 2：定义一个类描述平面上的点并提供移动点和计算到另一个点距离的方法

参考答案：

```java
public class Point {

    private Integer x;
    private Integer y;

    public Point() {
        this.x = 0;
        this.y = 0;
    }

    public Point(Integer x, Integer y) {
        this.x = x;
        this.y = y;
    }

    /**
     * 移动到指定位置
     */
    public void moveTo(Integer x, Integer y) {
        this.x = x;
        this.y = y;
    }

    /**
     * 移动指定的距离
     */
    public void moveBy(Integer dx, Integer dy) {
        this.x += dx;
        this.y += dy;
    }

    /**
     * 计算并返回与另一个点的距离
     */
    public Double distanceTo(Point other) {
        int dx = this.x - other.x;
        int dy = this.y - other.y;
        return Math.sqrt(dx ^ 2 + dy ^ 2);
    }

    /**
     * 当前的坐标信息
     */
    public String currentLocation() {
        return String.format("当前点横坐标：%d，纵坐标：%d", x, y);
    }

    /**
     * 内部测试
     */
    public static void main(String[] args) {
        Point point1 = new Point(3, 5);
        Point point2 = new Point();

        System.out.println(point1.currentLocation());
        System.out.println(point2.currentLocation());

        point2.moveTo(-1, 2);
        System.out.println(point2.currentLocation());

        System.out.println(point1.distanceTo(point2));
    }
}
```

# 参考资料

1. 《Java 核心技术 卷 I》
1. 《Java 编程思想》
1. 《码出高效 Java 开发手册》
1. Deepen your knowledge by learning Object Oriented Programming (OOP) with Swift - https://openclassrooms.com/en/courses/4542221-deepen-your-knowledge-by-learning-object-oriented-programming-oop-with-swift
1. Think like a computer: the logic of programming - https://openclassrooms.com/en/courses/5261196-think-like-a-computer-the-logic-of-programming
1. Introduction to Computer Science using Java - http://programmedlessons.org/Java9/index.html#part02
1. Python 100 天从新手到大师 - https://github.com/jackfrued/Python-100-Days

> - 本文已收录至我的 Github 程序员成长系列 **【More Than Java】，学习，不止 Code，欢迎 star：[https://github.com/wmyskxz/MoreThanJava](https://github.com/wmyskxz/MoreThanJava)**
> - **个人公众号** ：wmyskxz，**个人独立域名博客**：wmyskxz.com，坚持原创输出，下方扫码关注，2020，与您共同成长！

![](https://cdn.jsdelivr.net/gh/wmyskxz/img/img/common/qrcode.png)

非常感谢各位人才能 **看到这里**，如果觉得本篇文章写得不错，觉得 **「我没有三颗心脏」有点东西** 的话，**求点赞，求关注，求分享，求留言！**

创作不易，各位的支持和认可，就是我创作的最大动力，我们下篇文章见！