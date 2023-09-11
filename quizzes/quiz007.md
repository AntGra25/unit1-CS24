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
