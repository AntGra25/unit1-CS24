# Quiz006

# 1. Flow diagram

# 2. Solution
```.py
def room_loc(room:int) -> str:
    if room % 10 != 0:
        return f"Room {room // 10 + 1}F{room % 10:02d}"
    else:
        return f"Room {room // 10}F10"
```
# 3. Proof of work

