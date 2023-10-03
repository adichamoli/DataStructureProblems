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
