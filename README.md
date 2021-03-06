# wangzheng_algo

#### 如课程中所说，在技术圈里，大家都在讨论高大上的架构，鲜少有人关注代码层面的编程能力。

1. 真的愿意做一辈子CRUD boy？

   > 掌握了数据结构与算法，你看待问题的深度，解决问题的角度就会完全不一样。

2. 什么是数据结构？什么是算法？

   > 数据结构和算法是相辅相成，数据结构是为算法服务，算法要作用在特定的数据结构上。

------

- 复杂度分析

  1. 事后统计法的巨大局限性

     > 测试结果非常依赖测试环境， 受数据规模的影响很大。

  2. 大O复杂度表示法

     > 所有代码的执行时间T(n)与每行代码的执行次数n成正比。
     >
     > 表示代码执行时间随数据规模增长的变化趋势。

  3. 公式中的低阶、常量、系数三部分并不左右增长趋势。

     ```java
     // 函数执行总时间(2n+2)*unit_time
     1 int cal(int n) {
     2   int sum = 0;  //1个unit_time
     3   int i = 1;  //1个unit_time
     4   for (; i <= n; ++i) { //n个
     5     sum = sum + i;  //n个
     6   }
     7   return sum;
     8 }
     
     ```

  4. 只关注循环执行次数最多的一段代码。

     T(n) = O(n)

  5. 加法法则：总复杂度等于量级最大的那段代码的复杂度

  6. 