# <font color=DodgerBlue>[Java学习笔记-003]：String类常用方法</font>

代码：

```java
package com.java.string;

public class TestString {
	public static void main(String[] args) {
		String str1 = new String("abcd");
		String str2 = new String("abcd");

		System.out.println("[1]:" + str1.charAt(2));
		System.out.println("[2]:" + str2.equals(str1));// 比较内容
		System.out.println("[3]:" + (str1 == str2));// 比较是否是同一个对象

		String str3 = "def";
		String str4 = "def";

		System.out.println("[4]:" + str4.equals(str3));// 比较内容
		System.out.println("[5]:" + (str3 == str4));// 比较是否是同一个对象

		System.out.println("[6]:" + str3.indexOf("y"));
		System.out.println("[7]:" + (str3.substring(1)));// 截取下标1后面的字符串

		String str5 = str3.replace("e", "a");// 替换字符
		System.out.println("[8]:" + str5);

		String str6 = "aaa,bbb,ccc";
		String[] arr = str6.split(",");// 根据逗号切割
		for (int i = 0; i < arr.length; i++) {
			System.out.println("[9]:" + arr[i]);
		}

	}
}

```



结果:

```
[1]:c
[2]:true
[3]:false
[4]:true
[5]:true
[6]:-1
[7]:ef
[8]:daf
[9]:aaa
[9]:bbb
[9]:ccc
```

