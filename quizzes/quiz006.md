# Quiz006

# 1. Flow diagram
![Quiz006C](https://github.com/AntGra25/unit1-CS24/assets/142757981/f030780f-d9a7-4fd3-b50f-b88f83d0d792)

# 2. Solution
```.py
def room_loc(room:int) -> str:
    if room % 10 != 0:
        return f"Room {room // 10 + 1}F{room % 10:02d}"
    else:
        return f"Room {room // 10}F10"
```
# 3. Proof of work
![Quiz006](https://github.com/AntGra25/unit1-CS24/assets/142757981/0192911b-af13-4060-9395-3d62bc4d129f)
