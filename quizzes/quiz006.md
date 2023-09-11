# Quiz006

# 1. Flow diagram
![IMG_20230911_234724](https://github.com/AntGra25/unit1-CS24/assets/142757981/dd45d6da-461f-45d8-b4e1-bf0dae4b33e2)

# 2. Solution
```.py
def room_loc(room:int) -> str:
    if room % 10 != 0:
        return f"Room {room // 10 + 1}F{room % 10:02d}"
    else:
        return f"Room {room // 10}F10"
```
# 3. Proof of work
![image](https://github.com/AntGra25/unit1-CS24/assets/142757981/b0efdcf8-301b-4435-b8f7-68ccd68c5d5e)

