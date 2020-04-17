# java-skill
Some information for the interview
<h1>JavaSE and JavaEE</h1>

<b>1.面向对象软件开发的优点有哪些？</b>
代码开发模块化，更易维护和修改。
代码复用。
增强代码的可靠性和灵活性。
增加代码的可理解性。
面向对象编程有很多重要的特性，比如：封装，继承，多态和抽象。

<b>封装</b>给对象提供了隐藏内部特性和行为的能力。<br>
<b>多态</b>是编程语言给不同的底层数据类型做相同的接口展示的一种能力。一个多态类型上的操作可以应用到其他类型的值上面。<br>
<b>继承</b>给对象提供了从基类获取字段和方法的能力。继承提供了代码的重用性，也可以在不修改类的情况下给现存的类添加新特性。<br>
<b>抽象</b>是把想法从具体的实例中分离出来的步骤，因此，要根据他们的功能而不是实现细节来创建类。Java支持创建只暴漏接口而不包含方法实现的抽象的类。这种抽象技术的主要目的是把类的行为和实现细节分离开。<br>
抽象和封装是互补的概念。一方面，抽象关注对象的行为。另一方面，封装关注对象行为的细节。一般是通过隐藏对象内部状态信息做到封装，因此，封装可以看成是用来提供抽象的一种策略。

<b>2.接口和抽象类有什么联系和区别?</b><br>
<b>抽象类：</b>
一个类中有抽象方法，这个类就变成了抽象类。
抽象类中class的前面必须有abstract修饰符。
抽象类中可以有普通方法，也可以有抽象方法，而抽象方法的个数可以是0个，也可以是多个。
子类继承父类，必须重写全部的抽象方法，除非这个类也变成了抽象类。

<b>接口：</b>
表面上看，接口是一种特殊的抽象类，但是类是类，接口是接口，是并列的关系。

抽象类和接口区别如下：
一个类只能继承一个抽象类，而一个类可以实现多个接口。
抽象类可以有构造方法，接口中不能有构造方法。
抽象类中可以有成员变量，接口中没有成员变量。（被final修饰变成了常量）
抽象类中可以有普通方法，接口中所有方法都必须是抽象的。（1.8后允许接口定义非抽象方法）
抽象类中抽象方法的访问类型可以是public，protected，但接口中抽象方法的访问类型只能是public，并且默认为public abstract（省略则自动默认补全）。
抽象类中的成员变量可以是各种类型的，而接口中的成员变量只能是public static final类型的；

<b>3.重载（overload）和重写（override）的联系和区别</b><br>

java中的重载（overload）就是可以在一个类中创建多个方法，它们具有相同的名字，但是具有不同的参数和含义
而重写方法的参数和返回类型必须相同，否则就是重载而不是重写

<b>总结</b><br>
overload（重载）
参数类型、个数、顺序至少有一个不相同。
不能重载只有返回值不同的方法名。
存在于父类和子类、同类中。
override（重写）
方法名、参数、返回值相同。
子类方法不能缩小父类方法的访问权限。
子类方法不能抛出比父类方法更多的异常(但子类方法可以不抛出异常)。
存在于父类和子类之间。
方法被定义为final不能被重写。

<b>4.数组有没有length()方法?String有没有length()方法?</b><br>
数组有length属性，String有length()方法，集合求长度用size()

<b>5.自动装箱和自动拆箱</b><br>
数据类型	关键字	封装类型	占用字节	默认数值	取值范围<br>
布尔型	   boolean	Boolean 	1	false	true,false<br>
字节型  	 byte	    Byte	1	0	-128 ~ 127<br>
短整型	   short	  Short	2	0	-32768 ~32767<br>
整型	    int	     Integer	4	0	-2147483648~2147483647<br>
长整型	   long	    Long	8	0.0l	-9223372036854775808~9223372036854775807<br>
浮点型	   float	  Float	4	0.0f	1.4E-45~3.4028235E38<br>
双精度浮点型	double	Double	8	0	4.9E-324~1.7976931348623157E308<br>
字符型	   char    	Character	2	'\u0000'	'\u0000' ~ '\uffff'<br>
<br>
自动装箱: 就是将基本数据类型自动转换成对应的包装类。<br>
自动拆箱：就是将包装类自动转换成对应的基本数据类型。<br>
自动装箱:将基本类型数据重新转化为对象 Integer num = 9；<br>
自动拆箱:将对象重新转化为基本类型 int num1 = num。<br>

