##### 1.在pom.xml添加依赖

~~~xml
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
  <modelVersion>4.0.0</modelVersion>
  <groupId>com.atguigu</groupId>
  <artifactId>atcrowdfunding-parent</artifactId>
  <version>0.0.1-SNAPSHOT</version>
  <packaging>pom</packaging>
  
<dependencies>                                                              
    <dependency>                                                            
        <groupId>javax.servlet</groupId>                        
        <artifactId>servlet-api</artifactId>                          
        <version>2.5</version>                              
    </dependency>                                                           
    <dependency>                                                            
        <groupId>javax.servlet.jsp</groupId>                        
        <artifactId>jsp-api</artifactId>                       
        <version>2.1.3-b06</version>                              
    </dependency>                                                           
    <dependency>                                                            
        <groupId>org.springframework</groupId>                        
        <artifactId>spring-core</artifactId>                          
        <version>4.0.0.RELEASE</version>                              
    </dependency>                                                           
    <dependency>                                                            
        <groupId>org.springframework</groupId>                        
        <artifactId>spring-context</artifactId>                       
        <version>4.0.0.RELEASE</version>                              
    </dependency>                                                           
    <dependency>                                                            
        <groupId>org.springframework</groupId>                        
        <artifactId>spring-jdbc</artifactId>                          
        <version>4.0.0.RELEASE</version>                              
    </dependency>                                                           
    <dependency>                                                            
        <groupId>org.springframework</groupId>                        
        <artifactId>spring-orm</artifactId>                           
        <version>4.0.0.RELEASE</version>                              
    </dependency>                                                           
    <dependency>                                                            
        <groupId>org.springframework</groupId>                        
        <artifactId>spring-web</artifactId>                           
        <version>4.0.0.RELEASE</version>                              
    </dependency>                                                           
    <dependency>                                                            
        <groupId>org.springframework</groupId>                        
        <artifactId>spring-webmvc</artifactId>                        
        <version>4.0.0.RELEASE</version>                              
    </dependency>                                                           
    <dependency>                                                            
        <groupId>com.mchange</groupId>                                
        <artifactId>c3p0</artifactId>                                 
        <version>0.9.2</version>                                      
    </dependency>                                                           
    <dependency>                                                            
        <groupId>cglib</groupId>                                      
        <artifactId>cglib</artifactId>                                
        <version>2.2</version>                                        
    </dependency>                                                           
    <dependency>                                                            
        <groupId>org.aspectj</groupId>                                
        <artifactId>aspectjweaver</artifactId>                        
        <version>1.6.8</version>                                      
    </dependency>                                                           
                                                                                  
    <!-- Spring整合MyBatis -->                                              
    <!-- MyBatis中延迟加载需要使用Cglib -->                                 
    <!-- https://mvnrepository.com/artifact/org.mybatis/mybatis -->         
    <dependency>                                                            
        <groupId>org.mybatis</groupId>                                
        <artifactId>mybatis</artifactId>                              
        <version>3.2.8</version>                                      
    </dependency>                                                           
                                                                                  
    <dependency>                                                            
        <groupId>org.mybatis</groupId>                                
        <artifactId>mybatis-spring</artifactId>                       
        <version>1.2.2</version>                                      
    </dependency>                                                           
                                                                                  
    <!-- 控制日志输出：结合log4j -->                                        
    <dependency>                                                            
        <groupId>log4j</groupId>                                      
        <artifactId>log4j</artifactId>                                
        <version>1.2.17</version>                                     
    </dependency>                                                           
    <dependency>                                                            
        <groupId>org.slf4j</groupId>                                  
        <artifactId>slf4j-api</artifactId>                            
        <version>1.7.7</version>                                      
    </dependency>                                                           
    <dependency>                                                            
        <groupId>org.slf4j</groupId>                                  
        <artifactId>slf4j-log4j12</artifactId>                        
        <version>1.7.7</version>                                      
    </dependency>                                                           
                                                                                  
    <dependency>                                                            
        <groupId>mysql</groupId>                                      
        <artifactId>mysql-connector-java</artifactId>                 
        <version>5.1.37</version>                                     
    </dependency>                                                           
    <dependency>                                                            
        <groupId>jstl</groupId>                                       
        <artifactId>jstl</artifactId>                                 
        <version>1.2</version>                                        
    </dependency>                                                           
                                                                                  
    <!-- ********其他****************************** -->                     
                                                                                  
    <!-- Ehcache二级缓存 -->                                                
    <dependency>                                                            
        <groupId>net.sf.ehcache</groupId>                             
        <artifactId>ehcache</artifactId>                              
        <version>1.6.2</version>                                      
    </dependency>                                                           
                                                                                  
                                                                                  
    <!-- 石英调度 - 开始 -->                                                
    <dependency>                                                            
        <groupId>org.quartz-scheduler</groupId>                       
        <artifactId>quartz</artifactId>                               
        <version>1.8.5</version>                                      
    </dependency>                                                           
    <dependency>                                                            
        <groupId>org.springframework</groupId>                        
        <artifactId>spring-context-support</artifactId>               
        <version>4.0.0.RELEASE</version>                              
    </dependency>                                                           
    <dependency>                                                            
        <groupId>commons-collections</groupId>                        
        <artifactId>commons-collections</artifactId>                  
        <version>3.1</version>                                        
    </dependency>                                                           
    <!-- 石英调度 - 结束 -->                                                
                                                                                  
    <dependency>                                                            
        <groupId>org.codehaus.jackson</groupId>                       
        <artifactId>jackson-mapper-asl</artifactId>                   
        <version>1.9.2</version>                                      
    </dependency>                                                           
                                                                                  
    <dependency>                                                            
        <groupId>org.apache.poi</groupId>                             
        <artifactId>poi</artifactId>                                  
        <version>3.9</version>                                        
    </dependency>                                                           
                                                                                  
    <dependency>                                                            
        <groupId>org.jfree</groupId>                                  
        <artifactId>jfreechart</artifactId>                           
        <version>1.0.19</version>                                     
    </dependency>                                                           
                                                                                  
    <dependency>                                                            
        <groupId>commons-fileupload</groupId>                         
        <artifactId>commons-fileupload</artifactId>                   
        <version>1.3.1</version>                                      
    </dependency>                                                           
                                                                                  
    <dependency>                                                            
        <groupId>org.freemarker</groupId>                             
        <artifactId>freemarker</artifactId>                           
        <version>2.3.19</version>                                     
    </dependency>                                                           
                                                                                  
    <dependency>                                                            
        <groupId>org.activiti</groupId>                               
        <artifactId>activiti-engine</artifactId>                      
        <version>5.15.1</version>                                     
    </dependency>                                                           
                                                                                  
    <dependency>                                                            
        <groupId>org.activiti</groupId>                               
        <artifactId>activiti-spring</artifactId>                      
        <version>5.15.1</version>                                     
    </dependency>                                                           
                                                                                  
    <dependency>                                                            
        <groupId>org.apache.commons</groupId>                         
        <artifactId>commons-email</artifactId>                        
        <version>1.3.1</version>                                      
    </dependency>                                                           
                                                                                  
    <dependency>                                                            
        <groupId>org.activiti</groupId>                               
        <artifactId>activiti-explorer</artifactId>                    
        <version>5.15.1</version>                                     
        <exclusions>                                                        
            <exclusion>                                                     
                <artifactId>groovy-all</artifactId>                   
                <groupId>org.codehaus.groovy</groupId>                
            </exclusion>                                                    
        </exclusions>                                                       
    </dependency>                                                           
