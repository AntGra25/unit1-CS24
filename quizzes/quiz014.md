# Quiz014

# 1. flow chart

# 2. solution
```.py
def blackBoxThree(given:str) -> str:
    out = ""
    count = 0
    for l in range(len(given)):
        if given[l] == " ":
            out += " "
        else:
            for l2 in given[:l + 1]:
                if given[l].upper() == l2.upper():
                    count += 1
            out += str(count)
            count = 0
    return out


print(blackBoxThree(given="hello world"))
print(blackBoxThree(given="aaaaAABB"))
print(blackBoxThree(given="abABabAB"))
print(blackBoxThree(given="Create a Function"))
```
# 3. proof of work
![Quiz014](https://github.com/AntGra25/unit1-CS24/assets/142757981/67cc0945-c812-4255-918c-d27284544848)