<b>6.int和integer的区别</b><br>
int	             Integer<br>
基本数据类型	    包装类<br>
速度快	           速度慢<br>
栈中	            堆中<br>
初始值 = 0	       初始值 = null<br>
包装类Integer和基本数据类型int比较时,java会自动包装为int
new Integer生成的是两个对象,内存地址不同.

<b>7.String和StringBuffer的区别</b><br>
  这个String类提供了数值不可改变的字符串。而这个StringBuffer类提供的字符串进行修改。
StringBuilder：适用于单线程下在字符缓冲区进行大量操作的情况（是线程不安全的）。
StringBuffer：适用多线程下在字符缓冲区进行大量操作的情况（一般很少）（是线程安全的）。
首先说运行速度，或者说是执行速度，在这方面运行速度快慢为：StringBuilder > StringBuffer > String。

<b>8.什么是值传递和引用传递？</b><br>
值传递是对基本型变量而言的,传递的是该变量的一个副本,改变副本不影响原变量.
引用传递一般是对于对象型变量而言的,传递的是该对象地址的一个副本, 并不是原对象本身 。

<b>9.java集合框架</b><br>
https://blog.csdn.net/qq_26465035/article/details/103164167
http://gzhimages.paidanzi.com/Img/91d0b730-3d88-4330-811f-0d8870e69f82/1574234990453.png
Collection：代表一组对象，每一个对象都是它的子元素。
Set：不包含重复元素的Collection。
List：有顺序的collection，并且可以包含重复元素。
Map：可以把键(key)映射到值(value)的对象，键不能重复。

<b>10.Java异常框架？throw和throws的区别？</b><br>
throw抛出某个具体的异常实例，throws抛出某类型的异常
throws出现在方法函数头；而throw出现在函数体。

<b>11.final和finally的区别？</b><br>
f inal用来修饰类，变量和方法。修饰类时，不可被其他类继承，修饰变量时赋值后的值不可变，修饰方法时将导致子类中不能直接继承该方法，因此，此时可以在子类中定义相同方法名的函数，此时不会与重写final的矛盾，而是在子类中重新地定义了新方法。

finally是异常处理的一部分，注意：finally不是一定会执行的。try没有执行，finally不会执行，有时try执行后finally也不一定执行

<b>12.java内存模型</b><br>
  java内存模型(jmm)分配概念：
堆heap： 优点：运行时数据区，动态分配内存大小，有gc；,缺点：因为要在运行时动态分配，所以存取速度慢，对象存储在堆上，静态类型的变量跟着类的定义一起存储在堆上。
栈stack：存取速度快，仅次于寄存器，缺点：数据大小与生存期必须是确定的，缺乏灵活性，栈中主要存放基本类型变量（比如，int,shot,byte,char,double,foalt,boolean和对象句柄），jmm要求，调用栈和本地变量存放在线程栈上

<b>13.线程和进程</b><br>
进程是运行中的程序，线程是进程的内部的一个执行序列
进程是资源分配的单元，线程是执行单元
进程间切换代价大，线程间切换代价小
进程拥有资源多，线程拥有资源少
多个线程共享进程的资源

创建线程可以用：继承Thread类，实现Runnable接口，线程池，实现Callable接口

线程的几种状态：
1)新建（new）新建一个线程
2) 可运行( runnable ) 获取cpu使用权
3）运行( running ) 执行程序代码
4） 阻塞( block ) 等待阻塞、同步阻塞、其他阻塞
5） 死亡( dead ) 线程生命周期结束

<b>14.同步方法和同步代码块的区别是什么？</b><br>
  区别：
