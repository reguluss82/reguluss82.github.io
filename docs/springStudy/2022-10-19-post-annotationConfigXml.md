---
layout: default
title: "annotation config bean 사용"
parent: SpringStudy
---

# annotation-config
{: .no_toc }

MainClass
```java
package DI08;

import org.springframework.context.support.AbstractApplicationContext;
import org.springframework.context.support.GenericXmlApplicationContext;

public class MainClass08 {

	public static void main(String[] args) {
		AbstractApplicationContext ctx = new GenericXmlApplicationContext("classpath:applicationCTX08.xml");
		// annotation
		Student student1 = ctx.getBean("student1" , Student.class);
		System.out.println("이름 : "   + student1.getName());
		System.out.println("나이 : "   + student1.getAge());
		System.out.println("취미 : "   + student1.getHobbys());
		System.out.println("신장 : "   + student1.getHeigth());
		System.out.println("몸무게 : " + student1.getWeight());
		// XML
		Student student2 = ctx.getBean("student2" , Student.class);
		System.out.println("이름 : "   + student2.getName());
		System.out.println("나이 : "   + student2.getAge());
		System.out.println("취미 : "   + student2.getHobbys());
		System.out.println("신장 : "   + student2.getHeigth());
		System.out.println("몸무게 : " + student2.getWeight());
		
		ctx.close();

	}

}

```

Student Class
```java
package DI08;

import java.util.ArrayList;

public class Student {
	private String name;
	private int    age;
	private ArrayList<String> hobbys;
	private double weight;
	private double heigth;
	
	public Student(String name , int age , ArrayList<String> hobbys) {
		this.name   = name;
		this.age    = age;
		this.hobbys = hobbys;
	}

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

	public ArrayList<String> getHobbys() {
		return hobbys;
	}

	public void setHobbys(ArrayList<String> hobbys) {
		this.hobbys = hobbys;
	}

	public double getWeight() {
		return weight;
	}

	public void setWeight(double weight) {
		this.weight = weight;
	}

	public double getHeigth() {
		return heigth;
	}

	public void setHeigth(double heigth) {
		this.heigth = heigth;
	}
	
}

```
ApplicationConfig
```java
package DI08;

import java.util.ArrayList;

import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;

@Configuration
public class ApplicationConfig {
	@Bean
	public Student student1() {
		ArrayList<String> hobbys = new ArrayList<String>();
		hobbys.add("수영");
		hobbys.add("물내리기");
		
		Student student = new Student("을지문덕", 55, hobbys);
		student.setHeigth(170);
		student.setWeight(70);
		
		return student;
	}
}

```

context:annotation-config 위한 xml
```
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
	xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xmlns:context="http://www.springframework.org/schema/context"
	xsi:schemaLocation="http://www.springframework.org/schema/beans http://www.springframework.org/schema/beans/spring-beans.xsd
		http://www.springframework.org/schema/context http://www.springframework.org/schema/context/spring-context-4.1.xsd">

	<context:annotation-config/>
	<bean class="DI08.ApplicationConfig"></bean>
	
	<bean id="student2" class="DI08.Student">
		<constructor-arg value="양만춘"></constructor-arg>
		<constructor-arg value="30"></constructor-arg>
		<constructor-arg>
			<list>
				<value>활쏘기</value>
				<value>안시성</value>
			</list>
		</constructor-arg>
		<property name="heigth" value="175"/>
		<property name="weight" value="70"/>
	</bean>
	
</beans>
```