# DSA-Kth-Largest-Element-in-an-Array
Given an integer array nums and an integer k, return the kth largest element in the array.

Note that it is the kth largest element in the sorted order, not the kth distinct element.

Can you solve it without sorting?
```
Input: nums = [3,2,1,5,6,4], k = 2
Output: 5
```
```
import heapq
class Solution:
    def findKthLargest(self, nums: List[int], k: int) -> int:
        heap=[]
        for i in nums:
            heapq.heappush(heap,i)
            if len(heap)>k:
                heapq.heappop(heap)
        return heap[0]
```
