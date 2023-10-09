# Quiz016

# 1. flow chart

# 2. solution
```.py
def averageLength(words:list) -> float:
    count = 0
    for word in words:
        for let in word:
            if let != " ":
                count += 1
    return count/len(words)


print(averageLength(words=["hello", "main"]))
print(averageLength(words=["Peru", "France", "Nepal"]))
print(averageLength(words=["Computer Science", "Art"]))
print(averageLength(words=["one", "two"]))
```
# 3. proof of work
