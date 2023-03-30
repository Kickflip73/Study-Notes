# 一、Python 介绍

## Python 是一种解释型、面向对象、动态数据类型的高级程序设计语言

​	Python 是一种解释型语言： 这意味着开发过程中没有了编译这个环节。类似于PHP和Perl语言。

​	Python 是交互式语言： 这意味着，您可以在一个 Python 提示符 >>> 后直接执行代码。

​	Python 是面向对象语言: 这意味着Python支持面向对象的风格或代码封装在对象的编程技术。

## Python 特点
​    1.易于学习：Python有相对较少的关键字，结构简单，和一个明确定义的语法，学习起来更加简单。

​	2.易于阅读：Python代码定义的更清晰。

​	3.易于维护：Python的成功在于它的源代码是相当容易维护的。

​	4.一个广泛的标准库：Python的最大的优势之一是丰富的库，跨平台的，在UNIX，Windows和Macintosh兼容很好。

​	5.互动模式：互动模式的支持，您可以从终端输入执行代码并获得结果的语言，互动的测试和调试代码片断。

​	6.可移植：基于其开放源代码的特性，Python已经被移植（也就是使其工作）到许多平台。

​	7.可扩展：如果你需要一段运行很快的关键代码，或者是想要编写一些不愿开放的算法，你可以使用C或C++完成那部分程序，然后从你的Python程序中调用。

​	8.数据库：Python提供所有主要的商业数据库的接口。

​	9.GUI编程：Python支持GUI可以创建和移植到许多系统调用。

​	10.可嵌入: 你可以将Python嵌入到C/C++程序，让你的程序的用户获得"脚本化"的能力。

## Python 环境变量

![image-20230329083844213](C:\Users\30652\AppData\Roaming\Typora\typora-user-images\image-20230329083844213.png)

## 运行Python

### 1、交互式解释器：

通过命令行窗口输入 python 进入 Python，并在交互式解释器中开始编写 Python 代码。在 Unix、DOS 或任何其他提供了命令行或者 shell 的系统进行 Python 编码工作。

![image-20230329090321524](C:\Users\30652\AppData\Roaming\Typora\typora-user-images\image-20230329090321524.png)

### 2、命令行脚本

应用程序中通过引入解释器可以在命令行中执行Python脚本

![image-20230329090342709](C:\Users\30652\AppData\Roaming\Typora\typora-user-images\image-20230329090342709.png)

### 3、集成开发环境（IDE：Integrated Development Environment）: PyCharm



# 二、Python 基础语法

## Python 标识符

在 Python 里，标识符由字母、数字、下划线组成。

在 Python 中，所有标识符可以包括英文、数字以及下划线(_)，但不能以数字开头。

Python 中的标识符是区分大小写的。

以下划线开头的标识符是有特殊意义的。以单下划线开头 **_foo** 的代表不能直接访问的类属性，需通过类提供的接口进行访问，不能用 **from xxx import \*** 而导入。

以双下划线开头的 **__foo** 代表类的私有成员，以双下划线开头和结尾的 **__foo__** 代表 Python 里特殊方法专用的标识，如 **__init__()** 代表类的构造函数。

Python 可以同一行显示多条语句，方法是用分号 **;** 分开，如：

```
>>> print ('hello');print ('runoob');
```

## Python 保留字符

保留字不能用作常数或变数，或任何其他标识符名称。

所有 Python 的关键字只包含小写字母。

![image-20230329091855916](C:\Users\30652\AppData\Roaming\Typora\typora-user-images\image-20230329091855916.png)

## 行和缩进

Python 的代码块不使用大括号 **{}** 来控制类，函数以及其他逻辑判断。python 最具特色的就是用缩进来写模块。

缩进的空白数量是可变的，但是所有代码块语句必须包含相同的缩进空白数量，这个必须严格执行。

![image-20230329092050804](C:\Users\30652\AppData\Roaming\Typora\typora-user-images\image-20230329092050804.png)



![image-20230329092102961](C:\Users\30652\AppData\Roaming\Typora\typora-user-images\image-20230329092102961.png)

**IndentationError: unindent does not match any outer indentation level**错误表明，你使用的缩进方式不一致，有的是 tab 键缩进，有的是空格缩进，改为一致即可。

