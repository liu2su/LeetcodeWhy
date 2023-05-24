## Bubble Sort
### Leetcode: 75. Sort Colors
###

![849589-20171015223238449-2146169197](https://github.com/liu2su/leetcode/assets/96462566/0dd80500-6b04-40db-ab49-3df5c3d8710f)


Best case: O(n^2)

Avertage case : O(n^2)

Worst case: O(n^2)

### Code
```java
class Solution {
    public void sortColors(int[] nums) { // bubble sort
        // Bubble sort need to for loops
        int n = nums.length - 1; // n 表示数组最后一个元素
        int temp = 0; // swap 临时变量
        for(int i = 0; i<=n; i++){ 
            //因为 bubble sort put the largest element at the end of subarray each time
            //所以 i 代表的是已经有i个元素已经排好序，接下来的遍历要在未排序的数组内进行
            for(int j = 0; j <= n - i - 1; j++){
                //第二个for loop的目的是找出子数组内最大元素排序到最后，使用swap策略
                //因为数组是在末尾排序的，所以子数组的范围是数组第一个元素最后一个元素位置减去
                //已经排序完成的数组的个数再减去最后一个元素（-1，因为遍历最后一个元素的前一个元素
                //时已经排序了）
                if(nums[j] > nums[j+1]){
                    temp = nums[j];
                    nums[j] = nums[j+1];
                    nums[j+1] = temp;
                }
            }

        }
    }
}
```
