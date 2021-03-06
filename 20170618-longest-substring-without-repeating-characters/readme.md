输入一个字符串，找出其中没有重复字符的最长的子字符串（本题要求找出最长的子串，然后输出其长度，但不输出子串

想想能不能用到什么比较高级的算法和数据结构来简单高效的实现？链表？队列？栈？二叉树？排序？二分搜索？好吧，我就熟悉这几种简单的，更多的就想不到了，就这几种，用不上啊！

还是用循环呗

* 从字符串的第一个字符开始逐个循环
* 从起始位置循环，确定从这个位置开始的最长不重复子串的长度
* 最后获得最长的长度

详细的看代码实现！

最初的开发调试中就是因为一些边界情况没有考虑，所以在功能上一直出错，接下来给出time_limit_exceeded.c这个版本的实现代码，但是时间复杂度超过要求，这种实现方式的时间复杂度到了O(N^3)了，所以性能很差劲

## 更优的方案

先提出并回答几个问题：

* 在空间复杂度为O(1)的限制下，上面O(N^3)的时间复杂度是不是最优的了
* 如果第一个问题的回答是“Yes”，那么只能想办法通过提升空间复杂度来降低时间复杂度了
* 提升空间复杂度，就要想到该使用哪种数据结构来提升性能！

思维的局限：

* 面对很多算法的问题，目前我总是往“只用循环”这个思路上走
* 另外也许上面的三条思考也是有局限的

---

## Add In 20170629

仔细回想了一下，大多数时候，面对一些问题，自己第一想到的就是用暴力循环、轮询来解决问题，这种方法虽然能解决问题，但总是最慢的、最愚蠢的。甚至都不能称之为算法！

