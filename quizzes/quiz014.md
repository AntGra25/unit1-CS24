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