</dependencies> 
</project>
~~~

##### 2.在web.xml中添加配置信息

~~~xml
<?xml version="1.0" encoding="UTF-8"?>
<web-app xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://java.sun.com/xml/ns/javaee" xsi:schemaLocation="http://java.sun.com/xml/ns/javaee http://java.sun.com/xml/ns/javaee/web-app_2_5.xsd" id="WebApp_ID" version="2.5">
    <context-param>
        <param-name>contextConfigLocation</param-name>
        <param-value>classpath*:spring/spring-*.xml</param-value>
    </context-param>
    <listener>
        <listener-class>org.springframework.web.context.ContextLoaderListener</listener-class>
    </listener>
    
    <listener>
        <listener-class>com.atguigu.atcrowdfunding.web.ServerStartupListener</listener-class>
    </listener>
    
    <filter>
        <filter-name>encoding</filter-name>
        <filter-class>org.springframework.web.filter.CharacterEncodingFilter</filter-class>
        <init-param>
            <param-name>encoding</param-name>
            <param-value>UTF-8</param-value>
        </init-param>
        <init-param>
            <param-name>forceEncoding</param-name>
            <param-value>true</param-value>
        </init-param>
    </filter>
    
    <filter-mapping>
        <filter-name>encoding</filter-name>
        <servlet-name>springmvc</servlet-name>
    </filter-mapping>
    
    <servlet>
        <servlet-name>springmvc</servlet-name>
        <servlet-class>org.springframework.web.servlet.DispatcherServlet</servlet-class>
        <init-param>
            <param-name>contextConfigLocation</param-name>
            <param-value>classpath:spring/springmvc-context.xml</param-value>
        </init-param>
        <load-on-startup>1</load-on-startup>
    </servlet>
    <servlet-mapping>
        <servlet-name>springmvc</servlet-name>
        <url-pattern>/</url-pattern>
    </servlet-mapping>
</web-app>
~~~

#####3.新建三个配置文件，目录如下

