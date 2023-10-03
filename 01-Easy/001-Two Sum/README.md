Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

You can return the answer in any order.


#### **Example 1:**

Input: nums = [2,7,11,15], target = 9

Output: [0,1]

Explanation: Because nums[0] + nums[1] == 9, we return [0, 1].

#### **Example 2:**

Input: nums = [3,2,4], target = 6

Output: [1,2]

#### **Example 3:**

Input: nums = [3,3], target = 6

Output: [0,1]

##### **Questions to be asked before proceeding.**
1. Are the Numbers always sorted?
2. Are there any floating numbers in between?
3. Do the list contains negative number?
4. Whether list will be in memory?

### **Solution**

#### Brute Force Approach
The very first approach comes to everyone's mind is to go with brute force solution.
Simply iterating over the list using 2 for loops. 

1. Start the first loop (i-th loop) and iterate over to the end of list.
2. Start the second loop (j-th loop) and iterate over to the end of the list.
3. Add list element from i-th loop and j-th loop and compare with the target.
4. If it matches then return the index i and j.
5. Else iterate to next element

```
def two_sum_brute_force(nums, target):
    for i in range(len(nums) - 1):
        for j in range(i + 1, len(nums)):
            if nums[i] + nums[j] == target:
                return [i, j]


print(two_sum_brute_force([1, 2, 3, 9], 10))
```

<iframe width="800" height="500" frameborder="0" src="https://pythontutor.com/iframe-embed.html#code=def%20two_sum_brute_force%28nums,%20target%29%3A%0A%20%20%20%20for%20i%20in%20range%28len%28nums%29%20-%201%29%3A%0A%20%20%20%20%20%20%20%20for%20j%20in%20range%28i%20%2B%201,%20len%28nums%29%29%3A%0A%20%20%20%20%20%20%20%20%20%20%20%20if%20nums%5Bi%5D%20%2B%20nums%5Bj%5D%20%3D%3D%20target%3A%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20return%20%5Bi,%20j%5D%0A%0A%0Aprint%28two_sum_brute_force%28%5B1,%202,%203,%209%5D,%2010%29%29&codeDivHeight=400&codeDivWidth=350&cumulative=true&curInstr=12&heapPrimitives=nevernest&origin=opt-frontend.js&py=3&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>