同步方法默认用this或者当前类class对象作为锁；
同步代码块可以选择以什么来加锁，比同步方法要更细颗粒度，我们可以选择只同步会发生同步问题的部分代码而不是整个方法；
同步方法使用关键字 synchronized修饰方法，而同步代码块主要是修饰需要进行同步的代码，用synchronized（object）{代码内容}进行修饰；

<b>15.什么是死锁？</b><br>
  所谓死锁是指多个进程因竞争资源而造成的一种僵局（互相等待），若无外力作用，这些进程都将无法向前推进。死锁产生的4个必要条件：
互斥条件、请求与保持条件、不剥夺条件、循环等待条件

<b>16.多线程访问多资源而不会产生死锁？</b>
  使用多线程的时候，一种非常简单的避免死锁的方式就是：指定获取锁的顺序，并强制线程按照指定的顺序获取锁。因此，如果所有的线程都是以同样的顺序加锁和释放锁，就不会出现死锁了。

<b>17.迭代器</b><br>
  terator接口提供了很多对集合元素进行迭代的方法。每一个集合类都包含了可以返回迭代器实例的迭代方法。迭代器可以在迭代的过程中删除底层集合的元素,但是不可以直接调用集合的remove(Object Obj)删除，可以通过迭代器的remove()方法删除。
  
Iterator可用来遍历Set和List集合，但是ListIterator只能用来遍历List。
Iterator对集合只能是前向遍历，ListIterator既可以前向也可以后向。
ListIterator实现了Iterator接口，并包含其他的功能，比如：增加元素，替换元素，获取前一个和后一个元素的索引，等等。

Enumeration速度是Iterator的2倍，同时占用更少的内存。但是，Iterator远远比Enumeration安全，因为其他线程不能够修改正在被iterator遍历的集合里面的对象。同时，Iterator允许调用者删除底层集合里面的元素，这对Enumeration来说是不可能的。'

<b>18.快速失败(fail-fast)和安全失败(fail-safe)的区别是什么？</b><br>
一：快速失败（fail—fast）

          在用迭代器遍历一个集合对象时，如果遍历过程中对集合对象的结构进行了修改（增加、删除），则会抛出Concurrent Modification Exception。

          原理：迭代器在遍历时直接访问集合中的内容，并且在遍历过程中使用一个 modCount 变量。集合在被遍历期间如果结构发生变化，就会改变modCount的值。每当迭代器使用hashNext()/next()遍历下一个元素之前，都会检测modCount变量是否为expectedmodCount值，是的话就返回遍历；否则抛出异常，终止遍历。

      注意：这里异常的抛出条件是检测到 modCount！=expectedmodCount 这个条件。如果集合发生变化时修改modCount值刚好又设置为了expectedmodCount值，则异常不会抛出。因此，不能依赖于这个异常是否抛出而进行并发操作的编程，这个异常只建议用于检测并发修改的bug。

      场景：java.util包下的集合类都是快速失败的，不能在多线程下发生并发修改（迭代过程中被修改）。

    二：安全失败（fail—safe）

      采用安全失败机制的集合容器，在遍历时不是直接在集合内容上访问的，而是先复制原有集合内容，在拷贝的集合上进行遍历。

      原理：由于迭代时是对原集合的拷贝进行遍历，所以在遍历过程中对原集合所作的修改并不能被迭代器检测到，所以不会触发Concurrent Modification Exception。

      缺点：基于拷贝内容的优点是避免了Concurrent Modification Exception，但同样地，迭代器并不能访问到修改后的内容，即：迭代器遍历的是开始遍历那一刻拿到的集合拷贝，在遍历期间原集合发生的修改迭代器是不知道的。

          场景：java.util.concurrent包下的容器都是安全失败，可以在多线程下并发使用，并发修改。

