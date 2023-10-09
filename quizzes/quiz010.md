# Quiz010

# 1. flow chart

# 2. solution
```.py
def cal(month:str, start_day:int, total:int) -> str:

    calendar = ""
    days = ["Mo", "Tu", "We", "Th", "Fr", "Sa", "Su"]
    calendar += f"{(month + ' 2023').center(20)}\n"
    for d in days:
        if d == "Su":
            calendar += d + "\n"
        else:
            calendar += d + " "
    calendar += "   "*(start_day - 1)
    for d in range(1, total + 1):
        if d < 10:
            calendar += " "
        if (start_day - 1 + d) % 7 == 0:
            calendar += f"{d}\n"
        else:
            calendar += f"{d} "
    return calendar


months = {"January": [7, 31], "February": [3, 28], "March": [3, 31], "April": [6, 30], "May": [1, 31], "June": [4, 30],
"July": [6, 31], "August": [2, 31], "September": [5, 30], "October": [7, 31], "November": [3, 30], "December": [5, 31]}

month = input("Please enter a month: ").title()
while month not in months:
    month = input("[Error] Please enter a valid month: ").title()
start_day, total = months[month][0], months[month][1]

print(cal(month=month, start_day=start_day, total=total))
```
# 3. proof of work
