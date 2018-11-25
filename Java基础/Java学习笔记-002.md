# <font color=DodgerBlue>[Java学习笔记-002]：回调</font>

#### （1）什么是回调

所谓回调：就是A类中调用B类中的某个方法C，然后B类中反过来调用A类中的方法D，D这个方法就叫回调方法。

#### （2）代码实现



```java
public class SuperCalculator
{
    public void add(int a, int b, Student  xiaoming)
    {
        int result = a + b;
        xiaoming.fillBlank(a, b, result);
    }
}

public class Student
{
    private String name = null;

    public Student(String name)
    {
        this.name = name;
    }
    
    public void setName(String name)
    {
        this.name = name;
    }
    
    public void callHelp (int a, int b)
    {
        new SuperCalculator().add(a, b, this);
    }
    
    public void fillBlank(int a, int b, int result)
    {
        System.out.println(name + "求助小红计算:" + a + " + " + b + " = " + result);
    }
}

public class Test
{
    public static void main(String[] args)
    {
        int a = 26549;
        int b = 16487;
        Student s = new Student("小明");
        s.callHelp(a, b);
    }
}
```

