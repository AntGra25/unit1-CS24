# Quiz001

# 1. flow diagram

# 2. solution

```.py
word = input("Please enter text: ")
words = word.split()
for word in words:
    if len(word) >= 3:
        print(word[0], len(word)-2, word[-1], sep="", end=" ")
    else:
        print(word, end=" ")
```
# 3. proof of work
![image](https://github.com/AntGra25/unit1-CS24/assets/142757981/9c5a50a5-9634-4ad9-9fda-a988534bcccc)

