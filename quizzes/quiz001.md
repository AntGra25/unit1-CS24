# Quiz001

# 1. flow diagram
![IMG_20230906_103428](https://github.com/AntGra25/unit1-CS24/assets/142757981/26cd1e45-991c-4b92-b7b9-039b40905c09)


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
![Quiz001](https://github.com/AntGra25/unit1-CS24/assets/142757981/b328ef6e-67ff-4a05-9cbe-58fdbf160f79)

