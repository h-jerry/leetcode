## 题目地址

 https://leetcode-cn.com/problems/height-checker/ 

## 题目描述

```
学校在拍年度纪念照时，一般要求学生按照 非递减 的高度顺序排列。

请你返回至少有多少个学生没有站在正确位置数量。该人数指的是：能让所有学生以 非递减 高度排列的必要移动人数。

 

示例：

输入：[1,1,4,2,1,3]
输出：3
解释：
高度为 4、3 和最后一个 1 的学生，没有站在正确的位置。

来源：力扣（LeetCode）
链接：https://leetcode-cn.com/problems/height-checker
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。
```

## 思路

> 1. 根据题意可以得知，需要求得的值就是把数组排序之后，相同下标的值是否一样，不一样就表示移动过
>
> 这样，代码如下：
>
> ```java
> public boolean judgeCircle(String moves) {
>      int x=0,y=0;
>      char[] chars = moves.toCharArray();
>      for (int i = 0; i < chars.length; i++) {
>          if (chars[i]=='R'){
>              x++;
>          }
>          else if (chars[i]=='L'){
>              x--;
>          }
>          else if (chars[i]=='U'){
>              y++;
>          }
>          else if (chars[i]=='D'){
>              y--;
>          }
>      }
>      
>          return x==0 && y==0;
>      
>  }
> ```

## 执行结果

