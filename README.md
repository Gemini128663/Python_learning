# Python学习之路

## 1.  Python语法元素分析

### 1.1 程序的格式框架

* Python采用严格的缩进来表名程序的格式框架，代码编写中，缩进可以用TAb键实现，也可以用多个空格（一般来说是四个空格）实现。

### 1.2 注释

* 注释是程序员在代码中加入一行或者多行信息，用来对语句、函数、数据结构或方法等进行说明，提升代码的可读性。注释是辅助性文字，会被编译器忽略，不被计算及执行。

* Python语言有两种注释方法：单行注释和多行注释。单行注释以 **#** 开头，多行注释以 **'''**(3个单引号)开头和结尾。

* 注释主要有3个用途。第一，标明作者和版权信息。第二，解释代码原理或者用途。第三，辅助程序调试。

### 1.3 命名与保留字

* Python语言允许采用大写字母、小写字母、数字、下划线_和汉字等字符及其组合给变量命名，但名字的首字符不能是数字，中间不能出现空格，长度没有限制。注意：标识符对大小写敏感。  

* 保留字：也成为关键字，指被编程语言内部定义并保留使用放入标识符。在书写时不能定义与关键字相同的标识符。以下是Python的33个关键字列表：  

|    False     |    def    |    if     |  raise  |   None    |    del    |   import   |   return   |     True     |    elif    |     in      |
| :----------: | :-------: | :-------: | :-----: | :-------: | :-------: | :--------: | :--------: | :----------: | :--------: | :---------: |
|   **try**    |  **and**  | **else**  | **is**  | **while** |  **as**   | **except** | **lambda** |   **with**   | **assert** | **finally** |
| **nonlocal** | **yield** | **break** | **for** |  **not**  | **class** |  **from**  |   **or**   | **continue** | **global** |  **pass**   |

### 1.4 字符串

* Python语言中，字符串是用两个双引号 ***" "*** 或者单引号 ***' '*** 括起来的零个或多个字符。
  
* 字符串是字符的序列，可以按照单个字符或者字符片段进行索引。字符串包括两种序号体系：正向递增序号和反向递减序号。如果字符串长度为L，正向递增以最左侧字符序号为0，向右依次递增，最右侧字符序号为L-1；反向递减序号以最右侧字符序号为-1，向左依次递减，最左侧字符序号为-L。这两种索引字符的方法可以同时使用。
* Python字符串也提供区间访问方式，采用[N:M]格式，表示字符串中从N到M(不包含M)的子字符串,其中，N和M为字符串的索引符号，可以混合使用正向递增序号和反向递减序号。

### 1.5 赋值语句

* Python语言中，“=”表示“赋值”，即将等号右侧的计算结果赋给左边变量，包含等号(=)的语句称为赋值语句。此外，还有一种同步赋值语句，可以同时给多个变量赋值，基本格式如下：  
  <变量1>,<变量2>...<变量N> = <表达式1>,<表达式2>...<表达式N>  

### 1.6 input函数

* input函数从控制台获得用户输入，无论用户在控制台输入深内容，input()函数都以字符串类型返回结果。

### 1.7 分支语句

* 分支语句是控制程序运行的一类重要语句，它的作用是根据判断条件选择程序执行路径，使用方式如下：  
  
```b
  if <条件1>:  
      <语句块1>
  elif <条件2>:
      <语句块2>
  ......
  else:
      <语句块3>
```

### 1.8  eval()函数

* eval(字符串)函数是Python语言中一个十分重要的函数，它能够以Python表达式的方式解析并执行字符串，并将返回结果输出。简单说，eval(字符串)的作用是将输入的字符串转变成Python语句，并执行该语句。

### 1.9 循环语句

* 循环语句是控制程序运行的一类重要语句，与分支语句控制程序类似，它的作用是根据条件确定一段程序是否再次执行一次或者多次。

### 1.10 函数

* 函数可以理解为对一组表达特定功能表达式的封装，它与数学函数类似，能够接受变量并输出结果。input()、print()、eval()都是python解释器的内置函数。

### 1.11 import相关

* 使用import引用函数有两种方式，但对函数的使用方式略有不同。  
  第一种引用函数库的方法如下：  

  **import 库名**  

  此时，程序可以调用库名中的所有函数，使用库中函数的格式如下:  

  <库名>.<函数名>(函数参数)  

  第二种引用函数库的方法如下:  
  from <库名> import <函数名，函数名...函数名>  
  from <库名> import *  
  其中，*是通配符，表示所有函数,此时，调用该库的函数时不再需要使用库名，直接使用如下格式：  
  <函数名><函数参数>

