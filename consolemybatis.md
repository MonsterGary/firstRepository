eclipse 创建mybatis-config.xml、mapper.xml文件===https://blog.csdn.net/qq_21202769/article/details/87035933


<!-- Mybatis提供的标准日志输出 -->
<?xml version="1.0" encoding="utf-8"?>
<!DOCTYPE configuration PUBLIC "-//mybatis.org//DTD Config 3.0//EN" "http://mybatis.org/dtd/mybatis-3-config.dtd">

<configuration>

  <settings>        
     <setting name="defaultExecutorType" value="REUSE" />
     <!-- 配置控制台输出 -->
     <setting name="logImpl" value="STDOUT_LOGGING"/>  
  </settings>

  <typeAliases>

  </typeAliases>

</configuration>
————————————————
版权声明：本文为CSDN博主「狂飙的yellowcong」的原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/yelllowcong/article/details/78818825


mybatis 通过log4j
    <settings>
        <!-- 开启log4j来记录日志 -->
        <setting name="logImpl" value="log4j"/>
    </settings>
    那么，我们在log4j.properties中的配置应该是这样：


log4j.rootCategory=error, CONSOLE,LOGFILE
 
# 将selectAll的错误级别设置为info
log4j.logger.lixin.gan.mapper.FlowerMapper.selectAll=info
 
# 将selectCount的错误级别设置为debug
log4j.logger.lixin.gan.mapper.FlowerMapper.selectCount=debug
 
# 将lixin.gan.mapper.FlowerMapper下面的所有方法（selectAll，selectCount）都设为error
log4j.logger.lixin.gan.mapper.FlowerMapper=error
 
# 将所有mapper中的映射操作都设为error
log4j.logger.lixin.gan.mapper=error
原文https://www.cnblogs.com/-beyond/p/10113455.html

mybatis整合log4j打印sql语句https://www.jianshu.com/p/9bc00ca882e1


　　
