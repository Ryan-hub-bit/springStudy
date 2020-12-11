# springStudy

## IOC
控制反转, 控制+ 反转
通过xml 来配置bean, 然后通过IOC容器applicationContext 通过id getbean 来获取相应的bean, 执行相关的操作. 对于每个类的依赖关系我们都写到了xml 文件中, 通过使用@ImportResource("calsspath: spring-config.xml")注解的方式让来加载配置文件.

### 好处
应用程序开发人员不用去手动的new一个新的对象, 这些都交给了Spring 框架. 他会在适当的时候帮助我们创建对象.

### 过程
1. 通过Bean配置信息(注解, xml文件)来读取Bean的配置信息, 然后生成相应的Bean 定义的注册表.
2. 然后通过注册表实例化bean.
3. 然后将bean 的实例放入 spring 容器(bean缓存池)中
4. 当应用程序需要使用到相关的bean 的时候, spring 自动从bean缓存池中取出Bean交由应用程序使用

### Bean 配置信息(need to do some further study)
- Bean的实现类: 通过class = “”来配置
- Bean的属性信息: 数据源的连接数,用户名密码
- Bean的依赖关系: Spring 根据依赖关系配置完成Bean之间的装配
- Bean的行为配置, 生命周期范围以及生命各个过程的回调函数.

### Bean 的命名
ID用来唯一标示一个bean name 是这个bean 的name属性,同样可以通过getbean来获取这个bean, name 可以有分隔 可以通过不同的分隔部分来获取程序.
如果一个bean即没有id 也没有name, 我们可以通过类的全限定名来获取这个bean, 也就是class 后边的那个值.