## 2.[常用的Python内置函数](https://www.runoob.com/python/python-built-in-functions.html)

 |    函数名称    |                                                   函数说明                                                   |
 | :------------: | :----------------------------------------------------------------------------------------------------------: |
 |     abs(x)     |                                     x的绝对值。如果X是复数，返回负数的模                                     |
 |     all(x)     |                   组合类型变量x中所有元素都为真时返回True，否则返回else；若x为空，返回True                   |
 |     any(x)     |                  组合类型变量x中任一元素都为真时返回True，否则返回else；若x为空，返回False                   |
 |     bin(x)     |                      将整数x转换为等值的二进制字符串，如bin(1010)的结果是'0b1111110010'                      |
 |    bool(x)     |                         将x转换为Boolean类型，即True或False。如bool('')的结果是False                         |
 |     chr(i)     |                                返回Unicode为i的字符。如chr(9966)的结果是'✌'。                                |
 |  complex(i,j)  |                      创建一个复数r+i*1j，其中i可以省略。如complex(10,10)的结果是10+10j                       |
 |     dict()     |                                   创建字典类型。如dict()的结果是一个空字典                                   |
 |  divmod(a,b)   |                                              返回a和b的商及余数                                              |
 |    eval(s)     |                          计算字符串s作为Python表达式的值，如eval("1+99")的结果是100                          |
 |     exec()     |                   计算字符串s作为Python语句的值。如exec('a=1+999')运行后，变量a的值为1000                    |
 |    float(x)    |                                 将X转换成浮点数。如float(1010)的结果是1010.0                                 |
 |     hex(x)     |                             将整数转换为16进制字符串。如hex(1010)的结果是'0x3f2'                             |
 |    input(x)    |                               获取用户输入，其中s是字符串，作为提示信息。s可选                               |
 |     int(x)     |                                      将x转换成整数。如int(9.9)的结果是9                                      |
 |     len(x)     |                                 计算变量x的长度。如len(range(10))的结果是10                                  |
 |    list(x)     |                      创建或将变量x转换成一个列表类型。如list({10,9,8})的结果是[8,9,10]                       |
 | max(a1,a2,...) |                                 返回参数的最大值。如max(1,2,3,4,5)的结果是5                                  |
 | min(a1,a2,...) |                                 返回参数的最小值。如min(1,2,3,4,5)的结果是1                                  |
 |     oct(x)     |                            将整数x转换为8进制字符串。如oct(1010)的结果是'0o1762'                             |
 | open(fname,m)  |             打开文件，包括文本方式和二进制方式等。其中，m部分可以省略，默认是以文本可读形式打开              |
 |     ord(c)     |                            返回一个字符的Unicode编码值。如ord("字")的结果是23383                             |
 |  pow(x,y[,z])  |                     返回x的y次幂。如果z存在,则再对进行取模。如pow(2,pow(2,2))的结果是16                      |
 |    print(x)    |                          打印变量或字符串x。print()的end参数用来表示输出的结尾字符                           |
 |  range(a,b,s)  |                   从a到b(不含)以s为步长产生一个序列。如list(range(1,10,3))的结果是[1,4,7]                    |
 |  reversed(r)   |                   返回组合类型r的逆序迭达形式。如for i in reversed([1,2,3])将逆序遍历列表                    |
 |    round(n)    |                  四舍五入方式计算n。如                                round(10.6)的结果是11                  |
 |     set(x)     |        将组合数据类型x                                   转换成集合类型。如set([1,1,1,1])的结果是{1}         |
 |   sorted(x)    | 对组合数据类型x进行排序，默认从小到大                             。如sorted([1,3,5,2,4])的结果是[1,2,3,4,5] |
 |     str(x)     |                            将x转换成等值的字符串类型。如str(0x1010)的结果是'4112'                            |
 |     sum(x)     |      对组合数据类型x计算求和结果。如                                        sum([1,2,3,4,5])的结果是15       |
 |    type(x)     |                           返回变量x的数据类型。如type({1:2})的结果是<class 'dict'>                           |
 |    tuple()     |                     将可迭达对象转换成                                              元组                     |
 |     next()     |                                            返回迭达器的下一个元素                                            |
 |  enumerate()   |                            将可遍历的数据对象组合成一带有数据和数据下标的索引序列                            |
 |    filter()    |                                  通过指定条件过滤序列并返回符合要求的过滤值                                  |
 |     iter()     |                             根据指定的可迭达集合对象或可调用对象来生成一个迭代器                             |
 |  map       ()  |                           通过自定义函数实现对序列的元素映射操作并返回操作后的结果                           |
 |     zip()      |                                将可迭达的对象打包成元组并返回由元组组成的对象                                |
 |    format()    |                                                  格式化数据                                                  |
 |    slice()     |                                   通过指定的切片位置和间隔构造一个切片对象                                   |

## 3.组合数据类型

组合数据类型为多个同类型或者不同类型数据提供单一表示。组合数据类型分为3类：序列类型、集合类型和映射类型。

### 3.1.1 序列类型

序列类型是一维元素向量，元素之间存在先后关系，通过序号访问。Python语言中有很多数据类型都是序列类型，其中比较重要的是str(字符串)、tuple(元组)和list(列表)。序列类型有12个通用的操作符和函数，如表所示：

|       操作符       |                            描述                            |
| :----------------: | :--------------------------------------------------------: |
|       x in s       |           如果x是s是元素，返回Ture,否则返回False           |
|     x not in s     |          如果x不是s是元素，返回Ture,否则返回False          |
|       s + t        |                 连接s和t                                   |
|   s * n 或 n * s   |                       将序列s复制n次                       |
|        s[i]        |                 索引，返回序列的第i个元素                  |
|       s[i:j]       | 分片，返回包含序列s第i到第j个元素的子序列(不包含第j个元素) |
|      s[i:j:k]      |   步骤分片，返回包含序列s第i到第j个元素以k为步数的子序列   |
|       len(s)       |                      序列s的元素个数                       |
|       min(s)       |                     序列s中的最小元素                      |
|       max(s)       |                     序列s中的最大元素                      |
| s.index(x[,i[,j]]) |        序列s中从i开始到j位置中第一次出现元素x的位置        |
|     s.count(x)     |                       序列s中出现x的总次数                       |
