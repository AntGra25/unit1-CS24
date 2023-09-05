# Quiz003

# 1. Flow diagram

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

print(DNAtranslator("AGTGC"))
```
# 3. Proof of work
![image](https://github.com/AntGra25/unit1-CS24/assets/142757981/5f93088c-02b8-4cb3-b6b8-c099c1fe9eee)
