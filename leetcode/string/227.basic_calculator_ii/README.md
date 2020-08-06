# [227. Basic Calculator II](https://leetcode.com/problems/basic-calculator-ii/)

此算法的思路很简单，先把乘除法的值计算出来，最终将所有的运算简化成只有加法。

注意跳过空格

出现了数字则记录整个数字是多少，然后根据之前的运算符决定下一步：

如果是加号'+'，说明前面的运算独立于以后的运算，可以将结果暂时放入栈；

如果是减号'-'，可以看成-1 * tempNum，然后将-tempNum入栈；

如果是乘号'*'或者除号'/'，由于前面的运算独立于此，可以先计算lastNum和tempNum积，然后结果入栈。

最后将栈中的所有元素相加就是答案。