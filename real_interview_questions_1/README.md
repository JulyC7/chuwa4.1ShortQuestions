## Interview Questions:

# 1. java8 features (functional, lamda, function interface, async, （超级大重点9）



stream: https://www.baeldung.com/java-8-streams-introduction

lambda expression and functional interface :https://www.baeldung.com/java-8-lambda-expressions-tips

interface default and static method: https://www.baeldung.com/java-8-new-features


# 2. Rest design, url, methods. 

啥意思？

# 3. right view of tree (其实就是让你设计一套API，考你命名规范的。可以尝试设计一个vendor machine)

咋做？


## Interview Questions:
## 1.What is the Springboot?
https://www.tutorialspoint.com/spring_boot/spring_boot_introduction.htm

Spring Boot is an open source Java-based framework used to create a micro Service. It is developed by Pivotal Team and is used to build stand-alone and production ready spring applications.

### What is Spring Boot?

Spring Boot provides a good platform for Java developers to develop a stand-alone and production-grade spring application that you can just run. You can get started with minimum configurations without the need for an entire Spring configuration setup.

### Advantages

Spring Boot offers the following advantages to its developers −

Easy to understand and develop spring applications
Increases productivity
Reduces the development time
Goals
Spring Boot is designed with the following goals −

To avoid complex XML configuration in Spring
To develop a production ready Spring applications in an easier way
To reduce the development time and run the application independently
Offer an easier way of getting started with the application




## 2.Bean scope in spring （重点9）



https://www.tutorialspoint.com/spring/spring_bean_scopes.htm

https://www.baeldung.com/spring-bean-scopes



## 3.What is the singleton pattern? How to implement it? And When to use it? （重点9）

singleton pattern https://www.geeksforgeeks.org/singleton-design-pattern-introduction/?ref=lbp

singleton pattern in spring boot : https://baeldung-cn.com/spring-framework-design-patterns



## 4. What is the result in the console?

```java 
class Operation{ 

Int data;

void change(int data){ 

 data=data+100;//changes will be in the local variable only 

 } 

public static void main(String args[]){ 

Operation op=new Operation(); 

System.out.println("before change "+op.data); 

op.change(500); 

System.out.println("after change "+op.data); 

} 

}
```

before change 0 
after change 0

## 5. Given the string, find the maximum number in the this string and return it
Example: ajnfjn100jnvjnf400jnjnjn


```java 
public class Main {
    public static void main(String[] args) {
        String input="ajnfjn100jnvjnf400jnjnjn";

        System.out.println(input);
        
        int max_num=0;
        int num=0;
        for (int i=0;i<input.length();i++){
            
            //System.out.println(i+","+input.charAt(i));
            if (Character.isDigit(input.charAt(i))){
                num=num*10+(input.charAt(i)-'0');
            }
            
            if (Character.isAlphabetic(input.charAt(i))){
                max_num=Math.max(num,max_num);
                num=0;
            }
            
        }
        return max_num;
        //System.out.println(max_num);
    }
}
```
