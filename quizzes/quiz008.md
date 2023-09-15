# Quiz008

# 1. Flow diagram
![Quiz008C](https://github.com/AntGra25/unit1-CS24/assets/142757981/cb55bb7f-c5c4-4cc2-9da2-ec3563bb9a91)

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
![Quiz008](https://github.com/AntGra25/unit1-CS24/assets/142757981/17a94837-cf1f-4350-94d3-671fa5238586)
