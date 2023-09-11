# Quiz005

# 1. Flow diagram

# 2. Solution
```.py
def ascii_sum(word:str) -> int:
    char_sum = 0
    for char in word:
        char_sum += int(ord(char))
    return char_sum
```
# 3. Proof of work
