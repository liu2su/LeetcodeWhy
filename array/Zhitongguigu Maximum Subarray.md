## Zhitongguigu - Maximum Subarray
### Description
Find the contiguous subarray within an array (containing at least one number) whichhasthe largest sum.

For example, given the array [-2,1,-3,4,-1,2,1,-5,4], the contiguous subarray [4,-1,2,1] hasthe largest sum = 6

### Analyse
这道题用贪心或者动态规划做都可以，此处只记录brute force的方法，枚举出所有可能的子数组的合，记录最大值，
需要两个for循环完成，第一个for循环指定子数组的起始位置，第二个for循环将包括次位置在内的后续元素依次遍历求和，每次求和后与记录值比较，选出最大值。

### Code
```java
int maxSubArray(int[] nums) {
  int gloablMax = Integer.MIN_VALUE;
  int n = nums.length;
  // i 是子数组起始位置
  for (int i = 0; i < n; i++) {
    int partialSum = 0;
    // 固定起始位置，不同长度的子数组求和
    for (int j = i; j < n; j++) {
      partialSum += nums[j];
      if (partialSum > gloablMax) {
      gloablMax = partialSum;
      }
    }
  }
  return gloablMax;
}
```
