# Quiz001

# 1. flow diagram

# 2. solution

```.py
def word_compress(word:str) -> str:
    words = word.split()
    output = ""
    for word in words:
        if len(word) >= 3:
            output += word[0] + str(len(word)-2) + word[-1] + " "
        else:
            output += word + " "
    return(output)

print(word_compress("internationalization"))
print(word_compress("localization"))
print(word_compress("98 99 100 101 1062"))
print(word_compress("Hello world !"))
print(word_compress("(codin) + (game) = (codingame)"))
```
# 3. proof of work
![image](https://github.com/AntGra25/unit1-CS24/assets/142757981/9c5a50a5-9634-4ad9-9fda-a988534bcccc)

