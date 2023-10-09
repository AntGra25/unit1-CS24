# Quiz009

# 1. flow chart

# 2. solution
```.py
def powersTen(num:int, unit:str) -> str:
    units = {"Tera": 12, "Giga": 9, "Mega": 6, "kilo": 3, "": 0, "mili": -3, "micro": -6, "nano": -9, "pico": -12}
    out = ""
    for rep in units:
        j = num*(10**units[rep])
        if units[rep] < 0:
            j = f"{j:.{abs(units[rep])}f}"
        out += f"{str(j).ljust(20)}{rep}{unit}\n"
    return out


uinput = input("Please enter a measurement: ")
num, unit = uinput.split(" ", 1)

print(powersTen(num=int(num), unit=unit))
```
# 3. proof of work
![Quiz009](https://github.com/AntGra25/unit1-CS24/assets/142757981/2cca7c28-bd42-425e-8e1c-6a81a5347def)
