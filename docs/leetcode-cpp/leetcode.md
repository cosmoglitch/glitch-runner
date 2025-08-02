---
sidebar_label: 'Leetcode Problems'
id: leetcode
title: Leetcode problems in C++
slug: /leetcode
description: Let's solve Leetcode problems
---

## 1. Two Sum
> Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.
You may assume that each input would have exactly one solution, and you may not use the same element twice.
You can return the answer in any order.
Example 1:
Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Explanation: Because nums[0] + nums[1] == 9, we return [0, 1].


***Approach*** : 
We will loop through the array once. And add the visited umber and its index to a Map.
* With every index in loop, we will fetch the number and find the difference from "target". 
* If the difference has already been visited in the array, then we return the current index and the index of the visited number.
* Else we add the visited number and index to the Map and move along.
* At the end if no 2 numbers satisfy the condition, we send {-1, -1}

```
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {

        unordered_map<int, int> visitedMapList;

        for (int i = 0; i<nums.size(); i++) {
            int difference = target - nums[i];

            if (visitedMapList.find(difference) != visitedMapList.end()) {
                return {visitedMapList[target-nums[i]], i};
            }

            visitedMapList[nums[i]] = i;
        }

        return {-1,-1};
    }
};
```

**Space Complexity** : O(n)

**Time Complexity**  : O(n)
