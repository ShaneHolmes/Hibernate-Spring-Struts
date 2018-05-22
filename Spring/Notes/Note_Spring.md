# Spring框架

* * *
## 1 Spring概述
	开源，轻量级框架（轻量级：与EJB--Enterprise Java Beans对比，依赖资源少，销毁的资源少）
	spring的核心是IoC（控制反转）和AOP(面向切面).
- [ ] 分层架构（一站式，每一层都提供解决方案）：
![框架结构图](https://github.com/ShaneHolmes/Hibernate-Spring-Struts/blob/master/Spring/Images/structure.png)
- web层：struts，spring-MVC
- service层：spring
- dao层：hibernate，mybatis，jdbcTemplate

  spring的<font color=red>核心</font>
  
- **IoC(控制反转)**Inverse of Control：
- **AOP(面向切面)**：
- [ ] spring优点：
- **高内聚，低耦合**：Spring就是一个大工厂（容器），可以将所有对象创建和依赖关系维护，交给Spring管理。spring工厂是用于生成bean
- **AOP编程的支持**：Spring提供面向切面编程，可以对程序进行权限拦截，运行监控等功能
- **声明式事物编程**：只需要通过配置就可以完成对事物的管理，无需手动编程
- **方便的程序测试**：支持Junit4
- **方便集成各种优秀的框架**：spring不排斥各种优秀的框架，内部提供了对（Struts，Hibernate，MyBatis等）的直接支持
- **对API封装**
## 入门案例：IoC
- [ ] **在lib导入jar包**：4+1：4个核心（beans、core、context、expression）+1个依赖（commons-loggins...jar）
- [ ] 目标类
- 提供UserService接口和实现类
- 获得UserService实现类的实例
之前开发中，直接new一个对象即可。学习spring之后，将由Spring创建对象实例--> IoC 控制反转（Inverse of  Control）之后需要实例对象时，从spring工厂（容器）中获得，需要将实现类的全限定名称配置到xml文件中
```
public interface UserService {
	public void addUser();
}
```
```
public class UserServiceImpl implements UserService {
	@Override
	public void addUser() {
		System.out.println("a_ico add user");
	}

}
```
