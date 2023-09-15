# Quiz003

# 1. Flow diagram
![Quiz003C](https://github.com/AntGra25/unit1-CS24/assets/142757981/1bd9ccfe-80ad-46a7-9dfb-6b6c9b7003f0)

# 2. Solution
```.py
def DNAtranslator(in_protein: str) -> str:
    out_protein = ""
    for i in in_protein:
        if i == "A":
            out_protein += "T"
        elif i == "G":
            out_protein += "C"
        elif i == "T":
            out_protein += "A"
        elif i == "C":
            out_protein += "G"
    return out_protein

print(DNAtranslator("A"))
print(DNAtranslator("G"))
print(DNAtranslator("T"))
print(DNAtranslator("C"))
print(DNAtranslator("AGCT"))
```
# 3. Proof of work
![Quiz003](https://github.com/AntGra25/unit1-CS24/assets/142757981/d3483dc5-91ab-4ca2-a9c2-76271a41823c)