![image-20181202011621536](https://ws4.sinaimg.cn/large/006tNbRwgy1fxrr0f2yhqj30jo0emgnd.jpg)

（1）config.xml

~~~xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE configuration PUBLIC "-//mybatis.org//DTD Config 3.0//EN" "http://mybatis.org/dtd/mybatis-3-config.dtd">
<configuration>
    <typeAliases>
        
    </typeAliases>
</configuration>
~~~

（2）spring-context.xml

~~~xml
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xmlns:context="http://www.springframework.org/schema/context"
    xmlns:tx="http://www.springframework.org/schema/tx"
    xmlns:aop="http://www.springframework.org/schema/aop"
    xsi:schemaLocation="http://www.springframework.org/schema/aop http://www.springframework.org/schema/aop/spring-aop-4.0.xsd
        http://www.springframework.org/schema/beans http://www.springframework.org/schema/beans/spring-beans.xsd
        http://www.springframework.org/schema/tx http://www.springframework.org/schema/tx/spring-tx-4.0.xsd
        http://www.springframework.org/schema/context http://www.springframework.org/schema/context/spring-context-4.0.xsd">
    <!-- Controller不由spring管理 -->
    <context:component-scan base-package="com.rbac.*" >
        <context:exclude-filter type="annotation" expression="org.springframework.stereotype.Controller"/>
    </context:component-scan>
    <!-- 数据库配置 -->
    <bean id="dataSource" class="com.mchange.v2.c3p0.ComboPooledDataSource" >
        <property name="driverClass" value="com.mysql.jdbc.Driver"/>
        <property name="jdbcUrl" value="jdbc:mysql://localhost:3306/rbac?rewriteBatchedStatements=true&amp;useUnicode=true&amp;characterEncoding=utf8"/>
        <property name="user" value="root"/>
        <property name="password" value="Aa141280"/>
    </bean>
    <!-- Mybatis映射文件 -->
    <bean id="sqlSessionFactory" class="org.mybatis.spring.SqlSessionFactoryBean" >
        <property name="configLocation" value="classpath:mybatis/config.xml" />
        <property name="dataSource" ref="dataSource" />
        <property name="mapperLocations" >
            <list>
                <value>classpath*:mybatis/mapper-*.xml</value>
            </list>
        </property>
    </bean>
    
    <bean id="mapperScannerConfigurer" class="org.mybatis.spring.mapper.MapperScannerConfigurer" >
        <property name="basePackage" value="com.rbac.dao" />
    </bean>
    
    <!-- 声明事务 -->
    <bean id="transactionManager" class="org.springframework.jdbc.datasource.DataSourceTransactionManager" >
        <property name="dataSource" ref="dataSource"/>
    </bean>
    <tx:advice id="transactionAdvice" transaction-manager="transactionManager" >
        <tx:attributes>
            <tx:method name="*" propagation="REQUIRED" isolation="DEFAULT" rollback-for="java.lang.Exception" />
            <tx:method name="query*" read-only="true" />
        </tx:attributes>
    </tx:advice>    
    <aop:config>
        <aop:advisor advice-ref="transactionAdvice" pointcut="execution(* com.rbac.service.*.*(..))"/>
    </aop:config>
 </beans>
~~~

（3）springmvc-context.xml

~~~xml
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
	xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xmlns:context="http://www.springframework.org/schema/context"
	xmlns:p="http://www.springframework.org/schema/p"
	xmlns:mvc="http://www.springframework.org/schema/mvc"
	xsi:schemaLocation="http://www.springframework.org/schema/mvc http://www.springframework.org/schema/mvc/spring-mvc-4.0.xsd
		http://www.springframework.org/schema/beans http://www.springframework.org/schema/beans/spring-beans.xsd
		http://www.springframework.org/schema/context http://www.springframework.org/schema/context/spring-context-4.0.xsd">
    <!-- 扫描base-package下的Controller -->
    <context:component-scan base-package="com.rbac.*" use-default-filters="false" >
        <context:include-filter type="annotation" expression="org.springframework.stereotype.Controller"/>
    </context:component-scan>
    <!-- 不拦截静态资源 -->
    <mvc:default-servlet-handler/>
    <mvc:annotation-driven />
    <!-- 配置视图解析器，页面跳转 -->
    <bean class="org.springframework.web.servlet.view.InternalResourceViewResolver" >
        <property name="viewClass" value="org.springframework.web.servlet.view.JstlView"/>
        <property name="prefix" value="/WEB-INF/jsp/"/>
        <property name="suffix" value=".jsp"/>
    </bean>
    <!-- json数据 -->
    <bean class="org.springframework.web.servlet.mvc.annotation.AnnotationMethodHandlerAdapter" >
        <property name="messageConverters" >
            <list>
                <bean class="org.springframework.http.converter.json.MappingJacksonHttpMessageConverter" >
                    <property name="supportedMediaTypes" >
                        <list>
                            <value>application/json;charset=UTF-8</value>
                        </list>
                    </property>
                </bean>
            </list>
        </property>
    </bean>
    <!-- 文件上传 -->
    <bean id="multipartResolver" class="org.springframework.web.multipart.commons.CommonsMultipartResolver" p:defaultEncoding="UTF-8" >
        <property name="maxUploadSize" value="2097152"/>
        <property name="resolveLazily" value="true"/>
    </bean>
</beans>
~~~

