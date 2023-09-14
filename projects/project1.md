# Criteria A: Planning

## Problem definition

Ms. Sato is a local trader who is interested in the emerging market of cryptocurrencies. She has started to buy and sell electronic currencies, however at the moment she is tracking all his transaction using a ledger in a spreadsheet which is starting to become burdensome and too disorganized. It is also difficult for Ms Sato to find past transactions or important statistics about the currency. Ms Sato is in need of a digital ledger that helps her track the amount of the cryptocurrency, the transactions, along with useful statistics.

Apart for this requirements, Ms Sato is open to explore a cryptocurrency selected by the developer.

An example of the data stored is

| Date        | Description                | Category | Amount       |
|-------------|----------------------------|----------|--------------|
| Sep 23 2022 | bought a house             | Expenses | 10 BTC       |
| Sep 24 2022 | food for house celebration | Food     | 0.000001 BTC |
## Proposed solution

## Success criteria

1. The electronic ledger is a text-based software (Runs in the Terminal).
2. The electronic ledger display the basic description of the cyrptocurrency selected.
3. The electronic ledger allows to enter, withdraw and record transactions.
4. The electronic ledger displays the current exchange rate by accessing data from the internet.
5. The electronic ledger allows to create accounts protected by passwords.
6. The electronic ledger compares the current exchange rate to rates dating back a year.

# Criteria B: Design

## System Diagram
![image](https://github.com/AntGra25/unit1-CS24/assets/142757981/13f2d5fc-7e89-4eaf-8a04-08a3ceb52c14)
The program receives the input from the keyboard and projects its output on the screen while accessing data from the internet. The electronic ledger was programmed on a laptop whose operating system is Windows 10 2H22, CPU is AMD Ryzen 9 5900HX, RAM is 16GB, and disk space is 933GB. Python 3.9.13 is used to code the electronic ledger, which is located in the project1.py file. The data is stored in the database.csv file.
## Flow Diagrams
[image] Fig.1 This is the flow diagram for the login system
## Record of Tasks
| Task No | Planned Action        | Planned Outcome                                                                          | Time estimate | Target completion date | Criterion |
|---------|-----------------------|------------------------------------------------------------------------------------------|---------------|------------------------|-----------|
| 1       | Create system diagram | To have a clear idea of the hardware and software requirements for the proposed solution | 20min         | Sep 13                 | B         |
| 2       | Create login system   | To have a flow diagram and the code for the login system                                 | 30min         | Sep 14                 | C         |

# Criteria C: Development

## Login System
My client requires a system to protect the private data. I thought about using a login system to accomplish this requirement using an if condition and the open command to work with a csv file

As you can see the the flow diagram in **Fig 1**, in the first line I am defining a function called try_login. This function has two inputs of type string, and the output is a boolean representing True if the user logins correctly or false otherwise. This is saved in the variable success. Then in line two...

```.py
def try_login(name:str, password:str) -> bool:
    with open("users.csv", mode="r") as f:
        data = f.readlines()

    success = False
    for line in data:
        uname = line.split(",")[0]
        upass = line.split(",")[1].strip()
        if uname == name and upass == password:
            success = True
            break
    return success


attempts = 3
in_name = input("Enter your username: ")
in_pass = input("Enter your password: ")
result = try_login(name=in_name, password=in_pass)
while result == False and attempts > 1:
    in_name = input("[Error try again] Enter your username")
    in_pass = input("Enter your username")
    result = try_login(name=in_name, password=in_pass)
    attempts -= 1

if result == False:
    print("Sayonara")
    exit(1) # 1 is the code for exit without error

# the program continues here if it does close
print("Welcome")
```