<b>19.HashMap</b><br>
  Java中的HashMap是以键值对(key-value)的形式存储元素的。HashMap需要一个hash函数，它使用hashCode()和equals()方法来向集合/从集合添加和检索元素。当调用put()方法的时候，HashMap会计算key的hash值，然后把键值对存储在集合中合适的索引上。如果key已经存在了，value会被更新成新值。HashMap的一些重要的特性是它的容量(capacity)，负载因子(load factor)和扩容极限(threshold resizing)。
  Java中的HashMap使用hashCode()和equals()方法来确定键值对的索引，当根据键获取值的时候也会用到这两个方法。而且，这两个方法也用来发现重复元素。所以这两个方法的实现对HashMap的精确性和正确性是至关重要的。
  HashMap和Hashtable都实现了Map接口，因此很多特性非常相似。但是，他们有以下不同点：
  HashMap允许键和值是null，而Hashtable不允许键或者值是null。
  Hashtable是同步的，而HashMap不是。因此，HashMap更适合于单线程环境，而Hashtable适合于多线程环境。
  HashMap提供了可供应用迭代的键的集合，因此，HashMap是快速失败的。另一方面，Hashtable提供了对键的列举(Enumeration)。
  一般认为Hashtable是一个遗留的类。
  
<b>20.数组(Array)和列表(ArrayList)有什么区别？什么时候应该使用Array而不是ArrayList？</b><br>
Array和ArrayList的不同点：
Array可以包含基本类型和对象类型，ArrayList只能包含对象类型。
Array大小是固定的，ArrayList的大小是动态变化的。
ArrayList提供了更多的方法和特性，比如：addAll()，removeAll()，iterator()等等。
对于基本类型数据，集合使用自动装箱来减少编码工作量。但是，当处理固定大小的基本数据类型的时候，这种方式相对比较慢。

ArrayList和LinkedList都实现了List接口，他们有以下的不同点：
ArrayList是基于索引的数据接口，它的底层是数组。它可以以O(1)时间复杂度对元素进行随机访问。与此对应，LinkedList是以元素列表的形式存储它的数据，每一个元素都和它的前一个和后一个元素链接在一起，在这种情况下，查找某个元素的时间复杂度是O(n)。
相对于ArrayList，LinkedList的插入，添加，删除操作速度更快，因为当元素被添加到集合任意位置的时候，不需要像数组那样重新计算大小或者是更新索引。
LinkedList比ArrayList更占内存，因为LinkedList为每一个节点存储了两个引用，一个指向前一个元素，一个指向下一个元素。
也可以参考ArrayList vs. LinkedList。

<b>21.Comparable和Comparator接口是干什么的？列出它们的区别。</b><br>
  Java提供了只包含一个compareTo()方法的Comparable接口。这个方法可以个给两个对象排序。具体来说，它返回负数，0，正数来表明已经存在的对象小于，等于，大于输入对象。
  Java提供了包含compare()和equals()两个方法的Comparator接口。compare()方法用来给两个输入参数排序，返回负数，0，正数表明第一个参数是小于，等于，大于第二个参数。equals()方法需要一个对象作为参数，它用来决定输入参数是否和comparator相等。只有当输入参数也是一个comparator并且输入参数和当前comparator的排序结果是相同的时候，这个方法才返回true。
  
<b>22.什么是Java优先级队列(Priority Queue)？</b><br>
  PriorityQueue是一个基于优先级堆的无界队列，它的元素是按照自然顺序(natural order)排序的。在创建的时候，我们可以给它提供一个负责给元素排序的比较器。PriorityQueue不允许null值，因为他们没有自然顺序，或者说他们没有任何的相关联的比较器。最后，PriorityQueue不是线程安全的，入队和出队的时间复杂度是O(log(n))。

<b>23.大O符号(big-O notation)</b><br>
  大O符号描述了当数据结构里面的元素增加的时候，算法的规模或者是一个渐进上界 。
大O符号也可用来描述其他的行为，比如：内存消耗。因为集合类实际上是数据结构，我们一般使用大O符号基于时间，内存和性能来选择最好的实现。大O符号可以对大量数据的性能给出一个很好的说明。

<b>24.如何权衡是使用无序的数组还是有序的数组？</b><br>
  有序数组最大的好处在于查找的时间复杂度是O(log n)，而无序数组是O(n)。有序数组的缺点是插入操作的时间复杂度是O(n)，因为值大的元素需要往后移动来给新元素腾位置。相反，无序数组的插入时间复杂度是常量O(1)。

