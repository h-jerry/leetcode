## 题目地址

 https://leetcode-cn.com/problems/duplicate-emails/ 

## 题目描述

```
编写一个 SQL 查询，查找 Person 表中所有重复的电子邮箱。

示例：

+----+---------+
| Id | Email   |
+----+---------+
| 1  | a@b.com |
| 2  | c@d.com |
| 3  | a@b.com |
+----+---------+
根据以上输入，你的查询应返回以下结果：

+---------+
| Email   |
+---------+
| a@b.com |
+---------+
说明：所有电子邮箱都是小写字母。

来源：力扣（LeetCode）
链接：https://leetcode-cn.com/problems/duplicate-emails
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。
```

## 思路

> 止题比较简单，通过Email字段分组并筛选出数量大于1即可
> 
>```java
> select Email from Person group by Email having count(Email)>1
> ```

## 执行结果

