## Insertion Sort
leetCode 75. Sort Colors

![insertionsort](https://github.com/liu2su/leetcode/assets/96462566/97a4fd59-867d-4e3d-888b-7d3cbc36cdff)

 ```java
 class Solution {
    public void sortColors(int[] nums) {
        //插入排序，未排序数组的元素依次与以排序数组比较，找到插入位置
        int index;
        int temp;
        for(int i = 0;i<= nums.length -1;i++){
            //第一个循环，i代表已经排序的元素，从0开始，停止条件为全部元素已经排序。
            index = i; 
            temp = nums[index]; //插入排序会造成已排序数组前移覆盖（每次循环已排序数组长度+1），所以需要临时变量储存需要比较的元素值
            while(index > 0 && temp < nums[index-1]){//注意nums[index]会覆盖，所以要用temp比较
                //由动图可知index是被比较元素的动态位置，如果前一个元素比它大，则，停止循环并插入该位置。否则持续前移
                nums[index] = nums[index -1];
                index--;
            }
            nums[index] = temp;//插入该位置，循环结束时，index代表的是被排序元素在新数组的位置
        }
        
    }
}
 ```




