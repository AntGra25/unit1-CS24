# Quiz004

# 1. Flow diagram
![Quiz004C](https://github.com/AntGra25/unit1-CS24/assets/142757981/a1a8c34a-0c2c-46a1-a1a1-6eee5aa42ad9)

# 2. Solution
```.py
num = input("Please enter an integer: ")
while not num.isdigit():
    num = input("Please enter an integer: ")
num = int(num)

div_sum = 0
for i in range(1, num):
    if num % i == 0:
        print(i, end=", ")
        div_sum += i

if div_sum == num:
    print(True)
else:
    print(False)
```
# 3. Proof of work
![Quiz004-1](https://github.com/AntGra25/unit1-CS24/assets/142757981/7ff6d785-6725-417d-8529-bf0a922e002a)
![Quiz004-2](https://github.com/AntGra25/unit1-CS24/assets/142757981/1eb4ceeb-3016-46ff-8b88-51c712854cf6)
![Quiz004-3](https://github.com/AntGra25/unit1-CS24/assets/142757981/6c962b41-ae6b-442a-b765-2a550e9de012)
![Quiz004-4](https://github.com/AntGra25/unit1-CS24/assets/142757981/7b12f526-48a1-4d52-b09c-4551343906f1)
![Quiz004-5](https://github.com/AntGra25/unit1-CS24/assets/142757981/5eedb6ce-fd8e-415d-80ec-6b5cbcdfc9a3)
