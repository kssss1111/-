# 一、容器

## I、单例集合

### Collection接口介绍

Collection 表示一组对象，它是集中、收集的意思。Collection接口的两个子接口是List、Set接口。

![image-20220424103542824-16507677441111](https://www.itbaizhan.com/wiki/imgs/image-20220424103542824-16507677441111.png)

Collection接口中定义的方法

| **方法**                          | **说明**                                      |
| --------------------------------- | --------------------------------------------- |
| boolean add(Object element)       | 增加元素到容器中                              |
| boolean remove(Object element)    | 从容器中移除元素                              |
| boolean contains(Object element)  | 容器中是否包含该元素                          |
| int size()                        | 容器中元素的数量                              |
| boolean isEmpty()                 | 容器是否为空                                  |
| void clear()                      | 清空容器中所有元素                            |
| Iterator iterator()               | 获得迭代器，用于遍历所有元素                  |
| boolean containsAll(Collection c) | 本容器是否包含c容器中的所有元素               |
| boolean addAll(Collection c)      | 将容器c中所有元素增加到本容器                 |
| boolean removeAll(Collection c)   | 移除本容器和容器c中都包含的元素               |
| boolean retainAll(Collection c)   | 取本容器和容器c中都包含的元素，移除非交集元素 |
| Object[] toArray()                | 转化成Object数组                              |

> 由于List、Set是Collection的子接口，意味着所有List、Set的实现类都有上面的方法。

> JDK8之后，Collection接口新增的方法（将在JDK新特性和函数式编程中介绍）：
>
> | 新增方法              | 说明                                                         |
> | --------------------- | ------------------------------------------------------------ |
> | removeIf              | 作用是删除容器中所有满足filter指定条件的元素                 |
> | stream parallelStream | stream和parallelStream 分别返回该容器的Stream视图表示，不同之处在于parallelStream()返回并行的Stream，Stream是Java函数式编程的核心类。 |
> | spliterator           | 可分割的迭代器，不同以往的iterator需要顺序迭代，Spliterator可以分割为若干个小的迭代器进行并行操作，可以实现多线程操作提高效率 |

**实时效果反馈**

**1**.**如下哪个接口不是Collection接口的子接口?**

A List

B Set

C Map

D Queue

**答案**

1=>C

## II、 List接口介绍

![image-20220424153210704-16507855316696](https://www.itbaizhan.com/wiki/imgs/image-20220424153210704-16507855316696.png)

**List接口特点**

List是有序、可重复的容器。

**有序：**有序(元素存入集合的顺序和取出的顺序一致)。List中每个元素都有索引标记。可以根据元素的索引标记（在List中的位置）访问元素，从而精确控制这些元素。

**可重复：**List允许加入重复的元素。更确切地讲，List通常允许满足 e1.equals(e2) 的元素重复加入容器。

**List接口中的常用方法**

除了Collection接口中的方法，List多了一些跟顺序(索引)有关的方法，参见下表：

| **方法**                              | **说明**                                           |
| ------------------------------------- | -------------------------------------------------- |
| void add (int index, Object element)  | 在指定位置插入元素，以前元素全部后移一位           |
| Object set (int index,Object element) | 修改指定位置的元素                                 |
| Object get (int index)                | 返回指定位置的元素                                 |
| Object remove (int index)             | 删除指定位置的元素，后面元素全部前移一位           |
| int indexOf (Object o)                | 返回第一个匹配元素的索引，如果没有该元素，返回-1.  |
| int lastIndexOf (Object o)            | 返回最后一个匹配元素的索引，如果没有该元素，返回-1 |

**实时效果反馈**

**1**.**如下哪个选项是List接口的特点？**

A 有序，可重复

B 有序，不可重复

C 无序，可重复

D 无序，不可重复

**答案**

1=>A

##  III、ArrayList容器的基本使用

![image-20220425095829813-16508519111341](https://www.itbaizhan.com/wiki/imgs/image-20220425095829813-16508519111341.png)

ArrayList是List接口的实现类。是List存储特征的具体实现。

ArrayList底层是用数组实现的存储。 特点：查询效率高，增删效率低，线程不安全。

```java
public class ArrayListTest {
    public static void main(String[] args) {
        //实例化ArrayList容器
        List<String> list  = new ArrayList<>();
        //添加元素
        boolean flag1 = list.add("oldlu");
        boolean flag2 = list.add("itbz");
        boolean flag3 = list.add("sxt");
        boolean flag4 = list.add("sxt");
        System.out.println(flag1+"\t"+flag2+"\t"+flag3+"\t"+flag4);   
        //删除元素
        boolean flag4 = list.remove("oldlu");
        System.out.println(flag4);

        //获取容器中元素的个数
        int size = list.size();
        System.out.println(size);

        //判断容器是否为空
        boolean empty = list.isEmpty();
        System.out.println(empty);

        //容器中是否包含指定的元素
        boolean value = list.contains("itbz");
        System.out.println(value);
              
        //清空容器
        list.clear();
        Object[] objects1 = list.toArray();
        System.out.println(Arrays.toString(objects1));
    }
}

```

## IV、LinkedList容器介绍

LinkedList底层用双向链表实现的存储。特点：查询效率低，增删效率高，线程不安全。

双向链表也叫双链表，是链表的一种，它的每个数据节点中都有两个指针，分别指向前一个节点和后一个节点。 所以，从双向链表中的任意一个节点开始，都可以很方便地找到所有节点。

**LinkedList的存储结构图**

![image-20220122150906353](https://www.itbaizhan.com/wiki/imgs/image-20220122150906353.png)

每个节点都应该有3部分内容：

```
1
class  Node<E> {
2
        Node<E>  previous;    //前一个节点
3
        E  element;          //本节点保存的数据
4
        Node<E> next;        //后一个节点
5
}
```

**List实现类的选用规则**

> 如何选用ArrayList、LinkedList、Vector?
>
> 1. 需要线程安全时，用Vector。
> 2. 不存在线程安全问题时，并且查找较多用ArrayList（一般使用它）
> 3. 不存在线程安全问题时，增加或删除元素较多用LinkedList

**实时效果反馈**

**1**.**LinkedList容器底层是用什么结构存储元素的？**

A 双向链表

B 数组

C 队列

D 树

**答案**

1=>A

## V、 Set接口介绍

![image-20220427145445513-16510424866091](https://www.itbaizhan.com/wiki/imgs/image-20220427145445513-16510424866091.png)

Set接口继承自Collection接口，Set接口中没有新增方法，它和Collection接口保持完全一致。我们在前面学习List接口的使用方式，在Set中仍然适用。因此，学习Set的使用将没有任何难度。

**Set接口特点**

Set特点：无序、不可重复。无序指Set中的元素没有索引，我们只能遍历查找；不可重复指不允许加入重复的元素。更确切地讲，新元素如果和Set中某个元素通过equals()方法对比为true，则只能保留一个。

Set常用的实现类有：HashSet、TreeSet等，我们一般使用HashSet。

**实时效果反馈**

**1**.**如下哪个选项是Set接口的特点？**

A 有序，可重复

B 有序，不可重复

C 无序，可重复

D 无序，不可重复

**答案**

1=>D

##  VI、单例集合使用案例

需求：

产生1-10之间的随机数([1,10]闭区间)，将不重复的10个随机数放到容器中。

### **使用List类型容器实现**

```java
public class ListDemo {
    public static void main(String[] args) {
        List<Integer> list = new ArrayList<>();
       while(true){
           //产生随机数
           int num = (int)(Math.random()*10+1);
            //判断当前元素在容器中是否存在
           if(!list.contains(num)){
                list.add(num);
           }
           //结束循环
           if(list.size() == 10){
               break;
           }
       }
       for(Integer i:list){
           System.out.println(i);
       }
    }
}

```

### **使用Set类型容器实现**

```java
public class SetDemo {
    public static void main(String[] args) {
        Set<Integer> set = new HashSet<>();
        while(true){
            int num = (int)(Math.random()*10+1);
            //将元素添加容器中，由于Set类型容器是不允许有重复元素的，所以不需要判断。
            set.add(num);
            //结束循环
            if(set.size() == 10){
                break;
            }
        }
        for(Integer i:set){
            System.out.println(i);
        }
    }
}

```

## 双例集合

![image-20220430154550065-16513047510453](https://www.itbaizhan.com/wiki/imgs/image-20220430154550065-16513047510453.png)

## VII、Map接口介绍**

Map接口定义了双例集合的存储特征，它并不是Collection接口的子接口。双例集合的存储特征是以key与value结构为单位进行存储。体现的是数学中的函数 y=f(x)感念。

Map与Collecton的区别：

- Collection中的容器，元素是孤立存在的（理解为单身），向集合中存储元素采用一个个元素的方式存储。
- Map中的容器，元素是成对存在的(理解为现代社会的夫妻)。每个元素由键与值两部分组成，通过键可以找对所对应的值。
- Collection中的容器称为单列集合，Map中的容器称为双列集合。
- Map中的集合不能包含重复的键，值可以重复；每个键只能对应一个值。
- Map中常用的容器为HashMap，TreeMap等。

**Map接口中常用的方法表**

| 方法                                | 说明                                            |
| ----------------------------------- | ----------------------------------------------- |
| V put (K key,V value)               | 把key与value添加到Map集合中                     |
| void putAll(Map m)                  | 从指定Map中将所有映射关系复制到此Map中          |
| V remove (Object key)               | 删除key对应的value                              |
| V get(Object key)                   | 根据指定的key，获取对应的value                  |
| boolean containsKey(Object key)     | 判断容器中是否包含指定的key                     |
| boolean containsValue(Object value) | 判断容器中是否包含指定的value                   |
| Set keySet()                        | 获取Map集合中所有的key，存储到Set集合中         |
| Set<Map.Entry<K,V>> entrySet()      | 返回一个Set基于Map.Entry类型包含Map中所有映射。 |
| void clear()                        | 删除Map中所有的映射                             |

**实时效果反馈**

**1**.**如下对Map描述错误的是？**

A Map接口定义的存储特征是键值对；

B Map接口是双例集合的根接口；

C Map中一个Key只能有一个Value与之对应；

D Map接口是Collection接口的子接口；

**2**.**在Map中添加元素的方法是？**

A put

B add

C insert

D addKV

**答案**

1=>D 2=>A

###  1、HashMap容器的使用

HashMap采用哈希算法实现，是Map接口最常用的实现类。 由于底层采用了哈希表存储数据，我们要求键不能重复，如果发生重复，新的键值对会替换旧的键值对。 HashMap在查找、删除、修改方面都有非常高的效率。

```java
public class HashMapTest {
    public static void main(String[] args) {
        //实例化HashMap容器
        Map<String,String> map = new HashMap<>();


        //添加元素
        map.put("a","A");
        map.put("b","B");
        map.put("c","C");
        map.put("a","D");


        //获取容器中元素数量
        int size = map.size();
        System.out.println(size);
        System.out.println("---------------");


        //获取元素
        //方式一
        String v = map.get("a");
        System.out.println(v);
        System.out.println("---------------");


        //方式二
        Set<String> keys = map.keySet();
        for(String key:keys){
            String v1 = map.get(key);
            System.out.println(key+" ---- "+v1);
        }
        System.out.println("-------------------");


        //方式三
        Set<Map.Entry<String,String>> entrySet = map.entrySet();
        for(Map.Entry<String,String> entry:entrySet){
            String key = entry.getKey();
            String v2 = entry.getValue();
            System.out.println(key+" ---------- "+v2);
        }


        System.out.println("--------------------");
        //Map容器的并集操作
        Map<String,String> map2 = new HashMap<>();
        map2.put("f","F");
        map2.put("c","CC");
        map.putAll(map2);
        Set<String> keys2 = map.keySet();
        for(String key:keys2){
            System.out.println("key: "+key+" Value: "+map.get(key));
        }


        System.out.println("---------------");
        //删除元素
        String v3 = map.remove("a");
        System.out.println(v3);
        Set<String> keys3 = map.keySet();
        for(String key:keys3){
            System.out.println("key: "+key+" Value: "+map.get(key));
        }


        System.out.println("-------------------");
        //判断Key是否存在
        boolean b = map.containsKey("b");
        System.out.println(b);
        //判断Value是否存在
        boolean cc = map.containsValue("CC");
        System.out.println(cc);


    }
}

```

### 2、HashMap的底层源码分析

**底层存储介绍**

HashMap底层实现采用了哈希表，这是一种非常重要的数据结构。对于我们以后理解很多技术都非常有帮助。

数据结构中由数组和链表来实现对数据的存储，他们各有特点。

(1) 数组：占用空间连续。 寻址容易，查询速度快。但是，增加和删除效率非常低。

(2) 链表：占用空间不连续。 寻址困难，查询速度慢。但是，增加和删除效率非常高。

那么，我们能不能结合数组和链表的优点（即查询快，增删效率也高）呢？ 答案就是“哈希表”。 哈希表的本质就是“数组+链表”。

![image-20220501100238040-16513705589873](https://www.itbaizhan.com/wiki/imgs/image-20220501100238040-16513705589873.png)

> **Oldlu建议**
>
> 对于本章中频繁出现的“底层实现”讲解，建议学有余力的童鞋将它搞通。刚入门的童鞋如果觉得有难度，可以暂时跳过。入门期间，掌握如何使用即可，底层原理是扎实内功，便于大家应对一些大型企业的笔试面试。

 Iterator接口

![image-20220502160603395-16514787645225](https://www.itbaizhan.com/wiki/imgs/image-20220502160603395-16514787645225.png)

## VIII、Iterator迭代器接口介绍

Collection接口继承了Iterable接口，在该接口中包含一个名为iterator的抽象方法，所有实现了Collection接口的容器类对该方法做了具体实现。iterator方法会返回一个Iterator接口类型的迭代器对象，在该对象中包含了三个方法用于实现对单例容器的迭代处理。

**Iterator对象的工作原理：**

![image-20220502155537969-16514781392653](https://www.itbaizhan.com/wiki/imgs/image-20220502155537969-16514781392653.png)

**Iterator接口定义了如下方法：**

1. `boolean hasNext();` //判断游标当前位置的下一个位置是否还有元素没有被遍历；
2. `Object next();` //返回游标当前位置的下一个元素并将游标移动到下一个位置；
3. `void remove();` //删除游标当前位置的元素，在执行完next后该操作只能执行一次；

**实时效果反馈**

**1**.**Iterator接口的作用是？**

A 定义了迭代双例集合的标准；

B 定义了迭代单例集合的标准；

C 定义了迭代数组的标准；

D 定义了迭代树型结构的标准；

**答案**

1=>B

###  Iterator迭代器的使用

迭代List接口类型容器

```java
public class IteratorListTest {
    public static void main(String[] args) {
        //实例化容器
        List<String> list  = new ArrayList<>();
        list.add("a");
        list.add("b");
        list.add("c");
        //获取元素
        //获取迭代器对象
        Iterator<String> iterator = list.iterator();
        //方式一:在迭代器中，通过while循环获取元素
        while(iterator.hasNext()){
            String value = iterator.next();
            System.out.println(value);
        }
        System.out.println("-------------------------------");
        //方法二：在迭代器中，通过for循环获取元素
        for(Iterator<String> it = list.iterator();it.hasNext();){
            String value = it.next();
            System.out.println(value);
        }


    }
}

```

### 在迭代器中删除元素

```java
public class IteratorRemoveTest {
    public static void main(String[] args) {
        List<String> list = new ArrayList<>();
        list.add("a");
        list.add("b");
        list.add("c");
        list.add("d");
        Iterator<String> iterator = list.iterator();
        while(iterator.hasNext()){
            //不要在一次循环中多次调用next方法。
            String value = iterator.next();
            iterator.remove();
        }
        System.out.println("----------------");
        for(Iterator<String> it = list.iterator();it.hasNext();){
            System.out.println(it.next());
            list.add("dddd");
        }
    }
}

```

### 遍历集合的方法总结

遍历List方法一：普通for循环

```java

for(int i=0;i<list.size();i++){//list为集合的对象名

    String temp = (String)list.get(i);

    System.out.println(temp);

}
```

遍历List方法二：增强for循环(使用泛型！)

```java

for (String temp : list) {
    System.out.println(temp);
}
```

遍历List方法三：使用Iterator迭代器(1)

```java

for(Iterator iter= list.iterator();iter.hasNext();){
    String temp = (String)iter.next();
    System.out.println(temp);
}
```

遍历List方法四：使用Iterator迭代器(2)

```java

Iterator  iter =list.iterator();
while(iter.hasNext()){
    Object  obj =  iter.next();
    iter.remove();//如果要遍历时，删除集合中的元素，建议使用这种方式！
    System.out.println(obj);
}
```

遍历Set方法一：增强for循环

```java

for(String temp:set){
    System.out.println(temp);
}
```

遍历Set方法二：使用Iterator迭代器

```java

for(Iterator iter = set.iterator();iter.hasNext();){
    String temp = (String)iter.next();
    System.out.println(temp);
}
```

遍历Map方法一：根据key获取value

```java

Map<Integer, Man> maps = new HashMap<Integer, Man>();
Set<Integer>  keySet =  maps.keySet();
for(Integer id : keySet){
    System.out.println(maps.get(id).name);
}
```

遍历Map方法二：使用entrySet

```java

Set<Map.Entry<Integer, Man>>  ss = maps.entrySet();
for (Iterator<Map.Entry<Integer, Man>> iterator = ss.iterator(); iterator.hasNext();) {
    Map.Entry e =  iterator.next(); 
    System.out.println(e.getKey()+"--"+e.getValue()); 
}
```

##  IX、Collections工具类

![image-20220503150917485-16515617585952](https://www.itbaizhan.com/wiki/imgs/image-20220503150917485-16515617585952.png)

类 java.util.Collections 提供了对Set、List、Map进行排序、填充、查找元素的辅助方法。

| 方法名                         | 说明                                     |
| ------------------------------ | ---------------------------------------- |
| void sort(List)                | 对List容器内的元素排序，排序规则是升序。 |
| void shuffle(List)             | 对List容器内的元素进行随机排列           |
| void reverse(List)             | 对List容器内的元素进行逆续排列           |
| void fill(List, Object)        | 用一个特定的对象重写整个List容器         |
| int binarySearch(List, Object) | 对于顺序的List容器，折半查找查找特定对象 |

Collections工具类的常用方法

```java
public class CollectionsTest {
    public static void main(String[] args) {
        List<String> list = new ArrayList<>();
        list.add("c");
        list.add("b");
        list.add("a");
        //对元素排序
        Collections.sort(list);
        for(String str:list){
            System.out.println(str);
        }
        System.out.println("-------------------");


        List<Users> list2 = new ArrayList<>();
        Users u = new Users("oldlu",18);
        Users u2 = new Users("sxt",22);
        Users u3 = new Users("admin",22);
        list2.add(u);
        list2.add(u2);
        list2.add(u3);
        //对元素排序
        Collections.sort(list2);
        for(Users user:list2){
            System.out.println(user);
        }
        System.out.println("-------------------");


        List<Student> list3 = new ArrayList<>();
        Student s = new Student("oldlu",18);
        Student s1 = new Student("sxt",20);
        Student s2 = new Student("admin",20);
        
        list3.add(s);
        list3.add(s1);
        list3.add(s2);
        
        Collections.sort(list3,new StudentComparator());
        for(Student student:list3){
            System.out.println(student);
        }
        System.out.println("-------------------");


        List<String> list4 = new ArrayList<>();
        list4.add("a");
        list4.add("b");
        list4.add("c");
        list4.add("d");


        //洗牌
        Collections.shuffle(list4);
        for(String str:list4){
            System.out.println(str);
        }
    }
}

```

## X、Vector容器的基本使用

Vector底层是用数组实现的，相关的方法都加了同步检查，因此“线程安全,效率低”。 比如，indexOf方法就增加了synchronized同步标记。

![image-20220426091910943-16509359521281](https://www.itbaizhan.com/wiki/imgs/image-20220426091910943-16509359521281.png)

**Vector的使用**

Vector的使用与ArrayList是相同的，因为他们都实现了List接口，对List接口中的抽象方法做了具体实现。

```java
public class VectorTest {
    public static void main(String[] args) {


        //实例化Vector
        List<String> v = new Vector<>();
        v.add("a");
        v.add("b");
        v.add("a");


        for(int i=0;i<v.size();i++){
            System.out.println(v.get(i));
        }
        System.out.println("----------------------");
        for(String str:v){
            System.out.println(str);
        }
    }
}

```





# 二、IO流

- 按流的方向分类：

  - 输入流：数据源到程序(InputStream、Reader读进来)。
  - 输出流：程序到目的地(OutputStream、Writer写出去)。

  

- 按流的处理数据单元分类：

  - 字节流：按照字节读取数据(InputStream、OutputStream)。
  - 字符流：按照字符读取数据(Reader、Writer)。

- 按流的功能分类：

  - 节点流：可以直接从数据源或目的地读写数据。
  - 处理流：不直接连接到数据源或目的地，是处理流的流。通过对其他流的处理提高程序的性能。

- IO的四个基本抽象类：InputStream、OutputStream、Reader、Writer

- InputStream的实现类：

  - FileInputStream(文件字节输入流)

  - BufferedInputStream(缓冲字节输入流，也称为处理流)

  - DataInputStream(数据字节输入流)

    ```java
    public class TestDataStream {
        public static void main(String[] args) {
            // 创建数据输出流对象与文件字节输出流对象
            try (DataOutputStream dos = new DataOutputStream(new FileOutputStream("F:/data"));
            // 创建数据输入流对象和文件字节输入流对象
                 DataInputStream dis = new DataInputStream(new FileInputStream("F:/data"))
                 ){
                // 将如下数据写入到文件中
                dos.writeChar('a');
                dos.writeInt(10);
                dos.writeDouble(Math.random());
                dos.writeBoolean(true);
                dos.writeUTF("呜呜呜");
                dos.flush();
                // 直接读取数据：读取的顺序需要与写入的顺序一致，否则不能正确读取数据
                System.out.println("char:" + dis.readChar());
                System.out.println("int:" + dis.readInt());
                System.out.println("double:" + dis.readDouble());
                System.out.println("boolean:" + dis.readBoolean());
                System.out.println("String:" + dis.readUTF());
    
            }catch (Exception e){
                e.printStackTrace();
            }
        }
    }
    ```

    

  - ObjectInputStream(对象字节输入流): 

    注：readObject()方法源输入流中读取字节序列，再把它们反序列化成为一个对象，并将其返回；
    
    ```java
    public class TestObjectInputStream {
        public static void main(String[] args) {
            // 创建对象字节输入流与文件字节输入流
            try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream("F:/data3"))){
                // 反序列化处理
                Users users = (Users) ois.readObject();
                System.out.println(users);
    
            }catch (Exception e){
                e.printStackTrace();
            }
        }
    }
    ```
    
    

- OutputStream的实现类：

  - FileOutputStream(文件字节输出流)

    ```java
    import java.io.FileOutputStream;
    import java.io.IOException;
    
    public class TestFileOutputStream {
        public static void main(String[] args) {
            // true:表示内容会追加到文件的末尾，false（默认）：表示重写（覆盖原来的内容）整个文件的内容
            try (FileOutputStream fos = new FileOutputStream("F:/a.txt",true)){
                // 准备输出的数据
                String str = "Old lu";
                fos.write(str.getBytes());
                // 刷新将数据从内存中写入到磁盘中
                fos.flush();
            }catch (IOException e){
                e.printStackTrace();
            }
        }
    }
    ```

    

  - BufferedOutputStream(缓冲字节输出流,也称为处理流)

  - DataOutputStream(数据字节输出流)

  - ObjectOutputStream(对象字节输出流)

    注：writeObject(Object obj)方法可以对参数指定的obj对象进行序列化，把得到的字节序列写到一个目标输出流中；

  - ```java
    public class TestObjectOutputStream {
        public static void main(String[] args) {
            // 创建对象输出字节流与文件字节输出流对象
            try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream("F:/data3"))){
                // 创建Users对象
                Users u = new Users();
                u.setUserage("20");
                u.setUsername("李四");
                u.setUserId(1);
    
                // 将Users对象序列化到文件中
                oos.writeObject(u);
                // 刷新
                oos.flush();
    
            }catch (Exception e){
                e.printStackTrace();
            }
        }
    }
    ```

    

- Reader的实现类

  - FileReader(文件字符输入流)

    ```java
    
    public class TestFileReader {
        public static void main(String[] args) {
            try (FileReader fr = new FileReader("F:/a.txt")){
                StringBuilder sb = new StringBuilder();
                int temp = 0;
                while ((temp = fr.read()) != -1){
                    sb.append((char) temp);
                }
                System.out.println(sb);
            }catch (IOException e){
                e.printStackTrace();
            }
        }
    }
    ```

    

  - BufferedReader(字符缓冲输入流)

    ```java
    public class TestBufferedReader {
        public static void main(String[] args) {
            // 创建字符输入缓冲流以及文件字符流对象
            try (BufferedReader br = new BufferedReader(new FileReader("F:/aa.txt"))){
                // 操作字符输入缓冲流
                String str = "";
                while ((str = br.readLine()) != null){
                    System.out.println(str);
                }
            }catch (IOException e){
                e.printStackTrace();
            }
        }
    }
    ```

    

  - InputStreamReader(字节到字符的转换流)

    ```java
    public class TestInputStreamReader {
        public static void main(String[] args) {
            //创建文件字节输入流对象
            try (FileInputStream fis = new FileInputStream("F:/sxt3.txt");
                 //创建转换流(字节到字符的转换)流对象，并在该对象中指定编码。
                 InputStreamReader isr = new InputStreamReader(fis,"GBK")){
                StringBuilder sb = new StringBuilder();
                //操作流对象
                int temp = 0;
                while ((temp = isr.read()) != -1){
                    sb.append((char) temp);
                }
                System.out.println(sb);
    
            }catch (IOException e){
                e.printStackTrace();
            }
        }
    }
    ```

    

- Writer的实现类

  - FileWriter(文件字符输出流)

  - ```java
    public class TestFileWriter {
        public static void main(String[] args) {
            try (FileWriter fw = new FileWriter("F:/aa.txt",true)){
    
                fw.write("邵风利！！\r\n");
                fw.write("傻逼！！\r\n");
                fw.flush();
            }catch (IOException e){
                e.printStackTrace();
            }
        }
    }
    ```

    

  - BufferedWriter(字符输出缓冲流)

    ```java
    public class TestBufferedWriter {
        public static void main(String[] args) {
            // 创建字符输出缓冲流以及文件字符输出流对象
            try (BufferedWriter bw = new BufferedWriter(new FileWriter("F:/sxt.txt"))){
                // 操作字符输出缓冲流
                bw.write("ni hao a!!");
                bw.write("456");
                // 换行
                bw.newLine();
                bw.write("我爱你！！");
                bw.newLine();
                bw.write("1314");
                bw.flush();
    
            }catch (IOException e){
                e.printStackTrace();
            }
        }
    }
    ```

    

  - OutputStreamWriter(字符到字节的转换流)

  - PrintWriter(打印流)

    ```java
    public class TestPrintWriter {
        public static void main(String[] args) {
            // 创建字符输出流对象
            try (PrintWriter pw = new PrintWriter("F:/sxt5.txt")){
                // 调用不带有换行方法完成内容输出
                pw.print("abc");
                pw.print("def");
                // 调用带有自动换行方法完成内容输出
                pw.println("oldli");
                pw.println("lsh");
                pw.flush();
    
            }catch (Exception e){
                e.printStackTrace();
            }
        }
    }
    ```

    

- 把Java对象转换为字节序列的过程称为对象的序列化。

- 把字节序列恢复为Java对象的过程称为对象的反序列化。



测试FileBufferStream：

```java
public class TestFileBufferStream {
    public static void main(String[] args) {
        long time1 = System.currentTimeMillis();
        copyFile("F:/1.jpg","F:/2.jpg");
        long time2 = System.currentTimeMillis();
        System.out.println((time2 - time1) + "ms");
    }

    /**
     *
     * @param source 源文件
     * @param destination 目的地文件
     */
    public static void copyFile(String source,String destination){
        // “后开先关”：try-with-resource按照io流对象被创建的顺序的逆序来关闭
        // 实例化 节点流对象
        try (FileInputStream fis = new FileInputStream(source);
             FileOutputStream fos = new FileOutputStream(destination);
             // 实例化 处理流对象
             BufferedInputStream bis = new BufferedInputStream(fis);
             BufferedOutputStream bos = new BufferedOutputStream(fos)){

            /*
            // 创建字节缓冲区
            byte[] buffer = new byte[1024];*/

            int temp = 0;
            while ((temp = bis.read()) != -1){
                bos.write(temp);
            }
            // 将数据从内存中写出到磁盘中
            fos.flush();
        }catch (IOException e){
            e.printStackTrace();
        }
    }
}
```

BufferedReader和BufferedWriter案例的使用(键盘输入，屏幕输出):

```java
public class TestKeyboardInput {
    public static void main(String[] args) {
        // 创建键盘输入相关的流对象
        try (BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
             // 创建向屏幕输出相关流对象
             BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out))){

            while (true) {
                bw.write("请输入：");
                bw.flush();
                // 获取键盘输入的字符串
                String input = br.readLine();
                // 判断输入的内容是否含有退出关键字
                if ("exit".equals(input) || "quit".equals(input)){
                    bw.write("Bye Bye!!");
                    bw.flush();
                    break;
                }
                bw.write("您输入的是：" + input);
                bw.newLine();
            }

        }catch (Exception e){
            e.printStackTrace();
        }
    }
}
```



## Apache-commons-io包的使用

### 	1、FileUtils类中常用方法的介绍

打开FileUtils的api文档，我们抽出一些工作中比较常用的方法，进行总结和讲解。总结如下：

| 方法名                | 使用说明                                                     |
| --------------------- | ------------------------------------------------------------ |
| cleanDirectory        | 清空目录，但不删除目录                                       |
| contentEquals         | 比较两个文件的内容是否相同                                   |
| copyDirectory         | 将一个目录内容拷贝到另一个目录。可以通过FileFilter过滤需要拷贝的文件 |
| copyFile              | 将一个文件拷贝到一个新的地址                                 |
| copyFileToDirectory   | 将一个文件拷贝到某个目录下                                   |
| copyInputStreamToFile | 将一个输入流中的内容拷贝到某个文件                           |
| deleteDirectory       | 删除目录                                                     |
| deleteQuietly         | 删除文件                                                     |
| listFiles             | 列出指定目录下的所有文件                                     |
| openInputSteam        | 打开指定文件的输入流                                         |
| readFileToString      | 将文件内容作为字符串返回                                     |
| readLines             | 将文件内容按行返回到一个字符串数组中                         |
| size                  | 返回文件或目录的大小                                         |
| write                 | 将字符串内容直接写到文件中                                   |
| writeByteArrayToFile  | 将字节数组内容写到文件中                                     |
| writeLines            | 将容器中的元素的toString方法返回的内容依次写入文件中         |
| writeStringToFile     | 将字符串内容写到文件中                                       |

读取文件内容，并输出到控制台上（只需一行代码！）

```java
public class TestFileUtilsDemo1 {
    public static void main(String[] args) throws Exception{
        String content = FileUtils.readFileToString(new File("F:/sxt.txt"), "UTF-8");
        System.out.println(content);
    }
}
```



### 	2、IOUtils的妙用

打开IOUtils的api文档，我们发现它的方法大部分都是重载的。所以，我们理解它的方法并不是难事。因此，对于方法的用法总结如下：

| 方法名                                  | 使用说明                                                   |
| --------------------------------------- | ---------------------------------------------------------- |
| buffer                                  | 将传入的流进行包装，变成缓冲流。并可以通过参数指定缓冲大小 |
| closeQueitly                            | 关闭流                                                     |
| contentEquals                           | 比较两个流中的内容是否一致                                 |
| copy                                    | 将输入流中的内容拷贝到输出流中，并可以指定字符编码         |
| copyLarge                               | 将输入流中的内容拷贝到输出流中，适合大于2G内容的拷贝       |
| lineIterator                            | 返回可以迭代每一行内容的迭代器                             |
| read                                    | 将输入流中的部分内容读入到字节数组中                       |
| readFully                               | 将输入流中的所有内容读入到字节数组中                       |
| readLine                                | 读入输入流内容中的一行                                     |
| toBufferedInputStream，toBufferedReader | 将输入转为带缓存的输入流                                   |
| toByteArray，toCharArray                | 将输入流的内容转为字节数组、字符数组                       |
| toString                                | 将输入流或数组中的内容转化为字符串                         |
| write                                   | 向流里面写入内容                                           |
| writeLine                               | 向流里面写入一行内容                                       |

我们没有必要对每个方法做测试，只是演示一下读入d:/sxt.txt文件内容到程序中，并转成String对象，打印出来。

**IOUtils的使用**

```java
public class TestIOUtilsDemo {
    public static void main(String[] args) throws Exception{
        String s = IOUtils.toString(new FileInputStream("F:/sxt.txt"), "UTF-8");
        System.out.println(s);
    }
}
```



# 三、线程

## 〇、什么是并发

并发是指在一段时间内同时做多个事情。当有多个线程在运行时,如果只有一个CPU,这种情况下计算机操作系统会采用并发技术实现并发运行，具体做法是采用“ 时间片轮询算法”，在一个时间段的线程代码运行时，其它线程处于就绪状。这种方式我们称之为并发。(Concurrent)。

![image-20211204095202680](https://www.itbaizhan.com/wiki/imgs/image-20211204095202680.png)

1. 串行(serial)：一个CPU上，按顺序完成多个任务
2. 并行(parallelism)：指的是任务数小于等于cpu核数，即任务真的是一起执行的
3. 并发(concurrency)：一个CPU采用时间片管理方式，交替的处理多个任务。一般是是任务数多余cpu核数，通过操作系统的各种任务调度算法，实现用多个任务“一起”执行（实际上总有一些任务不在执行，因为切换任务的速度相当快，看上去一起执行而已



## I、线程启动的三种方式：

### 	1.继承Thread类：

​	通过继承Thread类来创建并启动多线程步骤如下：

​	1、定义Thread类的子类，并重写该类的run()方法，该run()方法的方法体就代表了线程需要完成的任务。因此把run方法称为线程执行	体。

​	2、创建Thread子类的实例，即创建了线程对象。

​	3、调用线程对象的start()方法来启动该线程。
示例：

```java
public class TestThread extends Thread{  // 自定义类继承Thread类
    // run()方法是线程体
    @Override
    public void run() {
        for (int i = 0; i < 10; i++) {
            System.out.println(this.getName() + ":" + i); // getName()方法返回的是线程的名称
        }
    }

    public static void main(String[] args) {
        TestThread thread1 = new TestThread();  // 创建线程对象
        thread1.start(); // 启动线程
        TestThread thread2 = new TestThread();
        thread2.start();
    }
}
```

#### 	tip:线程的两个方法：

```
1.Thread.currentThread()，是Thread类的静态方法，该方法总是返回当前正在执行的线程对象。

 2.getName()：该方法是Thread类的实例方法，该方法返当前正在执行的线程的名称。在默认情况下，主线程的名称为main，用户启动的多线程的名称依次为Thread-0,Thread-1,Thread-3..Thread-n等。
```



### 	2.实现Runnable接口：

​	实现Runnable接口创建并启动多线程的步骤如下：

​	1.定义Runnable接口的实现类，并重写该接口的run方法，该run方法的方法体同样是该线程的线程执行体

​	2.创建Runnable实现类的实例对象，并以此实例对象作为Thread的target来创建Thread类，该Thread对象才是真正的线程对象。

​	3.调用线程对象的start()方法来启动该线程。

示例：

```java
public class TestThread2 implements Runnable{
    // 线程方法
    @Override
    public void run() {
        for (int i = 0; i < 10; i++) {
            System.out.println(Thread.currentThread().getName() + ": " + i);
        }
    }

    public static void main(String[] args) {
        // 包装成线程对象
        Thread thread1 = new Thread(new TestThread2());
        thread1.start();

        Thread thread2 = new Thread(new TestThread2());
        thread2.start();
    }
}
```

### 3、通过Callable和Future创建对象

​	1、定义一个实现Callable接口的类，并实现call()方法，该call方法将作为线程执行体，并且有返回值
​	2、创建该类的实例
​	3、创建FutureTask的实例，即使用FutrueTask类来包装Callable对象
​	4、将FutureTask的实例作为Thread的target创建并启动新线程
​	5、调用FutureTask对象的get()方法来获得子线程执行结束后的返回值 

示例：

```java
public class CallableDemo implements Callable<String> {
	@Override
	public String call() throws Exception {
		System.out.println(Thread.currentThread().getName()+"-启动了...");
		Thread.sleep(3000);
		return "Lisa";
	}

	public static void main(String[] args) throws Exception {
		Callable callable = new CallableDemo();
		FutureTask<String> task = new FutureTask(callable);
		Thread thread = new Thread(task);
		thread.start();
		// get()方法会阻塞
		String result = task.get();
		System.out.println(result);
		System.out.println(Thread.currentThread().getName()+"-运行结束.");
	}
}
输出：
Thread-0-启动了...
Lisa
main-运行结束.
```



## II、线程状态和生命周期

![image-20220123101751746](https://www.itbaizhan.com/wiki/imgs/image-20220123101751746.png)

一个线程对象在它的生命周期内，需要经历5个状态。

1. 新生状态(New)

   用new关键字建立一个线程对象后，该线程对象就处于新生状态。处于新生状态的线程有自己的内存空间，通过调用start方法进入就绪状态。

2. 就绪状态(Runnable)

   处于就绪状态的线程已经具备了运行条件，但是还没有被分配到CPU，处于“线程就绪队列”，等待系统为其分配CPU。就绪状态并不是执行状态，当系统选定一个等待执行的Thread对象后，它就会进入执行状态。一旦获得CPU，线程就进入运行状态并自动调用自己的run方法。有4种原因会导致线程进入就绪状态：

   1. 新建线程：调用start()方法，进入就绪状态；
   2. 阻塞线程：阻塞解除，进入就绪状态；
   3. 运行线程：调用yield()方法，直接进入就绪状态；
   4. 运行线程：JVM将CPU资源从本线程切换到其他线程。

3. 运行状态(Running)

   在运行状态的线程执行自己run方法中的代码，直到调用其他方法而终止或等待某资源而阻塞或完成任务而死亡。如果在给定的时间片内没有执行结束，就会被系统给换下来回到就绪状态。也可能由于某些“导致阻塞的事件”而进入阻塞状态。

4. 阻塞状态(Blocked)

   阻塞指的是暂停一个线程的执行以等待某个条件发生（如某资源就绪）。

   > 1. ```java
   >    有4种原因会导致阻塞：
   >                                                             
   >    1. 执行sleep(int millsecond)方法，使当前线程休眠，进入阻塞状态。当指定的时间到了后，线程进入就绪状态。
   >    2. 执行wait()方法，使当前线程进入阻塞状态。当使用nofity()方法唤醒这个线程后，它进入就绪状态。
   >    3. 线程运行时，某个操作进入阻塞状态，比如执行IO流操作(read()/write()方法本身就是阻塞的方法)。只有当引起该操作阻塞的原因消失后，线程进入就绪状态。
   >    4. join()线程联合: 当某个线程等待另一个线程执行结束后，才能继续执行时，使用join()方法。
   >    ```

5. 死亡状态(Terminated)

   死亡状态是线程生命周期中的最后一个阶段。线程死亡的原因有两个。一个是正常运行的线程完成了它run()方法内的全部工作； 另一个是线程被强制终止，如通过执行stop()或destroy()方法来终止一个线程（注：stop()/destroy()方法已经被JDK废弃，不推荐使用）。

   当一个线程进入死亡状态以后，就不能再回到其它状态了。



## III、终止线程的典型方式

1. 终止线程我们一般不使用JDK提供的stop()/destroy()方法(它们本身也被JDK废弃了)。通常的做法是提供一个boolean型的终止变量，当这个变量置为false，则终止线程的运行。


示例：

```java
public class TestStopThread implements Runnable{
    // 生死牌： true：生  false：死
    private boolean flag = true;
    @Override
    public void run() {
        System.out.println(Thread.currentThread().getName() + "线程开始！");
        int i = 0;
        while (this.flag){
            System.out.println(Thread.currentThread().getName() + " " + i++);
            try {
                Thread.sleep(1000);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
        System.out.println(Thread.currentThread().getName() + "线程结束！");
    }
    // 控制生死牌内容的方法
    public void stop(){
        this.flag = false;
    }

    public static void main(String[] args) {
        System.out.println("主线程开始！");
        TestStopThread tst = new TestStopThread();
        Thread t = new Thread(tst);
        t.start();
        try {
            System.in.read();
        } catch (IOException e) {
            e.printStackTrace();
        }
        tst.stop();
        System.out.println("主线程结束！");
    }
}
```



## IV、线程休眠

sleep()方法：可以让正在运行的线程进入阻塞状态，直到休眠时间满了，进入就绪状态。sleep方法的参数为休眠的毫秒数。

示例：

```java
public class TestSleepThread implements Runnable{
    @Override
    public void run() {
        System.out.println(Thread.currentThread().getName() + "线程开始");
        for (int i = 0; i < 20; i++) {
            System.out.println(Thread.currentThread().getName() + " " + i);
            // 线程休眠1秒
            try {
                Thread.sleep(1000);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
    }

    public static void main(String[] args) {
        System.out.println("主线程开始");
        Thread t = new Thread(new TestSleepThread());
        t.start();
        System.out.println("主线程结束");
    }
}
```

## V、线程让步

![image-20220520144720774](https://www.itbaizhan.com/wiki/imgs/image-20220520144720774-16530292416368.png)

yield()让当前正在运行的线程回到就绪状态，以允许具有相同优先级的其他线程获得运行的机会。因此，使用yield()的目的是让具有相同优先级的线程之间能够适当的轮换执行。但是，实际中无法保证yield()达到让步的目的，因为，让步的线程可能被线程调度程序再次选中。

使用yield方法时要注意的几点：

- yield是一个静态的方法。
- 调用yield后，yield告诉当前线程把运行机会交给具有相同优先级的线程。
- yield不能保证，当前线程迅速从运行状态切换到就绪状态。
- yield只能是将当前线程从运行状态转换到就绪状态，而不能是等待或者阻塞状态

示例：

```java
public class TestYieldThread implements Runnable{
    @Override
    public void run() {
        for (int i = 0; i < 20; i++) {
            if ("Thread-0".equals(Thread.currentThread().getName())){
                if (i == 0){
                    System.out.println("让步！");
                    Thread.yield();
                }
            }
            System.out.println(Thread.currentThread().getName() + " " + i);
        }
    }

    public static void main(String[] args) {
        Thread t1 = new Thread(new TestYieldThread());
        Thread t2 = new Thread(new TestYieldThread());
        t1.start();
        t2.start();
    }
}
```

## VI、线程联合

![image-20220520160125022](https://www.itbaizhan.com/wiki/imgs/image-20220520160125022-16530336861169.png)

当前线程邀请调用方法的线程优先执行，在调用方法的线程执行结束之前，当前线程不能再次执行。线程A在运行期间，可以调用线程B的join()方法，让线程B和线程A联合。这样，线程A就必须等待线程B执行完毕后，才能继续执行。

### **join方法的使用**

join()方法就是指调用该方法的线程在执行完run()方法后，再执行join方法后面的代码，即将两个线程合并，用于实现同步控制。

示例：

```java
class A implements Runnable{
    private Thread b;
    public A(Thread b){
        this.b = b;
    }
    @Override
    public void run() {
        for (int i = 0; i < 10; i++) {
            System.out.println(Thread.currentThread().getName() + " " + " A "+ i);
            if (i == 5){
                try {
                    this.b.join();
                } catch (InterruptedException e) {
                    e.printStackTrace();
                }
            }
            try {
                Thread.sleep(1000);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
    }
}

class B implements Runnable{
    @Override
    public void run() {
        for (int i = 0; i < 20; i++) {
            System.out.println(Thread.currentThread().getName() + " "  + " B "+ i);
            try {
                Thread.sleep(1000);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
    }
}


public class TestJoinThread {
    public static void main(String[] args) {
        Thread t1 = new Thread(new B());
        Thread t = new Thread(new A(t1));
        t.start();
        t1.start();
        for (int i = 0; i < 10; i++) {
            System.out.println(Thread.currentThread().getName() + " " + i);
            if (i == 2){
                try {
                    t.join();
                } catch (InterruptedException e) {
                    e.printStackTrace();
                }
            }
            try {
                Thread.sleep(1000);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
    }
}
```

### **线程联合案例**

```java
/**
 * 儿子买烟线程
 */
class SonThread implements Runnable{
    @Override
    public void run() {
        System.out.println("儿子出门买烟");
        System.out.println("儿子买烟需要十分钟");
        for (int i = 1; i <= 10; i++) {
            System.out.println("第" + i +"分钟");
            try {
                Thread.sleep(1000);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
        System.out.println("儿子买烟回来了！");
    }
}

/**
 * 爸爸抽烟线程
 */
class FatherThread implements Runnable{
    @Override
    public void run() {
        System.out.println("爸爸想抽烟，发现烟抽完了");
        System.out.println("爸爸让儿子去买包红塔山");
        // 启动儿子买烟线程
        Thread t = new Thread(new SonThread());
        t.start();
        // 爸爸需要等待儿子买烟回来。需要线程联合
        try {
            t.join();
        } catch (InterruptedException e) {
            e.printStackTrace();
            // 儿子跑丢了。或者忘记买烟
            System.out.println("爸爸出门找儿子");
            System.exit(1);
        }
        System.out.println("爸爸高兴地接过烟，并把零钱给了儿子！");
    }
}

public class TestJoinDemo {
    public static void main(String[] args) {
        System.out.println("爸爸抽烟儿子买烟的故事：");
        Thread t = new Thread(new FatherThread());
        t.start();
    }
}
```



## VII、Thread类中其他常用方法

### 1、获取当前线程名称

方式一

this.getName()获取线程名称，该方法适用于继承Thread实现多线程方式。

```java
class thread extends Thread{
    @Override
    public void run() {
        System.out.println(this.getName() + " Thread ");
    }
}
```

方式二

Thread.currentThread().getName()获取线程名称，该方法适用于实现Runnable接口实现多线程方式。

```java
class runnable implements Runnable{
    @Override
    public void run() {
        System.out.println(Thread.currentThread().getName() + " Runnable ");
    }
}
```

## VIII、设置线程的名称

方式一

通过构造方法设置线程名称。

```java
class SetName1 extends Thread{
    public SetName1(String name){
        super(name);
    }

    @Override
    public void run() {
        System.out.println(this.getName());
    }
}

public class TestSetNameThread {
    public static void main(String[] args) {
        SetName1 setName1 = new SetName1("SetName1");
        setName1.start();
    }
}
```

方式二

通过setName()方法设置线程名称。

```java
class SetName2 implements Runnable{
    @Override
    public void run() {
        System.out.println(Thread.currentThread().getName());
    }
}

public class TestSetNameThread {
    public static void main(String[] args) {

        Thread t = new Thread(new SetName2());
        // 要在start()方法之前调用setName()方法
        t.setName("SetName2");
        t.start();
    }
}
```

## IX、判断线程是否存活

isAlive()方法： 判断当前的线程是否处于活动状态。

活动状态是指线程已经启动且尚未终止(新生状态、死亡状态)，线程处于就绪或运行或阻塞的状态，就认为线程是存活的。

```java
class Alive implements Runnable{
    @Override
    public void run() {
        for (int i = 0; i < 4; i++) {
            System.out.println(Thread.currentThread().getName() + " " + i);
            try {
                Thread.sleep(500);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
    }
}

public class TestAliveThread {
    public static void main(String[] args) {
        Thread t = new Thread(new Alive());
        // 修改线程名称
        t.setName("Alive");
        t.start();
        System.out.println(t.getName() + " " + t.isAlive());
        try {
            Thread.sleep(4000);
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
        System.out.println(t.getName() + " " + t.isAlive());
    }
}
```

## X、线程的优先级

### 	1、什么是线程的优先级

每一个线程都是有优先级的，我们可以为每个线程定义线程的优先级，但是这并不能保证高优先级的线程会在低优先级的线程前执行。线程的优先级用数字表示，范围从1到10，一个线程的缺省优先级是5。

Java 的线程优先级调度会委托给操作系统去处理，所以与具体的操作系统优先级有关，如非特别需要，一般无需设置线程优先级。

> **注意**
>
> 线程的优先级，不是说哪个线程优先执行，如果设置某个线程的优先级高。那就是有可能被执行的概率高。并不是优先执行。

**实时效果反馈**

**1. 如下对线程优先级描述错误的是？**

A 线程的优先级用数字表示；

B 高优先级的线程不能保证会在低优先级的线程前执行；

C 高优先级的线程会绝对优先执行；

D 一个线程的缺省优先级是5；

**答案**

1=>C



### 2、线程优先级的使用

使用下列方法获得或设置线程对象的优先级。

- int getPriority();
- void setPriority(int newPriority);

> **注意：**优先级低只是意味着获得调度的概率低。并不是绝对先调用优先级高的线程后调用优先级低的线程。

```java
class Priority implements Runnable{
    // 定义执行次数
    private int num = 0;
    // 生死牌
    private boolean flag = true;
    @Override
    public void run() {
        while (this.flag){
            System.out.println(Thread.currentThread().getName() + " " + num++);
        }
    }
    public void stop(){
        this.flag = false;
    }
}

public class TestPriorityThread {
    public static void main(String[] args) throws Exception{
        Priority p1 = new Priority();
        Priority p2 = new Priority();
        Thread t1 = new Thread(p1,"线程1");
        Thread t2 = new Thread(p2,"线程2");
        // 线程没有start之前可以查看优先级（默认为5）
        System.out.println(t1.getPriority());

        // 线程优先级一定是在线程启动之前设置的
        // Thread.MAX_PRIORITY = 10
        t1.setPriority(Thread.MAX_PRIORITY);
        // Thread.MIN_PRIORITY = 1
        t2.setPriority(Thread.MIN_PRIORITY);

        t1.start();
        t2.start();

        Thread.sleep(1000);

        p1.stop();
        p2.stop();

    }
}
```

## XI、守护线程

### 1、什么是守护线程

在Java中有两类线程：

- User Thread(用户线程)：就是应用程序里的自定义线程。
- Daemon Thread(守护线程)：比如垃圾回收线程，就是最典型的守护线程。

守护线程（即Daemon Thread），是一个服务线程，准确地来说就是服务其他的线程，这是它的作用，而其他的线程只有一种，那就是用户线程。

守护线程特点：

守护线程会随着用户线程死亡而死亡。

守护线程与用户线程的区别：

用户线程，不随着主线程的死亡而死亡。用户线程只有两种情况会死掉，1在run中异常终止。2正常把run执行完毕，线程死亡。

守护线程，随着用户线程的死亡而死亡，当用户线程死亡守护线程也会随之死亡。

**实时效果反馈**

**1. 如下对守护线程描述错误的是？**

A 守护线程就是辅助线程；

B 守护线程不会随着用户线程死亡而死亡；

C 守护线程会随着用户线程死亡而死亡；

D 在Java多线程中Daemon Thread表示为守护线程；

**答案**

1=>B

### 2、守护线程的使用

```java
/**

 * 守护线程类
   */
   class Daemon implements Runnable{
   @Override
   public void run() {
       for (int i = 0; i < 20; i++) {
           System.out.println(Thread.currentThread().getName() + " " + i);
           try {
               Thread.sleep(2000);
           } catch (InterruptedException e) {
               e.printStackTrace();
           }
       }
   }
   }

class UsersThread implements Runnable{
    @Override
    public void run() {
        Thread t = new Thread(new Daemon(),"Daemon");
        // 将该线程设置为守护线程 ： true:守护线程，     不写或者false：用户线程
        t.setDaemon(true);
        t.start();
        for (int i = 0; i < 5; i++) {
            System.out.println(Thread.currentThread().getName() + " " + i);
            try {
                Thread.sleep(500);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
    }
}

public class TeatDaemonThread {
    public static void main(String[] args) throws Exception{
        Thread t = new Thread(new UsersThread(),"UserThread");
        t.start();
        Thread.sleep(1000);
        System.out.println("主线程结束");
    }
}
```



## XII、线程同步

### 1、什么是线程同步

**线程冲突现象**

![image-20220521153746821](https://www.itbaizhan.com/wiki/imgs/image-20220521153746821-16531186678974.png)

**同步问题的提出**

现实生活中，我们会遇到“同一个资源，多个人都想使用”的问题。 比如：教室里，只有一台电脑，多个人都想使用。天然的解决办法就是，在电脑旁边，大家排队。前一人使用完后，后一人再使用。

**线程同步的概念**

处理多线程问题时，多个线程访问同一个对象，并且某些线程还想修改这个对象。 这时候，我们就需要用到“线程同步”。 线程同步其实就是一种等待机制，多个需要同时访问此对象的线程进入这个对象的等待池形成队列，等待前面的线程使用完毕后，下一个线程再使用。

**实时效果反馈**

**1. 如下对线程同步描述错误的是？**

A 线程同步是为了解决线程冲突问题；

B 线程同步其实就是一种等待机制；

C 线程同步是将并行化变为串行化；

D 线程同步是将串行化变为并行化；

**答案**

1=>D

### 2、实现线程同步

由于同一进程的多个线程共享同一块存储空间，在带来方便的同时，也带来了访问冲突的问题。Java语言提供了专门机制以解决这种冲突，有效避免了同一个数据对象被多个线程同时访问造成的这种问题。这套机制就是synchronized关键字。

**synchronized语法结构：**

synchronized(锁对象){ 　 同步代码  }

**synchronized关键字使用时需要考虑的问题：**

- 需要对那部分的代码在执行时具有线程互斥的能力(线程互斥：并行变串行)。
- 需要对哪些线程中的代码具有互斥能力(通过synchronized锁对象来决定)。



**它包括两种用法：**

synchronized 方法和 synchronized 块。

- synchronized 方法

  通过在方法声明中加入 synchronized关键字来声明，语法如下：

  ```java
   public  synchronized  void accessVal(int newVal);
  ```

  synchronized 在方法声明时使用：放在访问控制符(public)之前或之后。这时同一个对象下synchronized方法在多线程中执行时，该方法是同步的，即一次只能有一个线程进入该方法，其他线程要想在此时调用该方法，只能排队等候，当前线程(就是在synchronized方法内部的线程)执行完该方法后，别的线程才能进入。

- synchronized块

  synchronized 方法的缺陷：若将一个大的方法声明为synchronized 将会大大影响效率。

  Java 为我们提供了更好的解决办法，那就是 synchronized 块。 块可以让我们精确地控制到具体的“成员变量”，缩小同步的范围，提高效率。

**实时效果反馈**

**1. 如下关于synchronized的概念错误的说法是?**

A synchronized是Java中的关键字；

B synchronized是用于实现线程同步的；

C synchronized可以出现在方法上的任何位置；

D synchronized的锁只能是对象类型；

**答案**

1=>C

### 3、修改线程冲突案例演示：

```java
/**
 * 账户类
 */
class Account{
    // 账号
    private String accountNo;
    // 账户余额
    private double balance;

    public Account() {
    }

    public Account(String accountNo, double balance) {
        this.accountNo = accountNo;
        this.balance = balance;
    }

    public String getAccountNo() {
        return accountNo;
    }

    public void setAccountNo(String accountNo) {
        this.accountNo = accountNo;
    }

    public double getBalance() {
        return balance;
    }

    public void setBalance(double balance) {
        this.balance = balance;
    }
}

/**
 * 取款线程
 */
class DrawMoney implements Runnable{
    // 账户对象
    private Account account;
    // 取款金额
    private double drawMoney;

    public DrawMoney(Account account, double drawMoney) {
        this.account = account;
        this.drawMoney = drawMoney;
    }

    @Override
    public void run() {
        synchronized (this.account) {
            // 判断当前账户金额是否大于或等于取款金额
            if (this.account.getBalance() >= this.drawMoney){
                System.out.println(Thread.currentThread().getName() + " 取钱成功，吐出钞票：" + 					 																						this.drawMoney);
                try {
                    Thread.sleep(1000);
                } catch (InterruptedException e) {
                    e.printStackTrace();
                }
                // 更新账户余额
                this.account.setBalance(this.account.getBalance() - this.drawMoney);
                System.out.println("\t余额为：" + this.account.getBalance());
            }else {
                System.out.println(Thread.currentThread().getName() + " 取钱失败，余额不足 ！" );
            }
        }
    }
}


public class TestDrawMoneyThread {
    public static void main(String[] args) {
        Account account = new Account("lisi",1000);
        new Thread(new DrawMoney(account,800),"老公").start();
        new Thread(new DrawMoney(account,800),"老婆").start();
    }
}
```

### 4、线程同步的使用

#### ①、使用this作为线程对象锁

语法结构:

```java
synchronized(this){ 
		 //同步代码 
	}
```

或

```java
public  synchronized  void accessVal(int newVal){

		//同步代码
	
}
```



```java
/**
 * 定义程序员类
 */
class Programmer{
    private String name;

    public Programmer(String name) {
        this.name = name;
    }

    /**
     * 打开电脑
     */
    public void computer(){
        synchronized (this) {
            try {
                System.out.println(this.name + " 接通电源 ");
                Thread.sleep(500);
                System.out.println(this.name + " 按开机按键");
                Thread.sleep(500);
                System.out.println(this.name + " 系统启动中");
                Thread.sleep(500);
                System.out.println(this.name + " 系统启动成功");
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
    }
    /**
     * 编码
     */
    public void coding() {
        synchronized (this) {
            try {
                System.out.println(this.name + " 双击idea ");
                Thread.sleep(500);
                System.out.println(this.name + " idea启动完毕");
                Thread.sleep(500);
                System.out.println(this.name + " 开开心心写代码");
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
    }
}

/**
 * 打开电脑的工作线程
 */
class Working1 extends Thread{
    private Programmer p;
    public Working1(Programmer p){
        this.p = p;
    }
    @Override
    public void run() {
        this.p.computer();
    }
}

/**
 * 编写代码的工作线程
 */
class Working2 extends Thread{
    private Programmer p;
    public Working2(Programmer p){
        this.p = p;
    }
    @Override
    public void run() {
        this.p.coding();
    }
}

public class TestSyncThread {
    public static void main(String[] args) {
        Programmer p = new Programmer("itshihao");
        new Working1(p).start();
        new Working2(p).start();
    }
}

```

#### ②、使用字符串作为线程对象锁

​	**不同对象之间的线程同步**

```java
/**
 * 定义程序员类
 */
class Programmer1{
    private String name;

    public Programmer1(String name) {
        this.name = name;
    }
    /**
     * 去卫生间
     */
    public void wc(){
        synchronized ("随便啦") {
            try {
                System.out.println( this.name + "打开卫生间门");
                Thread.sleep(500);
                System.out.println( this.name + "开始排泄");
                Thread.sleep(500);
                System.out.println( this.name + "冲水");
                Thread.sleep(500);
                System.out.println( this.name + "离开卫生间");
                Thread.sleep(500);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
    }

}

/**
 * 去卫生间的线程
 */
class WC extends Thread{
    private Programmer1 p;
    public  WC(Programmer1 p){
        this.p = p;
    }
    @Override
    public void run() {
        this.p.wc();
    }
}



public class TestStringSyncThread {
    public static void main(String[] args) {
        Programmer1 p = new Programmer1("张三");
        Programmer1 p1 = new Programmer1("李四");
        Programmer1 p2 = new Programmer1("王五");
        new WC(p).start();
        new WC(p1).start();
        new WC(p2).start();

    }
}
```

#### ③、使用Class作为线程对象锁

![image-20220522110203012](https://www.itbaizhan.com/wiki/imgs/image-20220522110203012-16531885239836.png)

语法结构：

```java
synchronized(XX.class){ 
	 //同步代码 
	 }
```

或

```java
synchronized public static void accessVal()
```

**不同部门员工领取奖金案例**：

```java
/**
 * 定义销售员工类
 */
class sale{
    private String name;

    public sale(String name) {
        this.name = name;
    }

    public void money(){
        synchronized (sale.class) {
            try {
                System.out.println( this.name + "被领导表扬");
                Thread.sleep(500);
                System.out.println( this.name + "拿钱");
                Thread.sleep(500);
                System.out.println( this.name + "对公司表示感谢");
                Thread.sleep(500);
                System.out.println( this.name + "开开心心的拿钱走人");
                Thread.sleep(500);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
    }
}


/**
 * 定义程序员类
 */
class Programmer2{
    private String name;

    public Programmer2(String name) {
        this.name = name;
    }
    /**
     * 领取奖金
     */
    public void money(){
        synchronized (Programmer2.class) {
            try {
                System.out.println( this.name + "被领导表扬");
                Thread.sleep(500);
                System.out.println( this.name + "拿钱");
                Thread.sleep(500);
                System.out.println( this.name + "对公司表示感谢");
                Thread.sleep(500);
                System.out.println( this.name + "开开心心的拿钱走人");
                Thread.sleep(500);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
    }

}

/**
 * 程序员领取奖金的线程
 */
class ProgrammerMoney extends Thread{
    private Programmer2 p;
    public  ProgrammerMoney(Programmer2 p){
        this.p = p;
    }
    @Override
    public void run() {
        this.p.money();
    }
}

/**
 * 销售员工领取奖金的线程
 */
class SaleMoney extends Thread{
    private sale s;
    public  SaleMoney(sale p){
        this.s = p;
    }
    @Override
    public void run() {
        this.s.money();
    }
}


public class TestSyncClassThread {
    public static void main(String[] args) {
        Programmer2 p = new Programmer2("张三");
        Programmer2 p1 = new Programmer2("李四");
        Programmer2 p2 = new Programmer2("王五");
        new ProgrammerMoney(p).start();
        new ProgrammerMoney(p1).start();
        new ProgrammerMoney(p2).start();

        sale s = new sale("张晓丽");
        sale s1 = new sale("王宇");
        sale s2 = new sale("王健林");
        new SaleMoney(s).start();
        new SaleMoney(s1).start();
        new SaleMoney(s2).start();
    }
}

```

#### ④、使用自定义对象作为线程对象锁

![image-20220522110136128](https://www.itbaizhan.com/wiki/imgs/image-20220522110136128-16531884975925.png)

语法结构：

```java
synchronized(自定义对象){ 
　　    //同步代码 
}

```

自定义对象案例：

```java
/**
 * 定义经理类
 */
class Manager{
    private String name;

    public Manager(String name) {
        this.name = name;
    }

    public String getName() {
        return this.name;
    }
    /**
     * 敬酒
     */
    public void cheers(String mName, String eName){
        try {
            System.out.println(mName + "来到" + eName + "面前");
            Thread.sleep(500);
            System.out.println(eName + "拿起酒杯");
            Thread.sleep(500);
            System.out.println(mName + "和" + eName + "干杯");
        }catch (Exception e){
            e.printStackTrace();
        }
    }
}

/**
 * 敬酒线程类
 */
class CheersThread extends Thread{
    private Manager manager;
    private String name;
    public CheersThread(String name,Manager manager){
        this.name = name;
        this.manager = manager;
    }
    @Override
    public void run() {
        synchronized (this.manager) {
            this.manager.cheers(this.manager.getName(),name);
        }
    }
}




public class TestSyncSelfClassThread {
    public static void main(String[] args) {
        Manager manager = new Manager("张三丰");
        new CheersThread("张三",manager).start();
        new CheersThread("李四",manager).start();
    }
}
```

### 5、**死锁及解决方案**

#### ①、死锁的概念

![image-20220522201430621](https://www.itbaizhan.com/wiki/imgs/image-20220522201430621-16532216717493.png)

“死锁”指的是：

多个线程各自占有一些共享资源，并且互相等待其他线程占有的资源才能进行，而导致两个或者多个线程都在等待对方释放资源，都停止执行的情形。

> **某一个同步块需要同时拥有“两个以上对象的锁”时，就可能会发生“死锁”的问题。比如，“化妆线程”需要同时拥有“镜子对象”、“口红对象”才能运行同步块。那么，实际运行时，“小丫的化妆线程”拥有了“镜子对象”，“大丫的化妆线程”拥有了“口红对象”，都在互相等待对方释放资源，才能化妆。这样，两个线程就形成了互相等待，无法继续运行的“死锁状态”。**



#### ②、死锁案例演示

```java
/**
 * 口红类
 */
class Lipstick{

}

/**
 * 镜子类
 */
class Mirror{

}

/**
 * 化妆线程类
 */
class Makeup extends Thread{
    private int flag; // flag = 0:拿着口红    flag != 0：拿着镜子
    private String girlName;
    static Lipstick lipstick = new Lipstick();
    static Mirror mirror = new Mirror();

    public Makeup(int flag,String girlName){
        this.flag = flag;
        this.girlName = girlName;
    }
    @Override
    public void run() {
        this.doMakeup();
    }

    /**
     * 开始化妆
     */
    public void doMakeup(){
        if (flag == 0){
            synchronized (lipstick){
                System.out.println(this.girlName + "拿着口红");
                try {
                    Thread.sleep(1000);
                } catch (InterruptedException e) {
                    e.printStackTrace();
                }
                synchronized (mirror){
                    System.out.println(this.girlName  + "拿着镜子！");
                }
            }
        }else {
            synchronized (mirror){
                System.out.println(this.girlName + "拿着镜子");
                try {
                    Thread.sleep(2000);
                } catch (InterruptedException e) {
                    e.printStackTrace();
                }
                synchronized (lipstick){
                    System.out.println(this.girlName + "拿着口红");
                }
            }
        }
    }
}

public class DeadLockThread {
    public static void main(String[] args) {
        new Makeup(0,"小丫").start();
        new Makeup(1,"大丫").start();
    }
}
```

#### ③、死锁问题的解决

~~ 死锁是由于 “同步块需要同时持有多个对象锁造成”的，

~~ 要解决这个问题，思路很简单，

~~ 就是：同一个代码块，不要同时持有两个对象锁。

```java
public void doMakeup(){
        if (flag == 0){
            synchronized (lipstick){
                System.out.println(this.girlName + "拿着口红");
                try {
                    Thread.sleep(1000);
                } catch (InterruptedException e) {
                    e.printStackTrace();
                }
            }
            synchronized (mirror){
                System.out.println(this.girlName  + "拿着镜子！");
            }
        }else {
            synchronized (mirror){
                System.out.println(this.girlName + "拿着镜子");
                try {
                    Thread.sleep(2000);
                } catch (InterruptedException e) {
                    e.printStackTrace();
                }
            }
            synchronized (lipstick){
                System.out.println(this.girlName + "拿着口红");
            }
        }
    }
```

## XIII、线程并发协作(生产者/消费者模式)

![image-20220524144814064](https://www.itbaizhan.com/wiki/imgs/image-20220524144814064-16533748950163.png)

多线程环境下，我们经常需要多个线程的并发和协作。这个时候，就需要了解一个重要的多线程并发协作模型“生产者/消费者模式”。

### 1、角色介绍

- **什么是生产者？**

  生产者指的是负责生产数据的模块（这里模块可能是：方法、对象、线程、进程）。

- **什么是消费者？**

  消费者指的是负责处理数据的模块（这里模块可能是：方法、对象、线程、进程）。

- **什么是缓冲区？**

  消费者不能直接使用生产者的数据，它们之间有个“缓冲区”。生产者将生产好的数据放入“缓冲区”，消费者从“缓冲区”拿要处理的数据。

缓冲区是实现并发的核心，缓冲区的设置有两个好处：

1. 实现线程的并发协作

   有了缓冲区以后，生产者线程只需要往缓冲区里面放置数据，而不需要管消费者消费的情况；同样，消费者只需要从缓冲区拿数据处理即可，也不需要管生产者生产的情况。 这样，就从逻辑上实现了“生产者线程”和“消费者线程”的分离，解除了生产者与消费者之间的耦合。

2. 解决忙闲不均，提高效率

   生产者生产数据慢时，缓冲区仍有数据，不影响消费者消费；消费者处理数据慢时，生产者仍然可以继续往缓冲区里面放置数据 。



### 2、创建生产者消费者线程

```java
/**
 * 馒头类
 */
class Mantou{
    private int id;

    public Mantou(int id) {
        this.id = id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public int getId() {
        return this.id;
    }
}

/**
 * 定义缓冲区类
 */
class SyncStack{
    // 定义存放馒头的盒子
    private Mantou[] mt = new Mantou[10];
    // 定义操作盒子的索引
    private int index;

    /**
     * 放馒头
     */
    public synchronized void push(Mantou mantou){
        // 判断盒子是否已满
        while (this.index == mt.length){
            try {
                /**
                 * 语法： wait()方法必须要在synchronized块中调用。
                 * wait执行后，线程会将持有的对象锁释放，并进入阻塞状态
                 * 其他需要该对象锁的线程就可以运行了
                 */
                this.wait();
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
        // 唤醒取馒头的线程
        /**
         *  语法： notify()方法必须要在synchronized块中调用。
         *  该方法会唤醒处于等待状态队列中的一个线程
         */
        this.notify();
        this.mt[this.index] = mantou;
        this.index++;
    }

    /**
     *取馒头
     */
    public synchronized Mantou pop(){
        while (this.index == 0){
            try {
                /**
                 * 语法： wait()方法必须要在synchronized块中调用。
                 * wait执行后，线程会将持有的对象锁释放，并进入阻塞状态
                 * 其他需要该对象锁的线程就可以运行了
                 */
                this.wait();
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
        this.notify();
        this.index--;
        return this.mt[this.index];
    }
}

/**
 * 定义生产者线程类
 */
class ShengChan extends Thread{
    private SyncStack ss;
    public ShengChan(SyncStack ss){
        this.ss = ss;
    }
    @Override
    public void run() {
        for (int i = 0; i < 10; i++){
            Mantou mt = new Mantou(i);
            mt.setId(i);
            System.out.println("生产馒头：" + mt.getId());
            this.ss.push(mt);
        }
    }
}

/**
 * 定义消费者线程类
 */
class XiaoFei extends Thread{
    private SyncStack ss;
    public XiaoFei(SyncStack ss){
        this.ss = ss;
    }
    @Override
    public void run() {
        for (int i = 0; i < 10; i++){
            Mantou mt = this.ss.pop();
            System.out.println("消费馒头：" + mt.getId());
        }
    }
}


public class ProduceThread {
    public static void main(String[] args) {
        SyncStack ss = new SyncStack();
        new ShengChan(ss).start();
        new XiaoFei(ss).start();
    }
}
```

### 3、线程并发协作总结

线程并发协作（也叫线程通信）

生产者消费者模式：

1. 生产者和消费者共享同一个资源，并且生产者和消费者之间相互依赖，互为条件。

2. 对于生产者，没有生产产品之前，消费者要进入等待状态。而生产了产品之后，又需要马上通知消费者消费。

3. 对于消费者，在消费之后，要通知生产者已经消费结束，需要继续生产新产品以供消费。

4. 在生产者消费者问题中，仅有synchronized是不够的。synchronized可阻止并发更新同一个共享资源，实现了同步但是synchronized不能用来实现不同线程之间的消息传递（通信）。

5. 那线程是通过哪些方法来进行消息传递（通信）的呢？见如下总结：

   | **方法名**                              | **作 用**                                                    |
   | --------------------------------------- | ------------------------------------------------------------ |
   | final void wait()                       | 表示线程一直等待，直到得到其它线程通知                       |
   | void wait(long timeout)                 | 线程等待指定毫秒参数的时间                                   |
   | final void wait(long timeout,int nanos) | 线程等待指定毫秒、微秒的时间                                 |
   | final void notify()                     | 唤醒一个处于等待状态的线程                                   |
   | final void notifyAll()                  | 唤醒同一个对象上所有调用wait()方法的线程，优先级别高的线程优先运行 |

6. 以上方法均是java.lang.Object类的方法；

都只能在同步方法或者同步代码块中使用，否则会抛出异常。



> **OldLu建议**
>
> 在实际开发中，尤其是“架构设计”中，会大量使用这个模式。 对于初学者了解即可，如果晋升到中高级开发人员，这就是必须掌握的内容。

#  四、网络编程

## 〇、网络编程基本概念

![image-20220525143833935](https://www.itbaizhan.com/wiki/imgs/image-20220525143833935-16534607155931.png)

### 1、计算机网络

计算机网络是指将地理位置不同的具有独立功能的多台计算机及其外部设备，通过通信线路连接起来，在网络操作系统，网络管理软件及网络通信协议的管理和协调下，实现资源共享和信息传递的计算机系统。

从其中我们可以提取到以下内容：

1. 计算机网络的作用：资源共享和信息传递。
2. 计算机网络的组成：
   - 计算机硬件：计算机（大中小型服务器，台式机、笔记本等）、外部设备（路由器、交换机等）、通信线路（双绞线、光纤等）。             
   - 计算机软件：网络操作系统（Windows 2000 Server/Advance Server、Unix、Linux等）、网络管理软件（WorkWin、SugarNMS等）、网络通信协议（如TCP/IP协议栈等）。

**实时效果反馈**

**1**.**如下哪个选项不是计算机网络中的组成部分？**

A  计算机设备、网络设备、通信线路；

B  网络操作系统、网络管理软件；

C  网络通信协议；

D  聊天软件；

**答案**

1=>D

### 2、网络通信协议

![image-20211209112048423](https://www.itbaizhan.com/wiki/imgs/image-20211209112048423.png)

**什么是网络通信协议**

通过计算机网络可以实现不同计算机之间的连接与通信，但是计算机网络中实现通信必须有一些约定即通信协议，对速率、传输代码、代码结构、传输控制步骤、出错控制等制定标准。

国际标准化组织(ISO，即International Organization for Standardization)定义了网络通信协议的基本框架，被称为OSI（Open System Interconnect，即开放系统互联）模型。要制定通讯规则，内容会很多，比如要考虑A电脑如何找到B电脑，A电脑在发送信息给B电脑时是否需要B电脑进行反馈，A电脑传送给B电脑的数据格式又是怎样的？内容太多太杂，所以OSI模型将这些通讯标准进行层次划分，每一层次解决一个类别的问题，这样就使得标准的制定没那么复杂。OSI模型制定的七层标准模型，分别是：应用层，表示层，会话层，传输层，网络层，数据链路层，物理层。

OSI七层协议模型：

![image-20220525145914759](https://www.itbaizhan.com/wiki/imgs/image-20220525145914759-16534619556872.png)

**网络协议的分层**

虽然国际标准化组织制定了这样一个网络通信协议的模型，但是实际上互联网通讯使用最多的网络通信协议是TCP/IP网络通信协议。

TCP/IP 模型，也是按照层次划分，共四层：应用层，传输层，网络层，网络接口层（物理+数据链路层）。

OSI模型与TCP/IP模型的对应关系：

![image-20220525151808274](https://www.itbaizhan.com/wiki/imgs/image-20220525151808274-16534630893075.png)

**实时效果反馈**

**1**.**如下哪个选项不是TCP/IP 模型中的分层**。

A 应用层；

B 传输层；

C 网络层；

D 物理层；

**答案**

1=>D

### 3、数据封装与解封

![image-20220526091048716](https://www.itbaizhan.com/wiki/imgs/image-20220526091048716-16535274498671.png)

数据封装（Data Encapsulation）是指将协议数据单元（PDU）封装在一组协议头和协议尾中的过程。在OSI七层参考模型中，每层主要负责与其它机器上的对等层进行通信。该过程是在协议数据单元（PDU）中实现的，其中每层的PDU一般由本层的协议头、协议尾和数据封装构成。

- 数据发送处理过程
  1. 应用层将数据交给传输层，传输层添加上TCP的控制信息（称为TCP头部），这个数据单元称为段（Segment），加入控制信息的过程称为封装。然后，将段交给网络层。
  2. 网络层接收到段，再添加上IP头部，这个数据单元称为包（Packet）。然后，将包交给数据链路层。
  3. 数据链路层接收到包，再添加上MAC头部和尾部，这个数据单元称为帧（Frame）。然后，将帧交给物理层。
  4. 物理层将接收到的数据转化为比特流，然后在网线中传送。



- 数据接收处理过程
  1. 物理层接收到比特流，经过处理后将数据交给数据链路层。
  2. 数据链路层将接收到的数据转化为数据帧，再除去MAC头部和尾部，这个除去控制信息的过程称为解封，然后将包交给网络层。
  3. 网络层接收到包，再除去IP头部，然后将段交给传输层。
  4. 传输层接收到段，再除去TCP头部，然后将数据交给应用层。



从以上传输过程中，可以总结出以下规则：

1. 发送方数据处理的方式是从高层到底层，逐层进行数据封装。
2. 接收方数据处理的方式是从底层到高层，逐层进行数据解封。



接收方的每一层只把对该层有意义的数据拿走，或者说每一层只能处理发送方同等层的数据，然后把其余的部分传递给上一层，这就是对等层通信的概念。



数据封装与解封：

数据封装

![image-20220525160043418](https://www.itbaizhan.com/wiki/imgs/image-20220525160043418-16534656444636.png)

数据解封

![image-20220525160104765](https://www.itbaizhan.com/wiki/imgs/image-20220525160104765-16534656657938.png)

**实时效果反馈**

**1**.**在网络通信中，对数据封装步骤描述错误的是？**

A 应用层将数据交给传输层；

B 传输层将数据交给网络链路层；

C 网络链路层将数据交给物理层；

D 物理层将数据交给网络链路层；

**答案**

1=>D

### 4、 IP地址

![image-20211209110317010](https://www.itbaizhan.com/wiki/imgs/image-20211209110317010.png)

**IP地址**

IP是Internet Protocol Address，即"互联网协议地址"。

用来标识网络中的一个通信实体的地址。通信实体可以是计算机、路由器等。 比如互联网的每个服务器都要有自己的IP地址，而每个局域网的计算机要通信也要配置IP地址。

路由器是连接两个或多个网络的网络设备。

IP地址分类：

| 类别 | 最大网络数    | IP地址范围                | 单个网段最大主机数 | 私有IP地址范围              |
| ---- | ------------- | ------------------------- | ------------------ | --------------------------- |
| A    | 126(2^7-2)    | 1.0.0.1-127.255.255.254   | 16777214           | 10.0.0.0-10.255.255.255     |
| B    | 16384(2^14)   | 128.0.0.1-191.255.255.254 | 65534              | 172.16.0.0-172.31.255.255   |
| C    | 2097152(2^21) | 192.0.0.1-223.255.255.254 | 254                | 192.168.0.0-192.168.255.255 |

目前主流使用的IP地址是IPV4，但是随着网络规模的不断扩大，IPV4面临着枯竭的危险，所以推出了IPV6。

![image-20211209124041972](https://www.itbaizhan.com/wiki/imgs/image-20211209124041972.png)

> IPV4，采用32位地址长度，只有大约43亿个地址，它只有4段数字，每一段最大不超过255。随着互联网的发展，IP地址不够用了，在2019年11月25日IPv4位地址分配完毕。
>
> IPv6采用128位地址长度，几乎可以不受限制地提供地址。按保守方法估算IPv6实际可分配的地址，整个地球的每平方米面积上仍可分配1000多个地址。

IP地址实际上是一个32位整数（称为IPv4），以字符串表示的IP地址如`192.168.0.1`实际上是把32位整数按8位分组后的数字表示，目的是便于阅读。

IPv6地址实际上是一个128位整数，它是目前使用的IPv4的升级版，以字符串表示类似于`2001:0db8:85a3:0042:1000:8a2e:0370:7334`

**公有地址**

公有地址（Public address）由Inter NIC（Internet Network Information Center互联网信息中心）负责。这些IP地址分配给注册并向Inter NIC提出申请的组织机构。通过它直接访问互联网。

**私有地址**

私有地址（Private address）属于非注册地址，专门为组织机构内部使用。

以下列出留用的内部私有地址

A类 10.0.0.0--10.255.255.255

B类 172.16.0.0--172.31.255.255

C类 192.168.0.0--192.168.255.255

> **注意事项**
>
> - 127.0.0.1 本机地址
> - 192.168.0.0--192.168.255.255为私有地址，属于非注册地址，专门为组织机构内部使用

**实时效果反馈**

**1**.**如下关于IP的说法，错误的是**。

A IP用来识别计算机通信地址的。

B 192.168.0.0--192.168.255.255为私有地址，专门为组织机构内部使用

C 127.0.0.1 本机地址。

D IP用来识别计算机中进行通信的不同应用程序。

**答案**

1=>D

###  5、端口port

端口号用来识别计算机中进行通信的应用程序。因此，它也被称为程序地址。

一台计算机上同时可以运行多个程序。传输层协议正是利用这些端口号识别本机中正在进行通信的应用程序，并准确地进行数据传输。

![image-20211209151558070](https://www.itbaizhan.com/wiki/imgs/image-20211209151558070.png)

> **总结**
>
> - IP地址好比每个人的地址（门牌号），端口好比是房间号。必须同时指定IP地址和端口号才能够正确的发送数据。
> - IP地址好比为电话号码，而端口号就好比为分机号。

**端口分配**

端口是虚拟的概念，并不是说在主机上真的有若干个端口。通过端口，可以在一个主机上运行多个网络应用程序。 端口的表示是一个16位的二进制整数，对应十进制的0-65535。

操作系统中一共提供了0~65535可用端口范围。

按端口号分类：

**公认端口（Well Known Ports）：**从0到1023，它们紧密绑定（binding）于一些服务。通常这些端口的通讯明确表明了某种服务的协议。例如：80端口实际上总是HTTP通讯。

**注册端口（Registered Ports）：**从1024到65535。它们松散地绑定于一些服务。也就是说有许多服务绑定于这些端口，这些端口同样用于许多其它目的。例如：许多系统处理动态端口从1024左右开始。

**实时效果反馈**

**1**.**如下关于端口的说法，正确的是？**

A 端口号用来识别计算机通信地址的。

B 端口号用来识别计算机中进行通信的不同应用程序。

C 端口号用来识别计算机中网卡。

D 端口号用来识别路由器。

**答案**

1=>B

### 6、 URL

![image-20220526104732940](https://www.itbaizhan.com/wiki/imgs/image-20220526104732940-16535332539833.png)

URL作用：

URL（Uniform Resource Locator），是互联网的统一资源定位符。用于识别互联网中的信息资源。通过URL我们可以访问文件、数据库、图像、新闻等。

在互联网上，每一信息资源都有统一且唯一的地址，该地址就叫URL，URL由4部分组成：协议 、存放资源的主机域名、资源文件名和端口号。如果未指定该端口号，则使用协议默认的端口。例如http 协议的默认端口为 80。 在浏览器中访问网页时，地址栏显示的地址就是URL。

在java.net包中提供了URL类，该类封装了大量复杂的涉及从远程站点获取信息的细节。

**实时效果反馈**

**1**.**如下关于URL说法，错误的是？**

A URL全称为统一资源定位符；

B URL由4部分组成；

C URL用来识别计算机中网卡。

D 在java.net包中提供了对URL操作的类。

**答案**

1=>C

###  7、Socket

![image-20220526110904374](https://www.itbaizhan.com/wiki/imgs/image-20220526110904374-16535345457944.png)

我们开发的网络应用程序位于应用层，TCP和UDP属于传输层协议，在应用层如何使用传输层的服务呢？在应用层和传输层之间，则是使用套接字Socket来进行分离。

套接字就像是传输层为应用层开的一个小口，应用程序通过这个小口向远程发送数据，或者接收远程发来的数据；而这个小口以内，也就是数据进入这个口之后，或者数据从这个口出来之前，是不知道也不需要知道的，也不会关心它如何传输，这属于网络其它层次工作。

Socket实际是传输层供给应用层的编程接口。Socket就是应用层与传输层之间的桥梁。使用Socket编程可以开发客户机和服务器应用程序，可以在本地网络上进行通信，也可通过Internet在全球范围内通信。

**实时效果反馈**

**1**.**如下关于Socket说法，错误的是？**

A Socket是网络层供给传输层的编程接口；

B Socket是传输层供给应用层的编程接口；

C 使用Socket编程可以开发客户机和服务器应用程序；

D Socket应用层与传输层之间的桥梁；

**答案**

1=>A

### 8、TCP协议和UDP协议

**TCP协议**

TCP（Transmission Control Protocol，传输控制协议）。TCP方式就类似于拨打电话，使用该种方式进行网络通讯时，需要建立专门的虚拟连接，然后进行可靠的数据传输，如果数据发送失败，则客户端会自动重发该数据。

![img](https://www.itbaizhan.com/wiki/imgs/TCP%E7%9A%84%E4%B8%89%E6%AC%A1%E6%8F%A1%E6%89%8B.gif)

**TCP在建立连接时又分三步走：**

n 第一步，是请求端（客户端）发送一个包含SYN即同步（Synchronize）标志的TCP报文，SYN同步报文会指明客户端使用的端口以及TCP连接的初始序号。

n 第二步，服务器在收到客户端的SYN报文后，将返回一个SYN+ACK的报文，表示客户端的请求被接受，同时TCP序号被加一，ACK即确认（Acknowledgement）。

n 第三步，客户端也返回一个确认报文ACK给服务器端，同样TCP序列号被加一，到此一个TCP连接完成。然后才开始通信的第二步：数据处理。

n 这就是所说的TCP的三次握手（Three-way Handshake）。

**UDP协议**

UDP（User Data Protocol，用户数据报协议）

UDP是一个非连接的协议，传输数据之前源端和终端不建立连接， 当它想传送时就简单地去抓取来自应用程序的数据，并尽可能快地把它扔到网络上。 在发送端，UDP传送数据的速度仅仅是受应用程序生成数据的速度、 计算机的能力和传输带宽的限制； 在接收端，UDP把每个消息段放在队列中，应用程序每次从队列中读一个消息段。

UDP方式就类似于发送短信，使用这种方式进行网络通讯时，不需要建立专门的虚拟连接，传输也不是很可靠，如果发送失败则客户端无法获得。

UDP 因为没有拥塞控制，一直会以恒定的速度发送数据。即使网络条件不好，也不会对发送速率进行调整。这样实现的弊端就是在网络条件不好的情况下可能会导致丢包，但是优点也很明显，在某些实时性要求高的场景（比如电话会议）就需要使用 UDP 而不是 TCP

![img](https://www.itbaizhan.com/wiki/imgs/UDP%E5%8F%91%E9%80%81%E6%A8%A1%E5%BC%8F.gif)

### 9、TCP和UDP区别

这两种传输方式都在实际的网络编程中使用，重要的数据一般使用TCP方式进行数据传输，而大量的非核心数据则可以通过UDP方式进行传递，在一些程序中甚至结合使用这两种方式进行数据传递。

由于TCP需要建立专用的虚拟连接以及确认传输是否正确，所以使用TCP方式的速度稍微慢一些，而且传输时产生的数据量要比UDP稍微大一些。

|              | UDP                                        | TCP                                    |
| :----------- | :----------------------------------------- | -------------------------------------- |
| 是否连接     | 无连接                                     | 面向连接                               |
| 是否可靠     | 不可靠传输，不使用流量控制和拥塞控制       | 可靠传输，使用流量控制和拥塞控制       |
| 连接对象个数 | 支持一对一，一对多，多对一和多对多交互通信 | 只能是一对一通信                       |
| 传输方式     | 面向报文                                   | 面向字节流                             |
| 首部开销     | 首部开销小，仅8字节                        | 首部最小20字节，最大60字节             |
| 适用场景     | 适用于实时应用（IP电话、视频会议、直播等） | 适用于要求可靠传输的应用，例如文件传输 |

> **总结**
>
> - TCP是面向连接的，传输数据安全，稳定，效率相对较低。
> - UDP是面向无连接的，传输数据不安全，效率较高。

**实时效果反馈**

**1**.**如下关于TCP和UDP协议，说法错误的是**。

A TCP是面向连接的，传输数据安全，稳定，效率相对较低

B UDP是面向无连接的，传输数据不安全，效率较高。

C UDP适用于实时应用（IP电话、视频会议、直播等）

D UDP适用于要求可靠传输的应用，例如文件传输

**答案**

1=>D

## I、 Java网络编程中的常用类

Java为了跨平台，在网络应用通信时是不允许直接调用操作系统接口的，而是由java.net包来提供网络功能。下面我们来介绍几个java.net包中的常用的类。

### 1、InetAddress的使用

作用：封装计算机的IP地址和DNS（没有端口信息）

> 注：DNS是Domain Name System，域名系统。

> **特点：**
>
> 这个类没有构造方法。如果要得到对象，只能通过静态方法：getLocalHost()、getByName()、 getAllByName()、 getAddress()、getHostName()

**获取本机信息**

获取本机信息需要使用getLocalHost方法创建InetAddress对象。getLocalHost()方法返回一个InetAddress对象，这个对象包含了本机的IP地址，计算机名等信息。

```java
import java.net.InetAddress;

public class TestInet {
    public static void main(String[] args) throws Exception{
        // 实例化InetAddress对象
        InetAddress inetAddress = InetAddress.getLocalHost();
        // 返回当前计算机的Ip地址
        System.out.println(inetAddress.getHostAddress());
        // 返回计算机名
        System.out.println(inetAddress.getHostName());
    }
}
```

### 2、根据域名获取计算机的信息

根据域名获取计算机信息时需要使用getByName(“域名”)方法创建InetAddress对象。

```java
import java.net.InetAddress;

public class TestInet2 {
    public static void main(String[] args) throws Exception{
        // 创建根据域名获取计算机信息的InetAddress对象
        InetAddress inetAddress = InetAddress.getByName("www.baidu.com");
        // 返回Ip地址
        System.out.println(inetAddress.getHostAddress());
        // 返回计算机名
        System.out.println(inetAddress.getHostName());
    }
}
```

### 3、根据IP获取计算机的信息

根据IP地址获取计算机信息时需要使用getByName(“IP”)方法创建InetAddress对象。

```java
import java.net.InetAddress;

public class TestInet3 {
    public static void main(String[] args) throws Exception{
        // 创建根据Ip地址获取计算机信息的InetAddress对象
        InetAddress inetAddress = InetAddress.getByName("192.168.10.21");

        // 返回Ip地址
        System.out.println(inetAddress.getHostAddress());
        // 返回计算机名
        System.out.println(inetAddress.getHostName());
    }
}
```

### 4、InetSocketAddress的使用

**作用：**包含IP和端口信息，常用于Socket通信。此类实现 IP 套接字地址（IP 地址 + 端口号），不依赖任何协议。

InetSocketAddress相比较InetAddress多了一个端口号，端口的作用：一台拥有IP地址的主机可以提供许多服务，比如Web服务、FTP服务、SMTP服务等，这些服务完全可以通过1个IP地址来实现。

那么，主机是怎样区分不同的网络服务呢？显然不能只靠IP地址，因为IP 地址与网络服务的关系是一对多的关系。实际上是通过“IP地址+端口号”来区分不同的服务的。

```java
import java.net.InetSocketAddress;

public class TestInetSocket {
    public static void main(String[] args) {
        // 创建InetSocketAddress对象
        InetSocketAddress inetSocketAddress = new InetSocketAddress("www.baidu.com",80);

        // 返回IP地址
        System.out.println(inetSocketAddress.getAddress().getHostAddress());
        // 返回计算机名
        System.out.println(inetSocketAddress.getHostName());
    }
}
```

### 5、URL的使用

IP地址标识了Internet上唯一的计算机，而URL则标识了这些计算机上的资源。 URL 代表一个统一资源定位符，它是指向互联网“资源”的指针。资源可以是简单的文件或目录，也可以是对更为复杂的对象的引用，例如对数据库或搜索引擎的查询。

为了方便程序员编程，JDK中提供了URL类，该类的全名是java.net.URL，有了这样一个类，就可以使用它的各种方法来对URL对象进行分割、合并等处理。

```java
import java.net.URL;

public class TestUrl {
    public static void main(String[] args) throws Exception{
        // 创建URL对象
        URL url = new URL("https://www.itbaizhan.com/search.html?kw=dsg");

        System.out.println("获取与此URL相关协议的默认端口：" + url.getDefaultPort());
        System.out.println("访问资源：" + url.getFile());
        System.out.println("主机名：" + url.getHost());
        System.out.println("访问资源的路径：" + url.getPath());
        System.out.println("协议：" + url.getProtocol());
        System.out.println("参数部分：" + url.getQuery());
    }
}
```

### 6、通过URL实现最简单的网络爬虫

```java
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.net.URL;

public class TestUrl2 {
    public static void main(String[] args) throws Exception{
        URL url = new URL("https://www.itbaizhan.com/");
        try (BufferedReader br = new BufferedReader(new InputStreamReader(url.openStream()))){
            StringBuilder sb = new StringBuilder();
            String temp = "";
            while ((temp = br.readLine()) != null){
                sb.append(temp + "\r\n");
            }
            System.out.println(sb);
        }catch (Exception e){
            e.printStackTrace();
        }
    }
}

```

## II、TCP通信的实现和项目案例

### 1、TCP通信实现原理

前边我们提到TCP协议是面向的连接的，在通信时客户端与服务器端必须建立连接。在网络通讯中，第一次主动发起通讯的程序被称作客户端(Client)程序，简称客户端，而在第一次通讯中等待连接的程序被称作服务器端(Server)程序，简称服务器。一旦通讯建立，则客户端和服务器端完全一样，没有本质的区别。



**“请求-响应”模式：**

- Socket类：发送TCP消息。
- ServerSocket类：创建服务器。



套接字Socket是一种进程间的数据交换机制。这些进程既可以在同一机器上，也可以在通过网络连接的不同机器上。换句话说，套接字起到通信端点的作用。单个套接字是一个端点，而一对套接字则构成一个双向通信信道，使非关联进程可以在本地或通过网络进行数据交换。一旦建立套接字连接，数据即可在相同或不同的系统中双向或单向发送，直到其中一个端点关闭连接。套接字与主机地址和端口地址相关联。主机地址就是客户端或服务器程序所在的主机的IP地址。端口地址是指客户端或服务器程序使用的主机的通信端口。

在客户端和服务器中，分别创建独立的Socket，并通过Socket的属性，将两个Socket进行连接，这样，客户端和服务器通过套接字所建立的连接使用输入输出流进行通信。

TCP/IP套接字是最可靠的双向流协议，使用TCP/IP可以发送任意数量的数据。

实际上，套接字只是计算机上已编号的端口。如果发送方和接收方计算机确定好端口，他们就可以通信了。

客户端与服务器端的通信关系图：

![image-20220526163838394](https://www.itbaizhan.com/wiki/imgs/image-20220526163838394-16535543194605.png)



**TCP/IP通信连接的简单过程：**

位于A计算机上的TCP/IP软件向B计算机发送包含端口号的消息，B计算机的TCP/IP软件接收该消息，并进行检查，查看是否有它知道的程序正在该端口上接收消息。如果有，他就将该消息交给这个程序。

要使程序有效地运行，就必须有一个客户端和一个服务器。



**通过Socket的编程顺序：**

1. 创建服务器ServerSocket，在创建时，定义ServerSocket的监听端口（在这个端口接收客户端发来的消息）
2. ServerSocket调用accept()方法，使之处于阻塞状态。
3. 创建客户端Socket，并设置服务器的IP及端口。
4. 客户端发出连接请求，建立连接。
5. 分别取得服务器和客户端Socket的InputStream和OutputStream。
6. 利用Socket和ServerSocket进行数据传输。
7. 关闭流及Socket。

**实时效果反馈**

**1**.**如下对TCP连接模式描述正确的是？**

A 基于请求模式；

B 基于响应模式；

C 基于请求与响应模式；

D 基于广播模式；

**答案**

1=>C

### 2、 TCP通信入门案例

#### ①、创建服务端

```java
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.net.ServerSocket;
import java.net.Socket;

public class BasicSocketServer {
    public static void main(String[] args) {
        System.out.println("服务端已启动，等待监听........");
        try (ServerSocket serverSocket = new ServerSocket(8888);
             // 监听8888端口，此时当前线程会处于阻塞状态
             Socket socket = serverSocket.accept();
             // 连接成功后会得到与客户端对应的Socket对象，并解除线程阻塞
             // 通过客户端对应的Socket对象中的输入流对象，获取客户端发送过来的消息
             BufferedReader br = new BufferedReader(new InputStreamReader(socket.getInputStream()));
        ){
            System.out.println(br.readLine());

        }catch (Exception e){
            e.printStackTrace();
            System.out.println("服务器启动失败！");
        }
    }
}
```

#### ②、创建客户端

```java
import java.io.PrintWriter;
import java.net.Socket;

public class BasicSocketClient {
    public static void main(String[] args) {
        // 创建Socket对象
        try (Socket socket = new Socket("127.0.0.1",8888);
             // 创建向服务端发送消息的输出流对象
             PrintWriter pw = new PrintWriter(socket.getOutputStream())
        ){
            pw.println("服务端，您好！");
            pw.flush();

        }catch (Exception e){
            e.printStackTrace();
        }
    }
}
```

### 3、TCP单向通信

单向通信是指通信双方中，一方固定为发送端，一方则固定为接收端。

#### ①、创建服务端

```java
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.PrintWriter;
import java.net.ServerSocket;
import java.net.Socket;

public class OneWaySocketServer {
    public static void main(String[] args) {
        System.out.println("服务端启动，开始监听.......");
        try (ServerSocket serverSocket = new ServerSocket(8888);
             Socket socket = serverSocket.accept();
             // 通过与客户端对应的Socket对象获取输入流对象
             BufferedReader br = new BufferedReader(new InputStreamReader(socket.getInputStream()));
             // 通过与客户单对应的Socket对象获取输出流对象
             PrintWriter pw = new PrintWriter(socket.getOutputStream());
        ){
            System.out.println("连接成功！");

            while (true){
                // 读取客户端发送的消息
                String str = br.readLine();
                System.out.println("客户端说：" + str);
                if ("exit".equals(str)){
                    break;
                }
                pw.println(str);
                pw.flush();
            }

        }catch (Exception e){
            e.printStackTrace();
        }
    }
}
```

#### ②、创建客户端

```java
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.PrintWriter;
import java.net.Socket;
import java.util.Scanner;

public class OneWaySocketClient {
    public static void main(String[] args) {
        // 获取与服务端对应的Socket对象
        try (Socket socket = new Socket("127.0.0.1",8888);
             // 创建键盘输入对象
             Scanner scanner = new Scanner(System.in);
             // 通过与服务端对应的Socket对象获取输出流对象
             PrintWriter pw = new PrintWriter(socket.getOutputStream());
             // 通过与服务端对应的Socket对象获取输入流对象
             BufferedReader br = new BufferedReader(new InputStreamReader(socket.getInputStream()));
        ){
            while (true){
                // 通过键盘输入获取需要向服务端发送的消息
                String str = scanner.nextLine();

                // 将消息发送到服务端
                pw.println(str);
                pw.flush();

                if ("exit".equals(str)){
                    break;
                }
                // 读取服务端返回的消息
                String serverInput = br.readLine();
                System.out.println("服务端返回的是：" + serverInput);
            }

        }catch (Exception e){
            e.printStackTrace();
        }
    }
}
```



### 4、TCP双向通信

双向通信是指通信双方中，任何一方都可为发送端，任何一方都可为接收端。

#### ①、创建服务端

```java
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.PrintWriter;
import java.net.ServerSocket;
import java.net.Socket;
import java.util.Scanner;

public class TwoWaySocketServer {
    public static void main(String[] args) {
        System.out.println("服务端启动，监听端口8888.....");
        try (ServerSocket serverSocket = new ServerSocket(8888);
             Socket socket = serverSocket.accept();
             // 创建键盘输入对象
             Scanner scanner = new Scanner(System.in);
             // 通过与客户端对应的Socket对象获取输入流对象
             BufferedReader br = new BufferedReader(new InputStreamReader(socket.getInputStream()));
             // 通过与客户端对应的Socket对象获取输出流对象
             PrintWriter pw = new PrintWriter(socket.getOutputStream());
        ){
            System.out.println("连接成功！");
            while (true){
                // 读取客户端发送的消息
                String str = br.readLine();
                System.out.println("客户端说：" + str);
                String keyInput = scanner.nextLine();
                // 发送到客户端
                pw.println(keyInput);
                pw.flush();
            }

        }catch (Exception e){
            e.printStackTrace();
        }
    }
}
```

#### ②、创建客户端

```java
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.PrintWriter;
import java.net.Socket;
import java.util.Scanner;

public class TwoWaySocketClient {
    public static void main(String[] args) {
        try (Socket socket = new Socket("127.0.0.1",8888);
             // 创建键盘输入对象
             Scanner scanner = new Scanner(System.in);
             // 通过与服务端对应的Socket对象获取输入流对象
             BufferedReader br = new BufferedReader(new InputStreamReader(socket.getInputStream()));
             // 通过与服务端对应的Socket对象获取输出流对象
             PrintWriter pw = new PrintWriter(socket.getOutputStream());
        ){
            while (true){
                // 通过键盘输入获取信息
                String str = scanner.nextLine();
                // 向服务端发送消息
                pw.println("客户端说：" + str);
                pw.flush();

                // 接收服务端发送的消息
                String keyInput = br.readLine();
                System.out.println("服务端说：" + keyInput);
            }

        }catch (Exception e){
            e.printStackTrace();
        }
    }
}
```

### 5、创建点对点的聊天应用

#### ①、创建服务端

```java
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.PrintWriter;
import java.net.ServerSocket;
import java.net.Socket;
import java.util.Scanner;

/**
 * 发送消息线程
 */
class Send extends Thread{
    private Socket socket;
    public Send(Socket socket){
        this.socket = socket;
    }
    @Override
    public void run() {
        this.sendMsg();
    }

    /**
     * 发送消息的方法
     */
    private void sendMsg(){
        // 创建Scanner对象
        try (Scanner scanner = new Scanner(System.in);
             // 创建向对方输出消息的流对象
             PrintWriter pw = new PrintWriter(this.socket.getOutputStream())
        ){
            while (true){
                String msg = scanner.nextLine();
                pw.println(msg);
                pw.flush();
            }

        }catch (Exception e){
            e.printStackTrace();
        }
    }
}

/**
 * 接收消息的线程
 */
class Receive extends Thread{
    private Socket socket;
    public Receive(Socket socket){
        this.socket = socket;
    }

    @Override
    public void run() {
		this.receiveMsg();
    }

    /**
     * 用于接收对方消息的方法
     */
    private void receiveMsg(){
        try (BufferedReader br = new BufferedReader(new InputStreamReader(this.socket.getInputStream()))){
            while (true) {
                String msg = br.readLine();
                System.out.println("他说：" + msg);
            }
        }catch (Exception e){
            e.printStackTrace();
        }
    }
}

public class ChatSocketServer {
    /**
     * 主线程
     */
    public static void main(String[] args) {
        try (ServerSocket serverSocket = new ServerSocket(8888)){
            System.out.println("服务端启动，等待连接......");
            // try-with-resource括号中内容，主线程结束后，括号中内容会自动释放关闭，所以将Socket对象置于括号以外
            Socket socket = serverSocket.accept();
            System.out.println("连接成功！");
            // 将与客户端对应的Socket对象传递给发送消息的线程，并启动该线程
            new Send(socket).start();
            // 将与客户端对应的Socket对象传递给接收消息的线程，并启动该线程
            new Receive(socket).start();
        }catch (Exception e){
            e.printStackTrace();
        }
    }
}
```

#### ②、创建客户端

```java
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.PrintWriter;
import java.net.Socket;
import java.util.Scanner;

/**
 * 用于发送消息的线程类
 */
class ClientSend extends Thread{
    private Socket socket;
    public ClientSend(Socket socket){
        this.socket = socket;
    }

    @Override
    public void run() {
        this.sendMsg();
    }

    /**
     * 发送消息的方法
     */
    private void sendMsg(){
        // 创建Scanner对象
        try (Scanner scanner = new Scanner(System.in);
             // 创建向对方输出消息的流对象
             PrintWriter pw = new PrintWriter(socket.getOutputStream())
        ){
            while (true){
                String msg = scanner.nextLine();
                pw.println(msg);
                pw.flush();
            }

        }catch (Exception e){
            e.printStackTrace();
        }
    }
}

/**
 * 用于接收消息的线程类
 */
class ClientReceive extends Thread{
    private Socket socket;
    public ClientReceive(Socket socket){
        this.socket = socket;
    }
    @Override
    public void run() {
        this.receiveMsg();
    }

    /**
     *  用于接收对方消息的方法
     */
    private void receiveMsg(){
        //创建用于接收对方发送消息的流对象
        try (BufferedReader br = new BufferedReader(new InputStreamReader(this.socket.getInputStream()))){
            while (true) {
                String msg = br.readLine();
                System.out.println("他说：" + msg);
            }

        }catch (Exception e){
            e.printStackTrace();
        }
    }
}

public class ChatSocketClient {
    public static void main(String[] args) {
        try {
            Socket socket = new Socket("127.0.0.1",8888);
            System.out.println("连接成功！");
            new ClientSend(socket).start();
            new ClientReceive(socket).start();

        }catch (Exception e){
            e.printStackTrace();
        }
    }
}
```

#### ③、优化点对点聊天应用

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.io.PrintWriter;
import java.net.ServerSocket;
import java.net.Socket;
import java.util.Scanner;

/**
 * 发送消息的线程
 */
class Send1 extends Thread{
    private Socket socket;
    private Scanner scanner;
    public Send1(Socket socket, Scanner scanner){
        this.socket = socket;
        this.scanner = scanner;
    }
    @Override
    public void run() {
        this.sendMsg();
    }

    /**
     * 发送消息
     */
    public void sendMsg(){
        //创建向对方输出消息的流对象
        try (PrintWriter pw = new PrintWriter(socket.getOutputStream())){
            while (true){
                String msg = scanner.nextLine();
                pw.println(msg);
                pw.flush();
            }
        }catch (Exception e){
            e.printStackTrace();
        }
    }
}

/**
 * 接收消息的线程
 */
class Receive1 extends Thread{
    private Socket socket;
    public Receive1(Socket socket){
        this.socket = socket;
    }

    @Override
    public void run() {
        this.receiveMsg();
    }

    /**
     * 用于接收对方消息的方法
     */
    private void receiveMsg(){
        //创建用于接收对方发送消息的流对象
        try (BufferedReader br = new BufferedReader(new InputStreamReader(this.socket.getInputStream()))){
            while (true) {
                String str = br.readLine();
                System.out.println("他说：" + str);
            }
        }catch (Exception e){
            e.printStackTrace();
        }
    }
}

public class GoodTCP {
    public static void main(String[] args) {
        Scanner scanner = null;
        ServerSocket serverSocket = null;
        Socket socket = null;
        try {
            scanner = new Scanner(System.in);
            System.out.println("请输入：server,<port> 或者: <ip>,<port>");
            String str = scanner.nextLine();
            String[] arr = str.split(",");
            if ("server".equals(arr[0])){
                // 启动服务器端
                System.out.println("TCP Server Listen at" + arr[1] + ".......");
                serverSocket = new ServerSocket(Integer.parseInt(arr[1]));
                socket = serverSocket.accept();
                System.out.println("连接成功！");
            }else {
                // 启动客户端
                socket = new Socket(arr[0],Integer.parseInt(arr[1]));
                System.out.println("连接成功！");
            }
            // 启动发送消息的线程
            new Send1(socket,scanner).start();
            // 启动接收消息的线程
            new Receive1(socket).start();
        }catch (Exception e){
            e.printStackTrace();
        }finally {
            if (serverSocket != null){
                try {
                    serverSocket.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            }
        }
    }
}
```

### 6、一对多应答型服务器

**注：与上文GoodTCP联合使用，支持多开！**

```java
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.PrintWriter;
import java.net.ServerSocket;
import java.net.Socket;

/**
 * 定义消息处理线程类
 */
class Msg extends Thread{
    private Socket socket;
    public Msg(Socket socket){
        this.socket = socket;
    }
    @Override
    public void run() {
        this.msg();
    }

    /**
     *  将从客户端读取到的消息写回给客户端
     */
    private void msg(){
        try (BufferedReader br = new BufferedReader(new InputStreamReader(this.socket.getInputStream()));
             PrintWriter pw = new PrintWriter(this.socket.getOutputStream())
        ){
            while (true){
                pw.println(br.readLine() + "[ok]");
                pw.flush();
            }

        }catch (Exception e){
            e.printStackTrace();
            System.out.println(this.socket.getInetAddress() + "断线了！");
        }
    }
}


public class EchoServer {
    public static void main(String[] args) {
        try (ServerSocket serverSocket = new ServerSocket(8888)){
            // 等待多客户连接
            while (true) {
                Socket socket = serverSocket.accept();
                new Msg(socket).start();
            }
        }catch (Exception e){
            e.printStackTrace();
        }
    }
}
```

### 7、一对多聊天服务器

#### ①服务器设计

1. 服务器的连接设计

   ![image-20220527184457994](https://www.itbaizhan.com/wiki/imgs/image-20220527184457994-16536482993141.png)

2. 服务器的线程设计

![image-20220527184510072](https://www.itbaizhan.com/wiki/imgs/image-20220527184510072-16536483109772.png)

 

#### ②创建一对多聊天服务应用

```java

import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.PrintWriter;
import java.net.ServerSocket;
import java.net.Socket;

/**
 * 接收客户端消息的线程类
 */
class ChatReceive extends Thread{
    private Socket socket;
    public ChatReceive(Socket socket){
        this.socket = socket;
    }

    @Override
    public void run() {
        this.receiveMsg();
    }

    /**
     *  实现接收客户端发送的消息
     */
    private void receiveMsg(){
        try (BufferedReader br = new BufferedReader(new InputStreamReader(this.socket.getInputStream()))){
            while (true){
                String msg = br.readLine();
                synchronized ("abc") {
                    // 把读取到的数据写入公共数据区
                    ChatRoomServer.buf = "[" + this.socket.getInetAddress() + "] " + msg;
                    // 唤醒发送消息的线程对象
                    "abc".notifyAll();
                }
            }
        }catch (Exception e){
            e.printStackTrace();
        }
    }
}

/**
 * 向客户端发送消息的线程类
 */
class ChatSend extends Thread{
    private Socket socket;
    public ChatSend(Socket socket){
        this.socket = socket;
    }

    @Override
    public void run() {
        this.sendMsg();
    }

    /**
     * 将公共数据区的消息发送给客户端
     */
    private void sendMsg(){
        try (PrintWriter pw = new PrintWriter(this.socket.getOutputStream())){
            while (true) {
                synchronized ("abc") {
                    // 让发送消息的线程处于等待状态
                    "abc".wait();
                    // 将公共数据区中的消息发送给客户端
                    pw.println(ChatRoomServer.buf);
                    pw.flush();
                }
            }
        }catch (Exception e){
            e.printStackTrace();
        }
    }
}
public class ChatRoomServer {
    // 定义公共数据区
    public static String buf;
    public static void main(String[] args) {
        System.out.println("Chat Server Version 1.0");
        System.out.println("Listen at 8888...");
        try (ServerSocket serverSocket = new ServerSocket(8888)){
            while (true) {
                Socket socket = serverSocket.accept();
                System.out.println("连接到：" + socket.getInetAddress());
                new ChatReceive(socket).start();
                new ChatSend(socket).start();
            }
        }catch (Exception e){
            e.printStackTrace();
        }
    }
}
```

## III、UDP通信的实现和项目案例

### 1、UDP通信实现原理

UDP协议与之前讲到的TCP协议不同，是面向无连接的，双方不需要建立连接便可通信。UDP通信所发送的数据需要进行封包操作（使用DatagramPacket类），然后才能接收或发送（使用DatagramSocket类）。

![image-20220527185723458](https://www.itbaizhan.com/wiki/imgs/image-20220527185723458-16536490444325.png)

#### ①、DatagramPacket：数据容器（封包）的作用

此类表示数据报包。 数据报包用来实现封包的功能。

**常用方法：**

| 方法名                                                       | 使用说明                                                     |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| DatagramPacket(byte[] buf, int length)                       | 构造数据报包，用来接收长度为 length 的数据包                 |
| DatagramPacket(byte[] buf, int length, InetAddress address, int port) | 构造数据报包，用来将长度为 length 的包发送到指定主机上的指定端口号 |
| getAddress()                                                 | 获取发送或接收方计算机的IP地址，此数据报将要发往该机器或者是从该机器接收到的 |
| getData()                                                    | 获取发送或接收的数据                                         |
| setData(byte[] buf)                                          | 设置发送的数据                                               |

#### ②、DatagramSocket：用于发送或接收数据报包

当服务器要向客户端发送数据时，需要在服务器端产生一个DatagramSocket对象，在客户端产生一个DatagramSocket对象。服务器端的DatagramSocket将DatagramPacket发送到网络上，然后被客户端的DatagramSocket接收。

DatagramSocket有两种常用的构造函数。一种是无需任何参数的，常用于客户端；另一种需要指定端口，常用于服务器端。如下所示：

1. DatagramSocket() ：构造数据报套接字并将其绑定到本地主机上任何可用的端口。
2. DatagramSocket(int port) ：创建数据报套接字并将其绑定到本地主机上的指定端口。

#### ③、常用方法：

| 方法名                    | 使用说明               |
| ------------------------- | ---------------------- |
| send(DatagramPacket p)    | 从此套接字发送数据报包 |
| receive(DatagramPacket p) | 从此套接字接收数据报包 |
| close()                   | 关闭此数据报套接字     |



#### ④、UDP通信编程基本步骤：

1. 创建客户端的DatagramSocket，创建时，定义客户端的监听端口。
2. 创建服务器端的DatagramSocket，创建时，定义服务器端的监听端口。
3. 在服务器端定义DatagramPacket对象，封装待发送的数据包。
4. 客户端将数据报包发送出去。
5. 服务器端接收数据报包。

### 2、 UDP通信入门案例

#### ①、创建服务端

```java
import java.net.DatagramPacket;
import java.net.DatagramSocket;

public class UDPServer {
    public static void main(String[] args) {
        // 创建服务端接收数据的DatagramSocket对象
        try (DatagramSocket datagramSocket = new DatagramSocket(9999)){
             // 创建数据缓存区
            byte[] b = new byte[1024];
            // 创建数据报包对象
            DatagramPacket datagramPacket = new DatagramPacket(b,b.length);
            // 等待接收客户端所发送的数据
            datagramSocket.receive(datagramPacket);
            String str = new String(datagramPacket.getData(),0,datagramPacket.getLength());
            System.out.println(str);


        }catch (Exception e){
            e.printStackTrace();
        }
    }
}
```

#### ②、创建客户端

```java
import java.net.DatagramPacket;
import java.net.DatagramSocket;
import java.net.InetSocketAddress;

public class UDPClient {
    public static void main(String[] args) {
        // 创建数据发送对象，DatagramSocket，需要指定消息的发送端口
        try (DatagramSocket datagramSocket = new DatagramSocket(8888)){

            // 消息需要进行类型转换，转换成字节数据类型
            byte[] b = "无敌的我！".getBytes();
            // 创建数据报包 包装对象DatagramSocket
            DatagramPacket datagramPacket = new DatagramPacket(b,b.length,new InetSocketAddress("127.0.0.1",9999));
            // 发送消息
            datagramSocket.send(datagramPacket);
        }catch (Exception e){
            e.printStackTrace();
        }
    }
}
```

### 3、传递基本数据类型

#### ①、创建服务端

```java
import java.io.ByteArrayInputStream;
import java.io.DataInputStream;
import java.net.DatagramPacket;
import java.net.DatagramSocket;

public class BasicTypeUDPServer {
    public static void main(String[] args) {
        try (DatagramSocket datagramSocket = new DatagramSocket(9999)){
            byte[] bytes = new byte[1024];
            DatagramPacket datagramPacket = new DatagramPacket(bytes,0,bytes.length);
            datagramSocket.receive(datagramPacket);
            // 实现数据类型转换
            try (DataInputStream dis = new DataInputStream(new ByteArrayInputStream(datagramPacket.getData()))) {
                // 通过基本数据数据流对象获取传递的数据
                System.out.println(dis.readLong());
            }
        }catch (Exception e){
            e.printStackTrace();
        }
    }
}
```

#### ②、创建客户端

```java
import java.io.ByteArrayOutputStream;
import java.io.DataOutputStream;
import java.net.DatagramPacket;
import java.net.DatagramSocket;
import java.net.InetSocketAddress;

public class BasicTypeUDPClient {
    public static void main(String[] args) {
        long n = 2000l;
        try (DatagramSocket datagramSocket = new DatagramSocket(8888);
             ByteArrayOutputStream bos = new ByteArrayOutputStream();
             DataOutputStream dos = new DataOutputStream(bos);
        ){
            dos.writeLong(n);
            // 将基本数据类型转换成数组
            byte[] bytes = bos.toByteArray();
            // 将数据包装成DatagramPacket对象
            DatagramPacket datagramPacket = new DatagramPacket(bytes,bytes.length,new InetSocketAddress("127.0.0.1",9999));
            // 发送数据
            datagramSocket.send(datagramPacket);

        }catch (Exception e){
            e.printStackTrace();
        }
    }
}
```

### 4、传递自定义对象类型

#### ①、创建Person类

```java
package UDP;

/**
 * 当该对象需要在网络上传输时，一定要实现Serializable接口
 */
public class Person implements Serializable{
    private String name;
    private int age;

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    @Override
    public String toString() {
        return "Person{" +
                "name='" + name + '\'' +
                ", age=" + age +
                '}';
    }
}
```

#### ②、创建服务端

```java
package UDP;

import java.io.ByteArrayInputStream;
import java.io.ObjectInputStream;
import java.net.DatagramPacket;
import java.net.DatagramSocket;

public class ObjectTypeServer {
    public static void main(String[] args) {
        try (DatagramSocket datagramSocket = new DatagramSocket(9999)){
            byte[] bytes = new byte[1024];
            DatagramPacket datagramPacket = new DatagramPacket(bytes,0,bytes.length);
            // 接收数据
            datagramSocket.receive(datagramPacket);
            // 对接收的内容做类型转换
            try (ObjectInputStream ois = new ObjectInputStream(new ByteArrayInputStream(datagramPacket.getData()))){
                Person person = (Person) ois.readObject();
                System.out.println(person);
            }
        }catch (Exception e){
            e.printStackTrace();
        }
    }
}
```

#### ③、创建客户端

```java
package UDP;

import java.io.ByteArrayOutputStream;
import java.io.ObjectOutputStream;
import java.net.DatagramPacket;
import java.net.DatagramSocket;
import java.net.InetSocketAddress;

public class ObjectTypeClient {
    public static void main(String[] args) {
        try (DatagramSocket datagramSocket = new DatagramSocket(8888);
             ByteArrayOutputStream bos = new ByteArrayOutputStream();
             ObjectOutputStream oos = new ObjectOutputStream(bos);
        ){
            Person p = new Person();
            p.setName("lisi");
            p.setAge(18);

            oos.writeObject(p);
            byte[] bytes = bos.toByteArray();
            // 将数据包装成DatagramPacket对象
            DatagramPacket datagramPacket = new DatagramPacket(bytes,bytes.length,new InetSocketAddress("127.0.0.1",9999));

            // 发送数据
            datagramSocket.send(datagramPacket);

        }catch (Exception e){
            e.printStackTrace();
        }
    }
}
```

## IV、本章总结

- 端口是虚拟的概念，并不是说在主机上真的有若干个端口。
- 在www上，每一信息资源都有统一且唯一的地址，该地址就叫URL（Uniform Resource Locator），它是www的统一资源定位符。
- TCP与UDP的区别
  - TCP是面向连接的，传输数据安全，稳定，效率相对较低。
  - UDP是面向无连接的，传输数据不安全，效率较高。
- Socket通信是一种基于TCP协议，建立稳定连接的点对点的通信。
- 网络编程是由java.net包来提供网络功能。
  - InetAddress：封装计算机的IP地址和DNS（没有端口信息！）。
  - InetSocketAddress：包含IP和端口，常用于Socket通信。
  - URL：以使用它的各种方法来对URL对象进行分割、合并等处理。
- 基于TCP协议的Socket编程和通信
  - “请求-响应”模式：
    - Socket类：发送TCP消息。
    - ServerSocket类：创建服务器。
- UDP通讯的实现
  - DatagramSocket：用于发送或接收数据报包。
  - 常用方法：send()、receive()、 close()。
- DatagramPacket：数据容器（封包）的作用
  - 常用方法：构造方法、getAddrress(获取发送或接收方计算机的IP地址)、getData(获取发送或接收的数据)、setData(设置发送的数据)。

# 五、反射机制介绍

![image-20220529104312037](https://www.itbaizhan.com/wiki/imgs/image-20220529104312037-16537921932711.png)

## 〇、什么是反射

Java 反射机制是Java语言一个很重要的特性，它使得Java具有了“动态性”。在Java程序运行时，对于任意的一个类，我们能不能知道这个类有哪些属性和方法呢？对于任意的一个对象，我们又能不能调用它任意的方法？答案是肯定的！这种动态获取类的信息以及动态调用对象方法的功能就来自于Java 语言的反射（Reflection）机制。

## I、反射的作用

简单来说两个作用，RTTI（运行时类型识别）和DC（动态创建）。

我们知道反射机制允许程序在运行时取得任何一个已知名称的class的内部信息，包括其modifiers(修饰符)，fields(属性)，methods(方法)等，并可于运行时改变fields内容或调用methods。那么我们便可以更灵活的编写代码，代码可以在运行时装配，无需在组件之间进行源代码链接，降低代码的耦合度；还有动态代理的实现等等；但是需要注意的是反射使用不当会造成很高的资源消耗！

**实时效果反馈**

**1**.**如下对Java反射描述错误的是？**

A 反射可以使代码在运行时装配；

B 反射可以降低代码的耦合度；

C 通过反射可以实现动态代理；

D 反射不会造成很高的资源消耗；

**答案**

1=>D

 创建对象过程

## II、Java创建对象的三个阶段

![image-20220529114936405](https://www.itbaizhan.com/wiki/imgs/image-20220529114936405-16537961772473.png)

### 1、创建对象时内存结构

```

Users user = new Users();
```

![image-20220528190213358](https://www.itbaizhan.com/wiki/imgs/image-20220528190213358-16537357344723.png)

实际上，我们在加载任何一个类时都会在方法区中建立“这个类对应的Class对象”，由于“Class对象”包含了这个类的整个结构信息，所以我们可以通过这个“Class对象”来操作这个类。

我们要使用一个类，首先要加载类；加载完类之后，在堆内存中，就产生了一个 Class 类型的对象（一个类只有一个 Class 对象），这个对象就包含了完整的类的结构信息。我们可以通过这个对象知道类的结构。这个对象就像一面镜子，透过这个镜子可以看到类的结构，所以，我们形象的称之为：反射。 因此，“Class对象”是反射机制的核心。

**实时效果反馈**

**1**.**如下对Class对象描述错误的是？**

A Class对象包含了这个类的整个结构信息；

B 通过Class对象可以获取类的相关信息；

C 一个类可以有多个 Class 对象；

D Class对象是反射机制的核心；

**答案**

1=>C

 反射的具体实现

## III、获取Class对象的三种方式

- 通过getClass()方法;

- 通过.class 静态属性;

- 通过Class类中的静态方法forName();

  

  创建User类

  ```java
  package com.itshihao;
  
  public class Users {
      private String userName;
      private int age;
  
      public String getUserName() {
          return userName;
      }
  
      public void setUserName(String userName) {
          this.userName = userName;
      }
  
      public int getAge() {
          return age;
      }
  
      public void setAge(int age) {
          this.age = age;
      }
  }
  ```

  

  ### 1、通过getClass()方法;

```java
/**
 *  通过getClass()方法获取该类的Class对象
 */
public class GetClass1 {
    public static void main(String[] args) {
        Users users = new Users();
        Users users1 = new Users();
        Class aClass = users.getClass();
        System.out.println(aClass);  // class com.itshihao.Users
        System.out.println(aClass.getName());  // com.itshihao.Users
        System.out.println(users.getClass() == users1.getClass());  // true

    }
}
```

### 2、通过.class 静态属性获取Class对象

```java
/**
 * 通过.class静态属性获取该类的Class对象
 */
public class GetClass2 {
    public static void main(String[] args) {
        Class clazz = Users.class;
        Class clazz1 = Users.class;
        System.out.println(clazz); // class com.itshihao.Users
        System.out.println(clazz.getName()); // com.itshihao.Users
        System.out.println(clazz == clazz1); // true
    }
}
```

### 3、通过forName()获取Class对象

```java
/**
 * 通过Class.forName("ClassName“)获取Class对象
 */
public class GetClass3 {
    public static void main(String[] args) throws Exception{
        Class clazz = Class.forName("com.itshihao.Users");
        Class clazz1 = Class.forName("com.itshihao.Users");
        System.out.println(clazz); // class com.itshihao.Users
        System.out.println(clazz.getName());// com.itshihao.Users
        System.out.println(clazz == clazz1); // true
    }
}
```

## IV、获取类的构造方法

### 1、方法介绍

| 方法名                                             | 描述                                                         |
| -------------------------------------------------- | ------------------------------------------------------------ |
| getDeclaredConstructors()                          | 返回 Constructor 对象的一个数组，这些对象反映此 Class 对象表示的类声明的所有构造方法。 |
| getConstructors()                                  | 返回一个包含某些 Constructor 对象的数组，这些对象反映此 Class 对象所表示的类的所有公共（public）构造方法。 |
| getConstructor(Class<?>... parameterTypes)         | 返回一个 Constructor 对象，它反映此 Class 对象所表示的类的指定公共（public）构造方法。 |
| getDeclaredConstructor(Class<?>... parameterTypes) | 返回一个 Constructor 对象，该对象反映此 Class 对象所表示的类或接口的指定构造方法。 |

### 2、方法使用

### ①、修改Users类

```java
package com.itshihao;

public class Users {
    private String userName;
    private int age;

    public Users() {
    }

    public Users(String userName, int age) {
        this.userName = userName;
        this.age = age;
    }
    public Users(String userName){
        this.userName = userName;
    }
    private Users(int age){
        this.age = age;
    }

    public String getUserName() {
        return userName;
    }

    public void setUserName(String userName) {
        this.userName = userName;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }
}
```

#### ②、获取构造方法

```java
package com.itshihao;

import java.lang.reflect.Constructor;

public class GetConstructor {
    public static void main(String[] args) throws Exception{
        Class clazz = Users.class;
        // 获取类的构造方法
        Constructor[] arr = clazz.getDeclaredConstructors();
        for (Constructor c : arr) {
            System.out.println(c);
        }
        /**
         * private com.itshihao.Users(int)
         * public com.itshihao.Users(java.lang.String)
         * public com.itshihao.Users(java.lang.String,int)
         * public com.itshihao.Users()
         */

        System.out.println("-----------------------");
        Constructor[] arr1 = clazz.getConstructors();
        for (Constructor c : arr1) {
            System.out.println(c);
        }
        /**
         * public com.itshihao.Users(java.lang.String)
         * public com.itshihao.Users(java.lang.String,int)
         * public com.itshihao.Users()
         */

        System.out.println("-----------------------");
        Constructor c = clazz.getDeclaredConstructor(int.class);
        System.out.println(c); // private com.itshihao.Users(int)
        System.out.println("-----------------------");
        Constructor c1 = clazz.getConstructor(null);
        System.out.println(c1); // public com.itshihao.Users()
    }
}
```

### 3、通过构造方法创建对象

```java
import java.lang.reflect.Constructor;

public class GetConstructor2 {
    public static void main(String[] args) throws Exception{
        // 获取类对象
        Class clazz = Users.class;
        // 通过类对象，获取指定的构造方法对象
        Constructor c = clazz.getConstructor(String.class, int.class);
        // 通过指定构造方法，创建对象
        Object o = c.newInstance("lisi", 1999);
        Users u = (Users) o;
        System.out.println(u); // Users类中需重写toString()方法   Users{userName='lisi', age=1999}
        System.out.println(u.getUserName() + "\t" + u.getAge()); //lisi    1999
    }
}
```

## V、获取类的成员变量

### 1、方法介绍

![image-20220709165154233](../AppData/Roaming/Typora/typora-user-images/image-20220709165154233.png)

### 2、方法使用

```java
package com.itshihao;

import java.lang.reflect.Field;

public class GetField {
    public static void main(String[] args) throws Exception{
        Class clazz = Users.class;

        Field[] arr = clazz.getFields();
        for (Field field : arr) {
            System.out.println(field);
            System.out.println(field.getName());
        }
        /**
          public int com.itshihao.Users.age
          age
         */
        System.out.println("-----------------------");

        Field[] arr1 = clazz.getDeclaredFields();
        for (Field field : arr1) {
            System.out.println(field);
            System.out.println(field.getName());
        }
        /**
         private java.lang.String com.itshihao.Users.userName
         userName
         public int com.itshihao.Users.age
         age
         */
        System.out.println("--------------------------");

        Field field = clazz.getField("age");
        System.out.println(field); // public int com.itshihao.Users.age

        System.out.println("---------------------------");
        Field field1 = clazz.getDeclaredField("userName");
        System.out.println(field1); // private java.lang.String com.itshihao.Users.userName
    }
}
```

### **3、操作成员变量**

```java
import java.lang.reflect.Field;

public class GetField2 {
    public static void main(String[] args) throws Exception{
        Class clazz = Users.class;
        Field field = clazz.getField("age");
        // 对象实例化
        Object o = clazz.getConstructor(null).newInstance();
        // 为成员变量赋值
        field.set(o,18);
        // 获取成员变量的值
        Object o1 = field.get(o); // 自动装箱、拆箱处理。
        System.out.println(o1);
    }
}
```

## VI、获取类的方法

### **1、方法介绍**

| 方法名                                                   | 描述                                                   |
| -------------------------------------------------------- | ------------------------------------------------------ |
| getMethods()                                             | 返回一个Method类型的数组，其中包含所有公共(public)方法 |
| getDeclaredMethods()                                     | 返回一个Method类型的数组，其中包含所有方法             |
| getMethod(String name,Class<?>...parameterTypes)         | 返回一个公共的Method方法对象                           |
| getDeclaredMethod(String name,Class<?>...parameterTypes) | 返回一个方法Method对象                                 |

### 2、**方法使用**

```java
package com.itshihao;

import java.lang.reflect.Method;

public class GetMethod {
    public static void main(String[] args) throws Exception{
        Class clazz = Users.class;
        Method[] arr = clazz.getMethods();
        for (Method m : arr) {
            System.out.println(m);
            System.out.println(m.getName());
        }
        System.out.println("-----------------------");

        Method[] arr1 = clazz.getDeclaredMethods();
        for (Method m : arr1) {
            System.out.println(m);
            System.out.println(m.getName());
        }
        System.out.println("--------------------------");

        Method method = clazz.getMethod("setAge", int.class);
        System.out.println(method);
        System.out.println(method.getName());
        System.out.println("--------------------------");

        Method method1 = clazz.getDeclaredMethod("suibian");
        System.out.println(method1);
        System.out.println(method1.getName());
    }
}
```

### 3、调用方法

```java
import java.lang.reflect.Method;

public class GetMethod2 {
    public static void main(String[] args) throws Exception{
        Class clazz = Users.class;
        Method method = clazz.getMethod("setUserName", String.class);
        // 实例化对象
        Object obj = clazz.getConstructor(null).newInstance();
        // 执行该方法
        method.invoke(obj,"oldli");
        // 通过getUserName获取值
        Method m1 = clazz.getMethod("getUserName");
        Object o = m1.invoke(obj);
        System.out.println(o);

    }
}
```

## VII、获取类的其他信息

```java
public class GetClassInfo {
    public static void main(String[] args) {
        Class<Users> clazz = Users.class;
        // 获取类名
        String className = clazz.getName();
        System.out.println(className);
        // 获取包名
        Package p = clazz.getPackage();
        System.out.println(p.getName());
        // 获取超类
        Class superclass = clazz.getSuperclass();
        System.out.println(superclass.getName());
        // 获取该类实现的所有接口
        Class[] interfaces = clazz.getInterfaces();
        for (Class anInterface : interfaces) {
            System.out.println(anInterface.getName());
        }
    }
}
```

## VIII、反射应用案例

需求：根据给定的方法名顺序来决定方法的执行顺序。

```java
package com.itshihao;

import java.lang.reflect.Method;

class Reflect{
    public void method1(){
        System.out.println("Method1.........");
    }
    public void method2(){
        System.out.println("Method2.........");
    }
    public void method3(){
        System.out.println("Method3.........");
    }
}
public class ReflectDemo {
    public static void main(String[] args) throws Exception{
        Reflect reflect = new Reflect();
        if (args != null && args.length > 0){
            // 获取Reflect的CLass对象
            Class clazz = reflect.getClass();
            // 通过反射获取Reflect的所有方法
            Method[] methods = clazz.getMethods();
            for (String str : args){
                for(int i = 0 ;i < methods.length; i++){
                    if (str.equalsIgnoreCase(methods[i].getName())){
                        methods[i].invoke(reflect);
                        break;
                    }
                }
            }
        }else {
            reflect.method1();
            reflect.method2();
            reflect.method3();
        }
    }
}
```

结果1：没有给定program arguments 时(是要**传给你的应用程序的，它通过主函数中的 args 来传值**)**

![image-20220710170223333](../AppData/Roaming/Typora/typora-user-images/image-20220710170223333.png)

```java
Method1.........
Method2.........
Method3.........
```

结果2：给定program arguments时

![image-20220710170345211](../AppData/Roaming/Typora/typora-user-images/image-20220710170345211.png)

```java
Method3.........
Method2.........
Method1.........
```

## IX、反射机制的效率

由于Java反射是要解析字节码，将内存中的对象进行解析，包括了一些动态类型，而JVM无法对这些代码进行优化。因此，反射操作的效率要比那些非反射操作低得多！

接下来我们做个简单的测试来直接感受一下反射的效率。

### 反射机制的效率测试

```java
import java.lang.reflect.Method;

public class Test {
    public static void main(String[] args) {
        try {
            // 反射耗时
            Class<?> clazz = Class.forName("com.itshihao.Users");
            Users users = (Users) clazz.getConstructor(null).newInstance();
            long startTime = System.currentTimeMillis();
            Method method = clazz.getMethod("setUserName", String.class);
            for (int i = 0; i < 100000000; i++) {
                method.invoke(users,"lisi");
            }
            long endTime = System.currentTimeMillis();

            // 非反射方式耗时
            Users user1 = new Users();
            long start = System.currentTimeMillis();
            for (int i = 0; i < 100000000; i++) {
                user1.setUserName("lisi");
            }
            long end = System.currentTimeMillis();
            System.out.println("反射方式耗时：" + (endTime - startTime));
            System.out.println("非反射方式耗时：" + (end - start));
        } catch (Exception e) {
            throw new RuntimeException(e);
        }
    }
}
// 反射方式耗时：368ms
// 非反射方式耗时：174ms
```

## X、setAccessible方法

setAccessible()方法：

setAccessible是启用和禁用访问安全检查的开关。值为 true 则指示反射的对象在使用时应该取消 Java 语言访问检查。值为 false 则指示反射的对象应该实施 Java 语言访问检查;默认值为false。

由于JDK的安全检查耗时较多.所以通过setAccessible(true)的方式关闭安全检查就可以达到提升反射速度的目的

```java
import java.lang.reflect.Field;
import java.lang.reflect.Method;

public class Test2 {
    public static void main(String[] args) throws Exception{
        Users users = new Users();
        Class clazz = users.getClass();
        Field field = clazz.getDeclaredField("userName");
        // 忽略安全检查
        field.setAccessible(true);
        field.set(users,"lisi");
        Object obj = field.get(users);
        System.out.println(obj);
        System.out.println("---------------------------");
        Method method = clazz.getDeclaredMethod("suibian");
        method.setAccessible(true);
        method.invoke(users);
    }
}
```

若不忽略安全检查，则会出现下列情况：

<img src="../AppData/Roaming/Typora/typora-user-images/image-20220710175238990.png" alt="image-20220710175238990" style="zoom: 200%;" />

# 六、 Lambda 表达式

![image-20220710195038665](../AppData/Roaming/Typora/typora-user-images/image-20220710195038665.png)

## I. 什么是 Lambda 表达式

什么是 Lambda 表达式呢？维基百科是这样定义的：

> Lambda expression in computer programming, also called an anonymous function, is a defined function not bound to an identifier. ——维基百科

翻译过来就是 Lambda 表达式也叫作匿名函数，是一种是未绑定标识符的函数定义，在编程语言中，匿名函数通常被称为 Lambda 抽象。

换句话说， Lambda 表达式通常是在需要一个函数，但是又不想费神去命名一个函数的场合下使用。这种匿名函数，在 JDK 8 之前是通过 Java 的匿名内部类来实现，从 Java 8 开始则引入了 Lambda 表达式——一种紧凑的、传递行为的方式

## II. 为什么要引入 Lambda 表达式

Java Lambda 表达式是伴随 Java 8 于 2014 年出现的。这个时候恰好是多核 CPU 和大数据兴起的时候。在这些趋势下，芯片设计者只能采用多核并行的设计思路，而软件开发者必须能够更好地利用底层硬件的并发特性。做过多线程编程的同学应该很清楚，在并发过程中涉及锁相关的编程算法不但容易出错，而且耗时费力。虽然 Java 提供了 `java.util.concurrent` 包以及很多第三方类库来帮助我们写出多核 CPU 上运行良好的程序，但在大数据集合的处理上面这些工具包在高效的并行操作上都有些欠缺，我们很难通过简单的修改就能够在多核 CPU 上进行高效的运行。

为了解决上述的问题，需要在程序语言上修改现有的 Java ——增加 Lambda 表达式，同时在 Java 8 也引入Stream（java.util.stream） 流——一个来自数据源的元素队列，支持聚合操作，来提供对大数据集合的处理能力。

所以 Lambda 表达式的出现时为了适应多核 CPU 的大趋势，一方面通过它我们方便的高效的并发程序，通过简单地修改就能编写复杂的集合处理算法。

## III. Lambda 表达式的优点

那么 Lambda 具体有哪些优点呢？

1. **更加紧凑的代码**： Lambda 表达式可以通过省去冗余代码来减少我们的代码量，增加我们代码的可读性；
2. **更好地支持多核处理**： Java 8 中通过 Lambda 表达式可以很方便地并行操作大集合，充分发挥多核 CPU 的潜能，并行处理函数如 filter、map 和 reduce；
3. **改善我们的集合操作**： Java 8 引入 Stream API，可以将大数据处理常用的 map、reduce、filter 这样的基本函数式编程的概念与 Java 集合结合起来。方便我们进行大数据处理

## IV、入门案例

```java
package com.itshihao;

/**
 * 无返回值，无参数
 */
@FunctionalInterface
interface NoReturnNoParam{
    void method();
}

/**
 * 无返回值，有一个参数
 */
@FunctionalInterface
interface NoReturnOneParam{
    void method(int a);
}

/**
 * 无返回值，有多个参数
 */
@FunctionalInterface
interface NoReturnMultiParam{
    void method(int a, int b);
}

/**
 * 有返回值，无参数
 */
interface ReturnNoParam{
    int method();
}

/**
 * 有返回值，有一个参数
 */
@FunctionalInterface
interface ReturnOneParam{
    int method(int a);
}

/**
 * 有返回值，有多个参数
 */
interface ReturnMultiParam{
    int method(int a, int b);
}


public class Test {
    public static void main(String[] args) {
        /**
         * 无返回值，无参数
         */
        NoReturnNoParam noReturnNoParam = () -> {
            System.out.println("NoReturnNoParam ");
        };
        noReturnNoParam.method();

        /**
         * 无返回值，有一个参数
         */
        NoReturnOneParam noReturnOneParam = (int a) -> {
            System.out.println("NoReturnOneParam " + a);
        };
        noReturnOneParam.method(10);

        /**
         * 无返回值，有多个参数
         */
        NoReturnMultiParam noReturnMultiParam = (int a,int b) ->{
            System.out.println("NoReturnMultiParam " + (a + b));
        };
        noReturnMultiParam.method(10,20);

        /**
         * 有返回值，无参数
         */
        ReturnNoParam returnNoParam = () -> {
            System.out.print("ReturnNoParam ");
            return 10;
        };
        System.out.println(returnNoParam.method());

        /**
         * 有返回值，有一个参数
         */
        ReturnOneParam returnOneParam = (int a) ->{
            System.out.print("ReturnOneParam ");
            return a;
        };
        System.out.println(returnOneParam.method(20));

        /**
         * 有返回值，有多个参数
         */
        ReturnMultiParam returnMultiParam = (int a, int b) -> {
            System.out.print("ReturnMultiParam ");
            return a+b;
        };
        System.out.println(returnMultiParam.method(20, 30));
    }
}
/* 	NoReturnNoParam 
	NoReturnOneParam 10
	NoReturnMultiParam 30
	ReturnNoParam 10
	ReturnOneParam 20
	ReturnMultiParam 50
	*/
```

### 简化后

```java
package com.itshihao;

/**
 * 无返回值，无参数
 */
@FunctionalInterface
interface NoReturnNoParam{
    void method();
}

/**
 * 无返回值，有一个参数
 */
@FunctionalInterface
interface NoReturnOneParam{
    void method(int a);
}

/**
 * 无返回值，有多个参数
 */
@FunctionalInterface
interface NoReturnMultiParam{
    void method(int a, int b);
}

/**
 * 有返回值，无参数
 */
interface ReturnNoParam{
    int method();
}

/**
 * 有返回值，有一个参数
 */
@FunctionalInterface
interface ReturnOneParam{
    int method(int a);
}

/**
 * 有返回值，有多个参数
 */
interface ReturnMultiParam{
    int method(int a, int b);
}


public class Test {
    public static void main(String[] args) {
        /**
         * 无返回值，无参数
         */
        /*NoReturnNoParam noReturnNoParam = () -> {
            System.out.println("NoReturnNoParam ");
        };*/
        NoReturnNoParam noReturnNoParam = () -> System.out.println("NoReturnNoParam ");
        noReturnNoParam.method();

        /**
         * 无返回值，有一个参数
         */
        NoReturnOneParam noReturnOneParam = (int a) -> {
            System.out.println("NoReturnOneParam " + a);
        };
        noReturnOneParam.method(10);

        /**
         * 无返回值，有多个参数
         */
        /*NoReturnMultiParam noReturnMultiParam = (int a,int b) ->{
            System.out.println("NoReturnMultiParam " + (a + b));
        };*/
        NoReturnMultiParam noReturnMultiParam = (a,b) -> System.out.println("NoReturnMultiParam " + (a + b));
        noReturnMultiParam.method(10,20);

        /**
         * 有返回值，无参数
         */
        /*ReturnNoParam returnNoParam = () -> {
            System.out.print("ReturnNoParam ");
            return 10;
        };*/
        ReturnNoParam returnNoParam = () ->10;

        System.out.println(returnNoParam.method());

        /**
         * 有返回值，有一个参数
         */
        /*ReturnOneParam returnOneParam = (int a) ->{
            System.out.print("ReturnOneParam ");
            return a;
        };*/
        ReturnOneParam returnOneParam = a -> a;;
        System.out.println(returnOneParam.method(20));

        /**
         * 有返回值，有多个参数
         */
        /*ReturnMultiParam returnMultiParam = (int a, int b) -> {
            System.out.print("ReturnMultiParam ");
            return a+b;
        };*/
        ReturnMultiParam returnMultiParam = (a, b) -> a+b;;
        System.out.println(returnMultiParam.method(20, 30));
    }
}
```

## V、 Lambda 表达式的使用

### 1、 Lambda 表达式引用方法

有时候我们不是必须使用 Lambda 的函数体定义实现，我们可以利用 lambda 表达式指 向一个已经被实现的方法。

#### 1.1语法

方法归属者::方法名 静态方法的归属者为类名，普通方法归属者为对象。

#### 1.2案例

Test类

```java
// 在上述案例中加一个静态方法和一个非静态方法。同时main方法中实现静态方法
public static void main(String[] args){
		ReturnOneParam returnOneParam1 = a -> doubleNum(a);
    	// ReturnOneParam returnOneParam1 = Test::doubleNum; 也可以这样
        int method = returnOneParam1.method(10);
        System.out.println(method);
}

 /**
     * 要求：
     * 1,参数的个数以及类型需要与函数接口中的抽象方法一致。
     * 2,返回值类型要与函数接口中的抽象方法的返回值类型一致
     */
    public static int doubleNum(int a){
        return 2*a;
    }
/**
     * 非静态
     */
    public int addTwo(int a){
        return a+2;
    }
```

Test2类：

```java
public class Test2 {
    public static void main(String[] args) {
        ReturnOneParam returnOneParam1 = Test::doubleNum;
        int method = returnOneParam1.method(10);
        System.out.println(method);

        // 实例化Test类对象
        Test test = new Test();
        ReturnOneParam returnOneParam = test::addTwo;
        int method1 = returnOneParam.method(10);
        System.out.println(method1);
    }
}
```

### 2、 Lambda 表达式创建线程

```java
public class TestThread {
    public static void main(String[] args) {
        System.out.println(Thread.currentThread().getName() + " 开始");
        new Thread(() ->{
            for (int i = 0; i < 20; i++) {
                System.out.println(Thread.currentThread().getName() + i);
                try {
                    Thread.sleep(500);
                } catch (InterruptedException e) {
                    e.printStackTrace();
                }
            }
        }," Lambda Thread").start();
        System.out.println(Thread.currentThread().getName() + " 结束");
    }
}
```

### 3 、操作集合

#### 	3.1遍历集合

​		我们可以调用集合的 public void forEach(Consumer action) 方法，通过 lambda 表达式的方式遍历集合中的元素。以下是 Consumer 接口的方法以及遍历集合的操 作。Consumer 接口是 jdk 为我们提供的一个函数式接口。

```java
public class TestList {
    public static void main(String[] args) {
        List<String> list = new ArrayList<>();
        list.add("a");
        list.add("b");
        list.add("c");
        list.add("d");
        list.forEach(System.out::println);
    }
}
```

#### 3.2删除集合中的元素

我们通过 public boolean removeIf(Predicate filter)方法来删除集合中的某个元 素，Predicate 也是 jdk 为我们提供的一个函数式接口，可以简化程序的编写。

```java
public class TestListRemoveIf {
    public static void main(String[] args) {
        List<String> list = new ArrayList<>();
        list.add("a");
        list.add("b");
        list.add("c");
        list.add("d");
        list.removeIf(ele->ele.equals("b"));
        list.forEach(System.out::println);
    }
}
```

#### 3.3元素排序

之前我们若要为集合内的元素排序，就必须调用 sort 方法;

传入比较器重写 compare 方法的比较器对象;

现在我们还可以使用 lambda 表达式来简化代码



**重写compara方法的比较器对象案例：**

```java
class ComparatorImpl implements Comparator<String>{

    @Override
    public int compare(String o1, String o2) {
        return o1.compareTo(o2);
    }
}
public class TestSort {
    public static void main(String[] args) {
        List<String> list = new ArrayList<>();
        list.add("a");
        list.add("c");
        list.add("d");
        list.add("b");
        list.sort(new ComparatorImpl());
        list.forEach(System.out::println);

    }
}
```

**使用** **lambda** **表达式来简化代码**

```java
public class TestSort {
    public static void main(String[] args) {
        List<String> list = new ArrayList<>();
        list.add("a");
        list.add("c");
        list.add("d");
        list.add("b");
        list.sort(((o1, o2) -> o1.compareTo(o2)));
        list.forEach(System.out::println);

    }
}
```

## 4、 Lambda 表达式中的闭包问题

### 4.1什么是闭包

闭包的本质就是代码片断。所以闭包可以理解成一个代码片断的引用。在 Java 中匿名 18 内部类也是闭包的一种实现方式。 在闭包中访问外部的变量时，外部变量必须是 final 类型，虚拟机会帮饰关键字。

```java
public class TestClosePacket {
    public static void main(String[] args) {
        final int num = 10;
        NoReturnNoParam noReturnNoParam = new NoReturnNoParam() {
            @Override
            public void method() {
                System.out.println(num); // 在闭包中，此num值不可改变，在编译过程中，jvm会自动在int前加上final关键字
            }
        };
        noReturnNoParam.method();
    }
}
```

简化后：

```java
public class TestClosePacket {
    public static void main(String[] args) {
        final int num = 10;
        NoReturnNoParam noReturnNoParam = () -> System.out.println(num); 
        // 在闭包中，此num值不可改变，在编译过程中，jvm会自动在int前加上final关键字
        noReturnNoParam.method();
    }
}
```











