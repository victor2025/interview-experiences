# 美团面经
- 一面 20220822

### 1. 面经
作者：小王要努力努力再努力
链接：https://www.nowcoder.com/discuss/1023648
来源：牛客网

##### 第一部分：项目
- 1，项目分工
- 2，mysql和redis分别存储的是什么信息，项目的使用场景（单独商家还是像美团这样），项目流量太大怎么办、加redis的目的。
- 3，菜单商品卖完了怎么办，怎么防止菜品超售。
- 4，当两个顾客同时下单，但是菜品只有一份了，该怎么解决？
- 答：互斥锁，超时取消订单。消息队列（无状态，怎么确定是哪个顾客先下的单）、
- 5，分布式锁有哪些，怎么实现（synchronized，ReentrantLock）
- 答：synchronized，ReentrantLock这些是线程方面的，
- 6，RPC的实现
- 7，使用的序列化方式，其他的序列化方式。
- 8，其他的RPC框架
- 跨语言和非跨语言，
- 9，springcloud的底层序列化方式
- 10，zookeeper怎么保证节点的选举
- 11，除了Netty作为通信协议，还有其他方式吗（JDK自带通信的协议可以吗）
##### 第二部分：算法
- 二叉树的层序遍历
- 为啥使用ArrayDeque这种双端队列结构，单端队列可以吗，双端队列的特点。
##### 第三部分：简历上基础知识考查（技能）；
1，ArrayList往第一个位置上插入元素，后续元素要怎么操作。
- 2，除了简历上的消息队列，还用过哪些消息队列、kafka用过没有。
- 3，两个服务（线程）A,B如何保证其有序执行，这两个服务可能来自不同的服务器。
- 答：分布式锁、版本号、
- 4，JDK动态代理的实现接口invocationHandler
- 5，spring种的AOP怎么理解的（JDK动态代理、cgliab动态代理）、cgliab的底层实现原理
- 6，对字节码了解吗
- 7，Map类型有哪些（安全、非安全）、List类型有哪些。
- 8，JVM内存模型
- 9，什么情况会发生oom，发生oom时，gc是如何操作的。
- 10，mysql的底层索引结构。
##### 第四部分：反问
- 部门技术栈

---

### 2. 面经
作者：yes的练级攻略
链接：https://www.nowcoder.com/discuss/1024221
来源：牛客网

#### 计算机网络类
- 为什么要三次握手，四次挥手
- 客户端挂了的话，后续流程怎么处理
- tcp状态码之4xx 和5xx
- seesion 存在于哪里？ 说说cookie 和 token
#### Java 基础类
- hashcode 和 equals ，对象相等 hashcode 一定相等吗？
- final finilize finally
- BIO AIO NIO 区别
- String 为什么不可变
- Integer 默认的范围值
- 集合遍历删除可以吗？
- ArrayList中的数组为什么用transient进行修饰？
- 线程池的退出过程
- 线程池队列已经满了，队列已经满了会怎样
- 单例模式 dcl 的介绍
- synchronized、 aqs、volidate
- cas aba问题
#### JVM
- 服务类变多对整体启动性能的影响有哪些？
- 不会 oom 的区域？
- 内存分配的方式？
- 访问对象的访问方式
- 用过什么垃圾回收器
- 垃圾回收算法有哪些
- 老年代引用新生代，除了 gc root 还用什么？
- 出现以下几种情况的话，说明那里出问题 ？
#### redis
- 为什么用 redis ，优点何在？
- 缓存穿透和缓存雪崩
#### mysql
- 说下表索引执行过程
- 索引怎样会失效？
- 什么情况会走索引？
- 大于或者等于的范围查询一定会使得索引失效吗？
- 说下事务中的二阶段提交
- 说下 change buffer
#### 智力题
- 8个球，有7个一样重，快速找其中的一个
- 两次都是女孩的概率

---

## 3. 面经
作者：herlerrrrrr
链接：https://www.nowcoder.com/discuss/1024177
来源：牛客网

- http状态码
- IO模型
- docker的实现机制
- 虚拟机与docker的区别
- rpc与http
- http3.0特性
- Redis的主从复制
- AOF RDB机制，他问我推荐他选哪种机制，我说我推荐选择RDB+AOF机制，他乐了hhh
- rpc的实现
- 除了grpc（项目里用的）还了解其他的rpc框架吗，他们的优缺点
- MySQL调优

---

## 4. 面经
作者：想成为秋招有满意offer的美女
链接：https://www.nowcoder.com/discuss/1016936
来源：牛客网

- 1.jvm内存的布局
- 2.继续追问哪些内存区域需要进行垃圾收集？
- 3.方法区里面放的什么？
- 4.垃圾回收算法了解哪些？
- 5.为什么要分新生代和老年代？（垃圾回收在新生代频繁，老年代反之，但是面试官和我说的好像说反了，他声音很小我说了嗯嗯，不会让他觉得我说错了吧，害怕）
- 6.栈为什么不需要垃圾回收 ？
- 7.一个变量怎么判断分配在栈还是堆上？int和Integer分别储存在哪里？
- 8.CopyOnWriteArrayList是为了解决什么问题？为什么用了这样数据结构？问了为什么要加锁？加什么锁？
- 9.CopyOnWriteArrayList的底层？
- 10.索引了解吗？说一下知道哪些数据库索引？
- 11.为什么需要数据库的索引？
- 12.那些字段需要加索引哪些不需要？
- 算法：删除链表重复节点（很简单 秒 写了几分钟）写完简单说了一下思路～