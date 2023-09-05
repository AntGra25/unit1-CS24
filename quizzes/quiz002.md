# Quiz002

# 1. Flow diagram

# 2. Solution
```.py
def is_20_SL(num1:int, num2:int) -> bool:
    if num1 == 20 or num2 == 20 or num1 + num2 == 20:
        return True
    else:
        return False

def is_20_HL(nums1:list, nums2:list) -> bool:
    for num1 in nums1:
        for num2 in nums2:
            if num1 == 20 or num2 == 20 or num1 + num2 == 20:
                return True
            else:
                return False

print(is_20_SL(30, 10))
print(is_20_SL(30, 5))
print(is_20_SL(30, -10))
print(is_20_SL(200, -180))
print(is_20_HL([10, 30, 10, 26], [20, 15, 5, -6]))
```
# 3. Proof of work
![image](https://github.com/AntGra25/unit1-CS24/assets/142757981/79db66a0-e6da-4b41-813c-d9d778ba898a)
