Session没有关闭的情况下，通过在PersistenceContext的对象状态，然后重新获取连接取lazzy的值；   
![](https://github.com/zhangzhenhuajack/spring-data-jpa-guide/blob/master/images/entity_lazy/1.png)   

lazy加载过程 :参考：https://cloud.tencent.com/developer/news/311577      

将所有集合类类初始化如下形式：  
![](https://github.com/zhangzhenhuajack/spring-data-jpa-guide/blob/master/images/entity_lazy/2.png)   

把Session喂进去   
![](https://github.com/zhangzhenhuajack/spring-data-jpa-guide/blob/master/images/entity_lazy/3.png)   
具体session里面的内容如下：   
![](https://github.com/zhangzhenhuajack/spring-data-jpa-guide/blob/master/images/entity_lazy/4.png)    
自定义了一套PersistentCollection类   
![](https://github.com/zhangzhenhuajack/spring-data-jpa-guide/blob/master/images/entity_lazy/5.png)   
继承List   
![](https://github.com/zhangzhenhuajack/spring-data-jpa-guide/blob/master/images/entity_lazy/6.png)   
覆盖一些List的方法通过read()来读数据；   
![](https://github.com/zhangzhenhuajack/spring-data-jpa-guide/blob/master/images/entity_lazy/7.png)   