<b>25.HashSet和TreeSet有什么区别？</b><br>
  HashSet是由一个hash表来实现的，因此，它的元素是无序的。add()，remove()，contains()方法的时间复杂度是O(1)。
另一方面，TreeSet是由一个树形的结构来实现的，它里面的元素是有序的。因此，add()，remove()，contains()方法的时间复杂度是O(logn)。

<b>26.串行(serial)收集器和吞吐量(throughput)收集器的区别是什么？<br>
  吞吐量收集器使用并行版本的新生代垃圾收集器，它用于中等规模和大规模数据的应用程序。而串行收集器对大多数的小应用(在现代处理器上需要大概100M左右的内存)就足够了。
  
<b>27.Java中的两种异常类型是什么？他们有什么区别？</b><br>
  Throwable包含了错误(Error)和异常(Excetion两类) <br>
Exception又包含了运行时异常(RuntimeException, 又叫非检查异常)和非运行时异常(又叫检查异常) <br>
(1) Error是程序无法处理了, 如果OutOfMemoryError、OutOfMemoryError等等, 这些异常发生时, java虚拟机一般会终止线程 . <br>
(2) 运行时异常都是RuntimeException类及其子类,如 NullPointerException、IndexOutOfBoundsException等, 这些异常是不检查的异常, 是在程序运行的时候可能会发生的, 所以程序可以捕捉, 也可以不捕捉. 这些错误一般是由程序的逻辑错误引起的, 程序应该从逻辑角度去尽量避免.<br> 
(3) 检查异常是运行时异常以外的异常, 也是Exception及其子类, 这些异常从程序的角度来说是必须经过捕捉检查处理的, 否则不能通过编译. 如IOException、SQLException等<br>

<b>28.Java中Exception和Error有什么区别？</b><br>
  Exception和Error都是Throwable的子类。Exception用于用户程序可以捕获的异常情况。Error定义了不期望被用户程序捕获的异常。
  
<b>29.异常处理完成以后，Exception对象会发生什么变化？</b><br>
  Exception对象会在下一个垃圾回收过程中被回收掉。
  
<b>30.什么是JDBC？</b><br>
  JDBC是允许用户在不同数据库之间做选择的一个抽象层。JDBC允许开发者用JAVA写数据库应用程序，而不需要关心底层特定数据库的细节。
Java中垃圾回收有什么目的？什么时候进行垃圾回收？<br>
  JDBC（Java DataBase Connectivity）,是一套面向对象的应用程序接口（API），制定了统一的访问各类关系数据库的标准接口，为各个数据库厂商提供了标准的实现。通过JDBC技术，开发人员可以用纯Java语言和标准的SQL语句编写完整的数据库应用程序，并且真正地实现了软件的跨平台性。 <br>
