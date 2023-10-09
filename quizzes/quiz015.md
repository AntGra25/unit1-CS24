# Quiz015

# 1. flow chart

# 2. solution
```.py
def open_doors(num_students:int) -> int:
    count = 0
    doors = [False]*num_students
    for stu in range(num_students):
        for d in range(stu, num_students, stu + 1):
            doors[d] = not doors[d]
    for d in doors:
        if d:
            count += 1
    return count


print(open_doors(num_students=10))
print(open_doors(num_students=100))
print(open_doors(num_students=200))
print(open_doors(num_students=5678))
```
# 3. proof of work
![Quiz015](https://github.com/AntGra25/unit1-CS24/assets/142757981/c93698e3-4827-4f5b-8848-c541b1030250)
