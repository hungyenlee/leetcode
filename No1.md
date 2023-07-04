# LeetCode No.1 TwoSum
**[題目連結](https://leetcode.com/problems/two-sum/description/)**

## Python
```python
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        tmp_list = []
        result = []
        for index in range(len(nums)):
            num = nums[index]
            tmp = target - num
            if tmp in tmp_list:
                result.append(nums.index(tmp))
                result.append(index)
                break
            else:
                tmp_list.append(num)
        return result
```

## JavaScript
```javascript
/**
 * @param {number[]} nums
 * @param {number} target
 * @return {number[]}
 */
var twoSum = function(nums, target) {
    for(var index1 = 0; index1<nums.length-1; index1++){
      for(var index2 = index1+1;index2<nums.length;index2++){
        sum = nums[index1]+nums[index2];
        if (sum == target){
            return [index1,index2];
        }
      }
    }
};
```
