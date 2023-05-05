## 1. Two sum
Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.
You may assume that each input would have exactly one solution, and you may not use the same element twice.
You can return the answer in any order.
···java
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
···
