# Quiz002

# 1. Flow diagram

# 2. Solution
```.py
def is_20(nums1:list, nums2:list) -> bool:
    for num1 in nums1:
        for num2 in nums2:
            if num1 == 20 or num2 == 20 or num1 + num2 == 20:
                return True
            else:
                return False

print(is_20([10, 30, 10, 26], [9, 15, 5, -5]))
```
# 3. Proof of work
