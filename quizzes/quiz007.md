# Quiz007

# 1. Flow diagram
![Quiz007C](https://github.com/AntGra25/unit1-CS24/assets/142757981/c8b1cf77-167e-4270-a41a-45637b2c74f9)

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
![Quiz007](https://github.com/AntGra25/unit1-CS24/assets/142757981/8577dc4a-8405-4280-aaee-9b68d0718167)
