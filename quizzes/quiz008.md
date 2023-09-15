# Quiz008

# 1. Flow diagram
![IMG_20230911_234701](https://github.com/AntGra25/unit1-CS24/assets/142757981/38ef87d2-7de1-4b24-aeb0-4d10c43f2669)

# 2. Solution
```.py
def cipher(text:str, shift:int) -> str:
    secret = ""
    i = 0
    for let in text:
        if let == " ":
            secret += " "
            continue
        else:
            i = ord(let) + shift
            if i > 122:
                i -= 26
            elif i < 97:
                i += 26
        secret += chr(i)
    return secret
```
# 3. Proof of work
![image](https://github.com/AntGra25/unit1-CS24/assets/142757981/8214ad6c-a753-4fc1-a908-f8807f7e2444)