如果是 **IndentationError: unexpected indent** 错误, 则 python 编译器是在告诉你"**Hi，老兄，你的文件里格式不对了，可能是 tab 和空格没对齐的问题**"，所以 python 对格式要求非常严格。

因此，在 Python 的代码块中必须使用相同数目的行首缩进空格数。

建议你在每个缩进层次使用 **单个制表符** 或 **两个空格** 或 **四个空格** , 切记不能混用

## 多行语句

Python语句中一般以新行作为语句的结束符。

但是我们可以使用斜杠（ \）将一行的语句分为多行显示，如下所示：

```python
total = item_one + \
        item_two + \
        item_three
```

语句中包含 [], {} 或 () 括号就不需要使用多行连接符。如下实例：

```python
days = ['Monday', 'Tuesday', 'Wednesday',
        'Thursday', 'Friday']
```

## Python 引号

Python 可以使用引号( **'** )、双引号( **"** )、三引号( **'''** 或 **"""** ) 来表示字符串，引号的开始与结束必须是相同类型的。

其中三引号可以由多行组成，编写多行文本的快捷语法，常用于文档字符串，在文件的特定地点，被当做注释。

```python
word = 'word'
sentence = "这是一个句子。"
paragraph = """这是一个段落。
包含了多个语句"""
```

## Python注释

python中单行注释采用 **#** 开头。

注释可以在语句或表达式行末：

```python
# 第一个注释
print ("Hello, Python!")  # 第二个注释
```

python 中多行注释使用三个单引号 **'''** 或三个双引号 **"""**。

```python
'''
这是多行注释，使用单引号。
这是多行注释，使用单引号。
这是多行注释，使用单引号。
'''

"""
这是多行注释，使用双引号。
这是多行注释，使用双引号。
这是多行注释，使用双引号。
"""
```

## Python空行

函数之间或类的方法之间用空行分隔，表示一段新的代码的开始。类和函数入口之间也用一行空行分隔，以突出函数入口的开始。

空行与代码缩进不同，空行并不是Python语法的一部分。书写时不插入空行，Python解释器运行也不会出错。但是空行的作用在于分隔两段不同功能或含义的代码，便于日后代码的维护或重构。

记住：空行也是程序代码的一部分。

## 等待用户输入

下面的程序执行后就会等待用户输入，按回车键后就会退出：

```python
input("按下 enter 键退出，其他任意键显示...\n")
```

以上代码中 ，**\n** 实现换行。一旦用户按下 enter(回车) 键退出，其它键显示。

## 同一行显示多条语句

语句之间使用分号(;)分割，以下是一个简单的实例：

```python
import sys; x = 'runoob'; sys.stdout.write(x + '\n')
```

## print 输出

print 默认输出是换行的，如果要实现不换行需要在变量末尾加上逗号 **,**。

```python
# 换行输出
print x
print y

# 不换行输出
print x,
print y,
```

## 多个语句构成代码组

缩进相同的一组语句构成一个代码块，我们称之代码组。

像if、while、def和class这样的复合语句，首行以关键字开始，以冒号( : )结束，该行之后的一行或多行代码构成代码组。

我们将首行及后面的代码组称为一个子句(clause)。

```python
if expression : 
   suite 
elif expression :  
   suite  
else :  
   suite 
```

## 命令行参数

很多程序可以执行一些操作来查看一些基本信息，Python 可以使用 **-h** 参数查看各参数帮助信息：



# 三、Python 变量类型

变量是存储在内存中的值，这就意味着在创建变量时会在内存中开辟一个空间。

基于变量的数据类型，解释器会分配指定内存，并决定什么数据可以被存储在内存中。

因此，变量可以指定不同的数据类型，这些变量可以存储整数，小数或字符。

## 变量赋值

Python 中的变量赋值不需要类型声明。

每个变量在内存中创建，都包括变量的标识，名称和数据这些信息。

每个变量在使用前都必须赋值，变量赋值以后该变量才会被创建。

等号 **=** 用来给变量赋值。

等号 **=** 运算符左边是一个变量名，等号 **=** 运算符右边是存储在变量中的值。例如：

```python
counter = 100 # 赋值整型变量
miles = 1000.0 # 浮点型
name = "John" # 字符串
```

## 多个变量赋值

Python允许同时为多个变量赋值。例如：

```python
a = b = c = 1
```

以上实例，创建一个整型对象，值为1，三个变量被分配到相同的内存空间上。

也可以为多个对象指定多个变量。例如：

```python
a, b, c = 1, 2, "john"
```

以上实例，两个整型对象 1 和 2 分别分配给变量 a 和 b，字符串对象 "john" 分配给变量 c。

## 标准数据类型

Python有五个标准的数据类型：

- Numbers（数字）
- String（字符串）
- List（列表）
- Tuple（元组）
- Dictionary（字典）

## Python 数字

数字数据类型用于存储数值。

他们是不可改变的数据类型，这意味着改变数字数据类型会分配一个新的对象。

当指定一个值时，Number 对象就会被创建：

```python
var1 = 1
var2 = 10
```

使用del语句删除一些对象的引用，del语句的语法是：

```python
del var1[,var2[,var3[....,varN]]]
```

可以通过使用del语句删除单个或多个对象的引用。例如：

```python
del var
del var_a, var_b
```

Python支持四种不同的数字类型：

- int（有符号整型）
- long（长整型，也可以代表八进制和十六进制）
- float（浮点型）
- complex（复数）

说明：

长整型也可以使用小写 l，但是还是建议使用大写 L，避免与数字 1 混淆。Python使用 L 来显示长整型。

Python 还支持复数，复数由实数部分和虚数部分构成，可以用 a + bj,或者 complex(a,b) 表示， 复数的实部 a 和虚部 b 都是浮点型。

> **注意：**long 类型只存在于 Python2.X 版本中，在 2.2 以后的版本中，int 类型数据溢出后会自动转为long类型。在 Python3.X 版本中 long 类型被移除，使用 int 替代。

## Python字符串

字符串或串(String)是由数字、字母、下划线组成的一串字符，是编程语言中表示文本的数据类型

python的字串列表有2种取值顺序:

- 从左到右索引默认0开始的，最大范围是字符串长度少1
- 从右到左索引默认-1开始的，最大范围是字符串开头

可以使用 **[头下标:尾下标]** 来截取相应的字符串，包含头下标的字符，但不包含尾下标的字符，其中下标是从 0 开始算起，可以是正数或负数，下标可以为空表示取到头或尾

```python
str = "hhh666sb"
print str[1:3]
```

加号（+）是字符串连接运算符，星号（*）是重复操作

```python
str = 'Hello World!'
 
print str           # 输出完整字符串
print str[0]        # 输出字符串中的第一个字符
print str[2:5]      # 输出字符串中第三个至第六个之间的字符串
print str[2:]       # 输出从第三个字符开始的字符串
print str * 2       # 输出字符串两次
print str + "TEST"  # 输出连接的字符串
```

Python 列表截取可以接收第三个参数，参数作用是截取的步长，以下实例在索引 1 到索引 4 的位置并设置为步长为 2（间隔一个位置）来截取字符串：![image-20230330100846104](C:\Users\30652\AppData\Roaming\Typora\typora-user-images\image-20230330100846104.png)

## Python列表

List（列表） 是 Python 中使用最频繁的数据类型。

列表可以完成大多数集合类的数据结构实现。它支持字符，数字，字符串甚至可以包含列表（即嵌套）。

列表用 **[ ]** 标识，是 python 最通用的复合数据类型。

列表中值的切割也可以用到变量 **[头下标:尾下标]** ，就可以截取相应的列表，从左到右索引默认 0 开始，从右到左索引默认 -1 开始，下标可以为空表示取到头或尾。

```python
list1 = ['a',2,5.6]
```

加号 **+** 是列表连接运算符，星号 ***** 是重复操作。如下实例：

```py
list = [ 'runoob', 786 , 2.23, 'john', 70.2 ]
tinylist = [123, 'john']
 
print list               # 输出完整列表
print list[0]            # 输出列表的第一个元素
print list[1:3]          # 输出第二个至第三个元素 
print list[2:]           # 输出从第三个开始至列表末尾的所有元素
print tinylist * 2       # 输出列表两次
print list + tinylist    # 打印组合的列表
```

## Python 元组

tuple（元组）类似于 List（列表）。

元组用 **()** 标识。内部元素用逗号隔开。但是元组不能二次赋值，相当于只读列表。

```python
tuple = ( 'runoob', 786 , 2.23, 'john', 70.2 )
tinytuple = (123, 'john')
 
print tuple               # 输出完整元组
print tuple[0]            # 输出元组的第一个元素
print tuple[1:3]          # 输出第二个至第四个（不包含）的元素 
print tuple[2:]           # 输出从第三个开始至列表末尾的所有元素
print tinytuple * 2       # 输出元组两次
print tuple + tinytuple   # 打印组合的元组
```

以下对元组的操作是无效的，因为元组不允许更新，而列表是允许更新的：

```
tuple[2] = 1000    # 元组中是非法应用
#元组是不允许更新的，所以以上代码执行错误
```

## Python 字典

dictionary(字典)是除列表以外python之中最灵活的内置数据结构类型。列表是有序的对象集合，字典是无序的对象集合。

两者之间的区别在于：字典当中的元素是通过键来存取的，而不是通过偏移存取。

字典用"{ }"标识。字典由索引(key)和它对应的值value组成。

```python
dict = {}
dict['one'] = "This is one"
dict[2] = "This is two"
 
tinydict = {'name': 'runoob','code':6734, 'dept': 'sales'}
 
 
print dict['one']          # 输出键为'one' 的值
print dict[2]              # 输出键为 2 的值
print tinydict             # 输出完整的字典
print tinydict.keys()      # 输出所有键
print tinydict.values()    # 输出所有值
```

## Python数据类型转换

数据类型的转换，只需要将数据类型作为函数名即可，这些函数返回一个新的对象，表示转换的值

![image-20230330101841564](C:\Users\30652\AppData\Roaming\Typora\typora-user-images\image-20230330101841564.png)

# 四、Python运算符

Python语言支持以下类型的运算符:

- 算术运算符
- 比较（关系）运算符
- 赋值运算符
- 逻辑运算符
- 位运算符
- 成员运算符
- 身份运算符
- 运算符优先级

## Python 算术运算符

![image-20230330102402495](C:\Users\30652\AppData\Roaming\Typora\typora-user-images\image-20230330102402495.png)

**注意：***Python2.x 里，整数除整数，只能得出整数。如果要得到小数部分，把其中一个数改成浮点数即可。

## Python比较运算符

![image-20230330102457354](C:\Users\30652\AppData\Roaming\Typora\typora-user-images\image-20230330102457354.png)

## Python赋值运算符

![image-20230330102544570](C:\Users\30652\AppData\Roaming\Typora\typora-user-images\image-20230330102544570.png)

## Python位运算符

按位运算符是把数字看作二进制来进行计算的

![image-20230330102650325](C:\Users\30652\AppData\Roaming\Typora\typora-user-images\image-20230330102650325.png)

## Python逻辑运算符

![image-20230330102742801](C:\Users\30652\AppData\Roaming\Typora\typora-user-images\image-20230330102742801.png)

## Python成员运算符

![image-20230330103134835](C:\Users\30652\AppData\Roaming\Typora\typora-user-images\image-20230330103134835.png)

## Python身份运算符

![image-20230330103222377](C:\Users\30652\AppData\Roaming\Typora\typora-user-images\image-20230330103222377.png)



注意：is 与 == 区别：

​	is 用于判断两个变量引用对象是否为同一个(同一块内存空间)， == 用于判断引用变量的值是否相等。

## Python运算符优先级

![image-20230330103354311](C:\Users\30652\AppData\Roaming\Typora\typora-user-images\image-20230330103354311.png)

# 五、Python 条件语句

Python条件语句是通过一条或多条语句的执行结果（True或者False）来决定执行的代码块。

![image-20230330103509908](C:\Users\30652\AppData\Roaming\Typora\typora-user-images\image-20230330103509908.png)

Python 编程中 if 语句用于控制程序的执行，指定任何非0和非空（null）值为true，0 或者 null为false。

```python
if 判断条件：
    执行语句……
else：
    执行语句……
```

其中"判断条件"成立时（非零），则执行后面的语句，而执行内容可以多行，以缩进来区分表示同一范围。

else 为可选语句，当需要在条件不成立时执行内容则可以执行相关语句。

```python
flag = False
name = 'luren'

if name == 'python':         # 判断变量是否为 python 
    flag = True              # 条件成立时设置标志为真
    print 'welcome boss'     # 并输出欢迎信息
else:
    print name               # 条件不成立时输出变量名称
```

if 语句的判断条件可以用>（大于）、<(小于)、==（等于）、>=（大于等于）、<=（小于等于）来表示其关系。

当判断条件为多个值时，可以使用以下形式：

```python
if 判断条件1:
    执行语句1……
elif 判断条件2:
    执行语句2……
elif 判断条件3:
    执行语句3……
else:
    执行语句4……
```

```python
num = 5     
if num == 3:            # 判断num的值
    print 'boss'        
elif num == 2:
    print 'user'
elif num == 1:
    print 'worker'
elif num < 0:           # 值小于零时输出
    print 'error'
else:
    print 'roadman'     # 条件均不成立时输出
```

由于 python 并不支持 switch 语句，所以多个条件判断，只能用 elif 来实现。

如果判断需要多个条件需同时判断时，可以使用 or （或），表示两个条件有一个成立时判断条件成功；使用 and （与）时，表示只有两个条件同时成立的情况下，判断条件才成功。

```python
num = 8
# 判断值是否在0~5或者10~15之间
if (num >= 0 and num <= 5) or (num >= 10 and num <= 15):    
    print 'hello'
else:
    print 'undefine'
```

当if有多个条件时可使用括号来区分判断的先后顺序，括号中的判断优先执行，此外 and 和 or 的优先级低于>（大于）、<（小于）等判断符号，即大于和小于在没有括号的情况下会比与或要优先判断。

简单的语句组:

也可以在同一行的位置上使用if条件判断语句，如下实例：

```python
if ( var  == 100 ) : print "变量 var 的值为100" 
```

# 六、Python 循环语句

循环语句允许我们执行一个语句或语句组多次

Python 提供了 for 循环和 while 循环（在 Python 中没有 do..while 循环）:

![image-20230330104136303](C:\Users\30652\AppData\Roaming\Typora\typora-user-images\image-20230330104136303.png)

## While循环语句

```python
while 判断条件：
    执行语句
```

执行语句可以是单个语句或语句块。判断条件可以是任何表达式，任何非零、或非空（null）的值均为true。

当判断条件假 false 时，循环结束。

![image-20230330104434153](C:\Users\30652\AppData\Roaming\Typora\typora-user-images\image-20230330104434153.png)

### 无限循环：

如果条件判断语句永远为 true，循环将会无限的执行下去：

```python
var = 1
while var == 1 :  # 该条件永远为true，循环将无限执行下去
   print "You entered: "
```

**注意：**以上的无限循环可以使用 CTRL+C 来中断循环。

### 循环使用 else 语句:

在 python 中，while … else 在循环条件为 false 时执行 else 语句块：

```python
count = -1
while count >= 0:
   print count, "aaa"
else:
   print "bbb"
```

else 中的语句会在循环正常执行完（即因为循环条件为false而跳出循环，而不是通过 break 跳出的）的情况下执行



### 简单语句组

类似 if 语句的语法，如果你的 while 循环体中只有一条语句，你可以将该语句与while写在同一行中:

```python
flag = 1 
while (flag): print 'Given flag is really true!'
```



## for循环语句

Python for循环可以遍历任何序列的项目，如一个列表或者一个字符串。

```python
for iterating_var in sequence:
   statements(s)
```

![image-20230330105104006](C:\Users\30652\AppData\Roaming\Typora\typora-user-images\image-20230330105104006.png)

```python
fruits = ['banana', 'apple',  'mango']
for fruit in fruits:        # 第二个实例
   print ('当前水果: %s'% fruit)
```

### 通过序列索引迭代

另外一种执行循环的遍历方式是通过索引

```python
fruits = ['banana', 'apple',  'mango']
for index in range(len(fruits)):
   print ('当前水果 : %s' % fruits[index])
```

函数 len() 返回列表的长度，即元素的个数。 range()返回一个序列的数

### 循环使用 else 语句

在 python 中，for … else 表示这样的意思，for 中的语句和普通的没有区别，else 中的语句会在循环正常执行完（即 for 不是通过 break 跳出而中断的）的情况下执行，while … else 也是一样。

```python
for num in nums:
	循环语句
else:
	跳出语句
```

## 循环控制语句

![image-20230330104214552](C:\Users\30652\AppData\Roaming\Typora\typora-user-images\image-20230330104214552.png)

### break

break语句用来终止循环语句，即循环条件没有False条件或者序列还没被完全递归完，也会停止执行循环语句。

break语句用在while和for循环中。

如果使用嵌套循环，break语句将停止执行最深层的循环，并开始执行下一行代码。

### continue

continue 语句跳出本次循环，而break跳出整个循环。

continue 语句用来告诉Python跳过当前循环的剩余语句，然后继续进行下一轮循环。

continue语句用在while和for循环中。

### pass

pass 是空语句，是为了保持程序结构的完整性。

pass 不做任何事情，一般用做占位语句。



## Python 循环嵌套

Python 语言允许在一个循环体里面嵌入另一个循环。

**Python for 循环嵌套语法：**

```python
for iterating_var in sequence:
   for iterating_var in sequence:
      statements(s)
   statements(s)
```

**Python while 循环嵌套语法：**

```python
while expression:
   while expression:
      statement(s)
   statement(s)
```

可以在循环体内嵌入其他的循环体，如在while循环中可以嵌入for循环， 反之，你可以在for循环中嵌入while循环。

# 七、Python 数字

Python Number 数据类型用于存储数值。

数据类型是不允许改变的,这就意味着如果改变 Number 数据类型的值，将重新分配内存空间。

以下实例在变量赋值时 Number 对象将被创建：

```python
var1 = 1
var2 = 10
```

也可以使用del语句删除一些 Number 对象引用:

```python
del var1[,var2[,var3[....,varN]]]]
```

可以通过使用del语句删除单个或多个对象:

```python
del var
del var_a, var_b
```

## Python 支持四种不同的数值类型

- **整型(Int)** - 通常被称为是整型或整数，是正或负整数，不带小数点。
- **长整型(long integers)** - 无限大小的整数，整数最后是一个大写或小写的L。
- **浮点型(floating point real values)** - 浮点型由整数部分与小数部分组成，浮点型也可以使用科学计数法表示（2.5e2 = 2.5 x 102 = 250）
- **复数(complex numbers)** - 复数由实数部分和虚数部分构成，可以用a + bj,或者complex(a,b)表示， 复数的实部a和虚部b都是浮点型。

注意：

长整型也可以使用小写"L"，但是还是建议使用大写"L"，避免与数字"1"混淆。Python使用"L"来显示长整型。

Python还支持复数，复数由实数部分和虚数部分构成，可以用a + bj,或者complex(a,b)表示， 复数的实部a和虚部b都是浮点型

## Python Number 类型转换

```python
int(x [,base ])         将x转换为一个整数  
long(x [,base ])        将x转换为一个长整数  
float(x )               将x转换到一个浮点数  
complex(real [,imag ])  创建一个复数  
str(x )                 将对象 x 转换为字符串  
repr(x )                将对象 x 转换为表达式字符串  
eval(str )              用来计算在字符串中的有效Python表达式,并返回一个对象  
tuple(s )               将序列 s 转换为一个元组  
list(s )                将序列 s 转换为一个列表  
chr(x )                 将一个整数转换为一个字符  
unichr(x )              将一个整数转换为Unicode字符  
ord(x )                 将一个字符转换为它的整数值  
hex(x )                 将一个整数转换为一个十六进制字符串  
oct(x )                 将一个整数转换为一个八进制字符串  
```

## Python math 模块、cmath 模块

Python 中数学运算常用的函数基本都在 math 模块、cmath 模块中。

Python math 模块提供了许多对浮点数的数学运算函数。

Python cmath 模块包含了一些用于复数运算的函数。

cmath 模块的函数跟 math 模块函数基本一致，区别是 cmath 模块运算的是复数，math 模块运算的是数学运算。

要使用 math 或 cmath 函数必须先导入：

```python
import math
import cmath
```

### Python数学函数

![image-20230330111916227](C:\Users\30652\AppData\Roaming\Typora\typora-user-images\image-20230330111916227.png)

### Python随机数函数

随机数可以用于数学，游戏，安全等领域中，还经常被嵌入到算法中，用以提高算法效率，并提高程序的安全性。

![image-20230330112120509](C:\Users\30652\AppData\Roaming\Typora\typora-user-images\image-20230330112120509.png)

### Python三角函数

![image-20230330112219246](C:\Users\30652\AppData\Roaming\Typora\typora-user-images\image-20230330112219246.png)

### Python数学常量

![image-20230330112301642](C:\Users\30652\AppData\Roaming\Typora\typora-user-images\image-20230330112301642.png)