通常情况下使用JDBC完成以下操作： 
1.同数据库建立连接； 
2.向数据库发送SQL语句； 
3.处理从数据库返回的结果；<br> 
JDBC具有下列优点： 
1.JDBC与ODBC(Open Database Connectivity，即开放数据库互连）十分相似，便于软件开发人员理解； 
2.JDBC使软件开发人员从复杂的驱动程序编写工作中解脱出来，可以完全专注于业务逻辑开发； 
3.JDBC支持多种关系型数据库，大大增加了软件的可移植性； 
4.JDBC API是面向对象的，软件开发人员可以将常用的方法进行二次封装，从而提高代码的重用性；
<br>
  JDBC驱动提供了特定厂商对JDBC API接口类的实现，驱动必须要提供java.sql包下面这些类的实现：Connection, Statement, PreparedStatement,CallableStatement, ResultSet和Driver。

<b>31.Class.forName()方法有什么作用？</b><br>
  初始化参数指定的类，并且返回此类对应的Class 对象
  
<b>32.PreparedStatement比Statement有什么优势？</b><br>
  PreparedStatements是预编译的，因此，性能会更好。同时，不同的查询参数值，PreparedStatement可以重用。
  
<b>33.什么是Servlet？</b><br>
   Servlet是用来处理客户端请求并产生动态网页内容的Java类。Servlet主要是用来处理或者是存储HTML表单提交的数据，产生动态内容，在无状态的HTTP协议下管理状态信息。<br>
   所有的Servlet都必须要实现的核心的接口是javax.servlet.Servlet。每一个Servlet都必须要直接或者是间接实现这个接口，或者是继承javax.servlet.GenericServlet或者javax.servlet.http.HTTPServlet。最后，Servlet使用多线程可以并行的为多个请求服务。<br>
   生命周期：<br>
   对每一个客户端的请求，Servlet引擎载入Servlet，调用它的init()方法，完成Servlet的初始化。然后，Servlet对象通过为每一个请求单独调用service()方法来处理所有随后来自客户端的请求，最后，调用Servlet(译者注：这里应该是Servlet而不是server)的destroy()方法把Servlet删除掉。<br>
   doGet和doPOST：
   doGet：GET方法会把名值对追加在请求的URL后面。因为URL对字符数目有限制，进而限制了用在客户端请求的参数值的数目。并且请求中的参数值是可见的，因此，敏感信息不能用这种方式传递。<br>
   doPOST：POST方法通过把请求参数值放在请求体中来克服GET方法的限制，因此，可以发送的参数的数目是没有限制的。最后，通过POST请求传递的敏感信息对外部客户端是不可见的。<br>
   ServletRequest类可以找出客户端机器的IP地址或者是主机名。getRemoteAddr()方法获取客户端主机的IP地址，getRemoteHost()可以获取主机名。<br>
   
<b>34.HTTP响应的结构是怎么样的？</b><br>
  HTTP响应由三个部分组成：<br>
状态码(Status Code)：描述了响应的状态。可以用来检查是否成功的完成了请求。请求失败的情况下，状态码可用来找出失败的原因。如果Servlet没有返回状态码，默认会返回成功的状态码HttpServletResponse.SC_OK。<br>
HTTP头部(HTTP Header)：它们包含了更多关于响应的信息。比如：头部可以指定认为响应过期的过期日期，或者是指定用来给用户安全的传输实体内容的编码格式。如何在Serlet中检索HTTP的头部看这里。<br>
主体(Body)：它包含了响应的内容。它可以包含HTML代码，图片，等等。主体是由传输在HTTP消息中紧跟在头部后面的数据字节组成的。<br>

<b>35.cookie和session</b><br>
  cookie是Web服务器发送给浏览器的一块信息。浏览器会在本地文件中给每一个Web服务器存储cookie。以后浏览器在给特定的Web服务器发请求的时候，同时会发送所有为该服务器存储的cookie。<br>
	下面列出了session和cookie的区别：
无论客户端浏览器做怎么样的设置，session都应该能正常工作。客户端可以选择禁用cookie，但是，session仍然是能够工作的，因为客户端无法禁用服务端的session。

<b>36.sendRedirect()和forward()方法有什么区别？</b><br>
  sendRedirect()方法会创建一个新的请求，而forward()方法只是把请求转发到一个新的目标上。重定向(redirect)以后，之前请求作用域范围以内的对象就失效了，因为会产生一个新的请求，而转发(forwarding)以后，之前请求作用域范围以内的对象还是能访问的。一般认为sendRedirect()比forward()要慢。
在存储的数据量方面session和cookies也是不一样的。session能够存储任意的Java对象，cookie只能存储String类型的对象。

<b>37.JSP</b><br>
  JSP页面是一种包含了静态数据和JSP元素两种类型的文本的文本文档。静态数据可以用任何基于文本的格式来表示，比如：HTML或者XML。JSP是一种混合了静态内容和动态产生的内容的技术。
	<br>
  浏览器首先要请求一个以.jsp扩展名结尾的页面，发起JSP请求，然后，Web服务器读取这个请求，使用JSP编译器把JSP页面转化成一个Servlet类。需要注意的是，只有当第一次请求页面或者是JSP文件发生改变的时候JSP文件才会被编译，然后服务器调用servlet类，处理浏览器的请求。一旦请求执行结束，servlet会把响应发送给客户端。这里看下如何在JSP中获取请求参数。
	<br>
  下面列出了使用JSP的优点：
JSP页面是被动态编译成Servlet的，因此，开发者可以很容易的更新展现代码。
JSP页面可以被预编译。
JSP页面可以很容易的和静态模板结合，包括：HTML或者XML，也可以很容易的和产生动态内容的代码结合起来。
开发者可以提供让页面设计者以类XML格式来访问的自定义的JSP标签库。
开发者可以在组件层做逻辑上的改变，而不需要编辑单独使用了应用层逻辑的页面。
<br>
  JSP隐含对象是页面中的一些Java对象，JSP容器让这些Java对象可以为开发者所使用。开发者不用明确的声明就可以直接使用他们.JSP页面中的隐含对象：
application
page
request
response
session
exception
out
config
pageContext
RMI（理解）
  Java RMI（Remote Method Invocation）--Java的远程方法调用是Java所特有的分布式计算技术，它允许运行在一个Java虚拟机上的对象调用运行在另一个Java虚拟机上的对象的方法，从而使Java编程人员可以方便地在网络环境中作分布式计算。面向对象设计要求每个任务由最适合该任务的对象执行，RMI将这个概念更深入了一步，使任务可以在最适合该任务的机器上完成。 RMI定义了一组远程接口，可以用于生成远程对象。客户机可以象调用本地对象的方法一样用相同的语法调用远程对象。RMI API提供的类和方法可以处理所有访问远程方法的基础通信和参数引用要求的串行化。 使用RMI开发步骤： 1、定义一个远程接口（远程接口必须继承接口，每个方法必须抛出远程异常，方法参数和方法返回值都必须是可序列化的） 2、实现远程接口 3、定义使用远程对象的客户程序 4、产生远程访问对象的桩和框 5、注册远程对象 6、运行服务器和客户程序
  RMI体系结构是基于一个非常重要的行为定义和行为实现相分离的原则。RMI允许定义行为的代码和实现行为的代码相分离，并且运行在不同的JVM上。
  DGC叫做分布式垃圾回收。RMI使用DGC来做自动垃圾回收。因为RMI包含了跨虚拟机的远程对象的引用，垃圾回收是很困难的。DGC使用引用计数算法来给远程对象提供自动内存管理。


垃圾回收是在内存中存在没有引用的对象或超过作用域的对象时进行。
垃圾回收的目的是识别并且丢弃应用不再使用的对象来释放和重用资源。
System.gc()和Runtime.gc()用来提示JVM要进行垃圾回收。但是，立即开始还是延迟进行垃圾回收是取决于JVM的。
垃圾回收方法
一、引用计数算法（Reference Counting）
二、根搜索算法（GC Root Tracing）
三、标记-清除算法（Mark-Sweep）
四、复制算法（Copying）
五、标记-整理算法（Mark-Compact）
六、分代收集算法（Generational Collection）

在Java中，对象什么时候可以被垃圾回收？
当对象对当前使用这个对象的应用程序变得不可触及的时候，这个对象就可以被回收了。

如果对象的引用被置为null，垃圾收集器是否会立即释放对象占用的内存？<b>不会</b>，在下一个垃圾回收周期中，这个对象将是可被回收的。

JVM的永久代中会发生垃圾回收么？
会，如果永久代满了或者是超过了临界值，会触发完全垃圾回收(Full GC)。如果你仔细查看垃圾收集器的输出信息，就会发现永久代也是被回收的。这就是为什么正确的永久代大小对避免Full GC是非常重要的原因。请参考下Java8：从永久代到元数据区
(注：Java8中已经移除了永久代，新加了一个叫做元数据区的native内存区)

finalize()方法什么时候被调用？析构函数(finalization)的目的是什么？
垃圾回收器(garbage collector)决定回收某对象时，就会运行该对象的finalize()方法 但是在Java中很不幸，如果内存总是充足的，那么垃圾回收可能永远不会进行，也就是说filalize()可能永远不被执行，显然指望它做收尾工作是靠不住的。 那么finalize()究竟是做什么的呢？它最主要的用途是回收特殊渠道申请的内存。Java程序有垃圾回收器，所以一般情况下内存问题不用程序员操心。但有一种JNI(Java Native Interface)调用non-Java程序（C或C++），finalize()的工作就是回收这部分的内存。


<hr>

<h1>J2EE</h1>

1.BeanFactory和ApplicationContext（spring的核心容器）

ApplicationContext是BeanFactory的子类，因为古老的BeanFactory无法满足不断更新的spring的需求，于是ApplicationContext就基本上代替了BeanFactory的工作，以一种更面向框架的工作方式以及对上下文进行分层和实现继承，并在这个基础上对功能进行扩展：
<1>MessageSource, 提供国际化的消息访问
<2>资源访问（如URL和文件）
<3>事件传递
<4>Bean的自动装配
<5>各种不同应用层的Context实现

区别：

<1>如果使用ApplicationContext，如果配置的bean是singleton，那么不管你有没有或想不想用它，它都会被实例化。好处是可以预先加载，坏处是浪费内存。
<2>BeanFactory，当使用BeanFactory实例化对象时，配置的bean不会马上被实例化，而是等到你使用该bean的时候（getBean）才会被实例化。好处是节约内存，坏处是速度比较慢。多用于移动设备的开发。
<3>没有特殊要求的情况下，应该使用ApplicationContext完成。因为BeanFactory能完成的事情，ApplicationContext都能完成，并且提供了更多接近现在开发的功能。

2.IoC和DI

IoC叫控制反转，是Inversion of Control的缩写，DI（Dependency Injection）叫依赖注入
依赖注入实际上就是向本来由代码控制的组件交给外部容器控制
注入方式有setter注入（实际开发中应该使用的），构造器注入，接口注入

3.Spring中的注解
• @Component: 可以使用此注解描述 Spring 中的 Bean ，但它是一个泛化的概念，仅仅表
示一个组件 (Bean ，并且可以作用在任何层次 使用时只需将该注解标注在相应类上即可
• @Repository: 用于将数据访问层( DAO 层)的类标识为 Spring 中的 Bean ，其功能与
@Component 相同
• @Service: 通常作用在业务层( Service ，用于将业务层的类标识为 Spring 中的 Bean
其功能与@Component 相同
• @Controller: 通常作用在控制层(如 Spring MVC Controller ，用于将控制层的类标识
Spring 中的 Bean ，其功能与@Component 相同
• @Autowired: 用于对 Bean 的属性变量、属性的 setter 方法及构造方法进行标注，配合对
应的注解处理器完成 Bean 的自动配置工作 默认按照 Bean 的类型进行装配
• @Resource: 其作用与 Autowired 一样 其区别在于@Autowired 默认按照 Bean 类型装
配，而@Resource 默认按照 Bean 实例名称进行装配 @Resource 中有两个重要属性: name
type Spring name 属性解析为 Bean 实例名称， type 属性解析为 Bean 实例类型 如果
指定 name 属性，贝IJ 按实例名称进行装配;如果指定 type 属性，则按 Bean 类型进行装配;如
果都不指定，则先按 Bean 实例名称装配，如果不能匹配，再按照 Bean 类型进行装自己;如果都
无法匹配，则抛出 NoSuchBeanDefinitionException 异常
• @Qualifier: @Autowired 注解配合使用，会将默认的按 Bean 类型装配修改为接 Bean
的实例名称装配， Bean 的实例名称由 @Qualifier 注解的参数指定
在上面几个注解中，虽然@Repository @Service @Controller 功能与@Component 注解
的功能相同，但为了使标注类本身用途更加清晰，建议在实际开发中使用@Repository @Service
@Controller 分别对实现类进行标注

4.Spring AOP

AOP 的全称是 Aspect-Oriented Programming ，即面向切面编程(也称面向方面编程)
是面向对象编程 (OOP) 的一种补充

