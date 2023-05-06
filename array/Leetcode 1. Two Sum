## 1. Two Sum
### Problem discription
Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.
You may assume that each input would have exactly one solution, and you may not use the same element twice.
You can return the answer in any order.
### Analyse
Two pointer:双指针法的入门题目，在使用双指针法之前我们一般需要sort数组。
            在本题中一个指针在数组head,另一个指针在rear,根据指针指向的两元素之和与target大小判定指针移动方向，停止条件为前后指针相交。
### Code
```java
class Solution {
    public int[] twoSum(int[] nums, int target) {
        Arrays.sort(nums);
        int i = 0;
        int j = nums.length - 1;
        int[] result = new int[2];
        while(i < j){
            if(nums[i] + nums[j] < target){
                i++;
            }
            if(nums[i] + nums[j] > target){
                j--;
            }
            else{
                result[0] = nums[i];
                result[1] = nums[j];
            }
        }
        return result;
        
    }
}
```
