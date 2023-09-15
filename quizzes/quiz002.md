# Quiz002

# 1. Flow diagram
![Quiz002C](https://github.com/AntGra25/unit1-CS24/assets/142757981/4968bb8f-65a0-4de2-be52-37ec059aecd6)

# 2. Solution
```.py
def is_20_SL(num1:int, num2:int) -> bool:
    if num1 == 20 or num2 == 20 or num1 + num2 == 20:
        return True
    else:
        return False
def is_20_HL(nums1:list, nums2:list) -> bool:
    is_20 = False
    for num1 in nums1:
        for num2 in nums2:
            if num1 == 20 or num2 == 20 or num1 + num2 == 20:
                is_20 = True
    return is_20

print(is_20_SL(30, 10))
print(is_20_SL(30, 5))
print(is_20_SL(30, -10))
print(is_20_SL(200, -180))
print(is_20_HL([10, 30, 10, 26], [20, 15, 5, -6]))
```
# 3. Proof of work
![Quiz002](https://github.com/AntGra25/unit1-CS24/assets/142757981/8ab873cc-18bc-4992-85d9-1b112e3f7a79)


