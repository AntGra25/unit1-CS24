# Quiz003

# 1. Flow diagram
![IMG_20230906_103513](https://github.com/AntGra25/unit1-CS24/assets/142757981/bc20aa09-0cb1-41c4-aa4b-25d67fb1adc8)

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
![image](https://github.com/AntGra25/unit1-CS24/assets/142757981/5f93088c-02b8-4cb3-b6b8-c099c1fe9eee)
