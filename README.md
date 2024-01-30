
# Intuition
<!-- Describe your first thoughts on how to solve this problem. -->
- The intuition here is to find the missing number in an array containing numbers from 0 to n, where one number is missing.


---
# Approach
<!-- Describe your approach to solving the problem. -->

- Calculate the expected sum of numbers from 0 to n using the formula (n * (n + 1)) / 2.
- Traverse the given array and calculate the actual sum.
- The difference between the expected sum and the actual sum is the missing number.


---

# Complexity

- **Time complexity: O(n)** (as we traverse the array once)

- **Space complexity: O(1)** (as we use a constant amount of space for variables)


---
# Code
```
class Solution {
public:
    int missingNumber(vector<int>& nums) 
    {
        int size = nums.size();
        int total = ( size * ( size + 1 ) )/2;
        int sum = 0;
        for ( int i=0; i< size; i++ )
            sum = sum + nums[i];
        return total - sum ;
    }
};
```
---
