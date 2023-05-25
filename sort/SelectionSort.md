## Selection Sort
leetCode 75. Sort Colors

![selection sort](https://github.com/liu2su/leetcode/assets/96462566/796c75a8-d545-4899-b885-e6f5be713d4a)

Best case: O(n^2)

Avertage case : O(n^2)

Worst case: O(n^2)

### Code
```java
class Solution {
    public void sortColors(int[] nums) {
        //选择排序的sorted array在数组的头部，与冒泡排序相反
        int temp = 0;//temp variable 记录子数组的最小值
        int tempindex = 0;
        for(int i = 0;i< nums.length -1;i++){
            //i 代表已经排序完成的数组的个数，停止条件为所有数组排序完成
            //因为数组的index start from 0,所以i的值也是进行遍历的子数组的第一个元素坐标
            temp = nums[i];
            tempindex = i;
            //将子数组的第一个元素记录为目前的最小值，同时记录坐标
            for(int j = i+1;j<=nums.length - 1; j++){
                if(temp > nums[j]){
                    temp =nums[j];
                    tempindex = j;
                    //遍历子数组找出子数组的最小值，因为数组维护在前端，所以for循环起始位置为子数组第一个元素（+1也可）停止位置为子数组最后一个元素遍历完成。
                }
            }
            nums[tempindex] = nums[i];
            nums[i] = temp;
            //swap
        }
    }
}
```
