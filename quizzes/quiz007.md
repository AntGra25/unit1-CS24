# Quiz007

# 1. Flow diagram

# 2. Solution
```.py
import random

num = random.randint(1,100)
count = 1

while num > 15:
    num = random.randint(1, 100)
    count += 1

if count == 1:
    print("It took 1 try for the number to be less than or equal to 15")
else:
    print(f"It took {count} tries for the number to be less than or equal to 15")
# if/else implemented in order to differentiate between 'try' and 'tries'
```
# 3. Proof of work
![image](https://github.com/AntGra25/unit1-CS24/assets/142757981/c41fda9d-4711-4235-898e-8df7d82feae7)
