# Criteria A: Planning

## Problem definition

Ms. Sato is a local trader who is interested in the emerging market of cryptocurrencies. She has started to buy and sell electronic currencies, however at the moment she is tracking all his transaction using a ledger in a spreadsheet which is starting to become burdensome and too disorganized. It is also difficult for Ms Sato to find past transactions or important statistics about the currency. Ms Sato is in need of a digital ledger that helps her track the amount of the cryptocurrency, the transactions, along with useful statistics.

Apart for this requirements, Ms Sato is open to explore a cryptocurrency selected by the developer.

An example of the data stored is

| Date        | Description                | Category | Amount       |
|-------------|----------------------------|----------|--------------|
| Sep 23 2022 | bought a house             | Expenses | 10 BTC       |
| Sep 24 2022 | food for house celebration | Food     | 0.000001 BTC |

## Success criteria

1. The electronic ledger is a text-based software (Runs in the Terminal).
2. The electronic ledger display the basic description of the cyrptocurrency selected.
3. The electronic ledger allows to enter, withdraw and record transactions.
4. The electronic ledger displays the current exchange rate by accessing data from the internet.
5. The electronic ledger allows to create accounts protected by passwords.
6. The electronic ledger compares the current exchange rate to rates dating back a year.

## Proposed solution
Design statement: I will design an XRP electronic ledger for Ms. Sato. It will be evaluated according to the success criteria described in the section above. The program will provide Ms. Sato with the current exchange rate of XRP by directly accessing the internet, so she can make decisions based on up-to-date information. It will also use downloaded data on exchange rates dating back to a year, so that she can compare past values to the current one and make a more informed decision. The program will also allow for the creation of multiple accounts that are protected by passwords, so that Ms. Sato can have her account and her digital ledger secured. The program will be designed in Python 3.9.13 and it will take until Oct 5 2023 to be made.

I will be using Python for the development of this program for four main reasons:
1. Python has a clear syntax that is understandable even to people with minimal programming experience. This makes the program simpler to maintain and makes explaining the code to Ms. Sato easier.
2. Python has a large community that is constantly active on the Internet. If I were to run into a problem, I can quickly consult online forums to find an easy fix.
3. Python is the programming language that I am most proficient in. This makes the development of the program more efficient and allows me to provide more complex solutions than if I were using another programming language
4. Python has a vast range of libraries that make development more effcient. For this project specifically I will use the'requests' library, which helps extract data from urls that can be used by the 'BeautifulSoup' library, which allows me to easily access the current exchange rate of XRP. I will also the 'currency_converter' library that allows me to access the exchange rates of major currencies, which I can use to allow entering deposits and taking withdrawals in USD, EUR, and JPY, which improves accessbility for Ms. Sato. Another library I will use is the 'datetime' library, which allows me to access the current date and use it when Ms. Sato makes transactions. The last library I will use is the 'tabulate' library, which allows me to display past transactions in a presentable format, making it easier for Ms. Sato to keep track of her withdrawals.
   
I will also be using my own libraries which I will save in the 'my_lib.py' file. These include 'frame_maker', 'print_menu', 'validate_int', 'currency_convert', 'colors', and 'date_format'. These enable more efficient development by facilitating time-consuming processes and allow me to display text in a more presentable manner.

For my repository I will be using GitHub. This is because it allows me to store my code and documentation, essentially acting as a backup and reducing risk of data loss. It is also easily accessible to other users and shows changes made over time, which allows Ms. Sato to monitor the progress of the project.

I chose XRP as the cryptocurrency used in the electronic ledger for the advantages it has over other cryptocurrencies:
* XRP is known for its rapid transaction settlement times. Confirmations typically occur in just four to five seconds, compared with the days it may take for a wire transfer or minutes or potentially hours for Bitcoin transactions.
* XRP boasts very low transaction fees. The cost to complete a transaction on the Ripple network is just 0.00001 XRP, which translates to a minimal fraction of a penny at current exchange rates.
* The Ripple network is highly versatile and not limited to processing transactions using XRP alone. It supports a wide range of fiat currencies and other cryptocurrencies, which allows Ms. Sato to easily transact in multiple currencies, reducing the need for multiple cryptocurrency wallets.
* XRP has gained significant recognition and adoption among large financial institutions. Institutions like Santander and Bank of America utilize the Ripple network for their transaction needs, setting XRP apart from many other cryptocurrencies.
By using XRP, I can make a digital ledger with a cryptocurrency that is characterised by its speed, cost-effectiveness, versatility, and instituitional support, which can greatly help Ms. Sato with cryptocurrency trading.

# Criteria B: Design

## System Diagram
![image](https://github.com/AntGra25/unit1-CS24/assets/142757981/13f2d5fc-7e89-4eaf-8a04-08a3ceb52c14)
The program receives the input from the keyboard and projects its output on the screen while accessing data from the internet. The electronic ledger was programmed on a laptop whose operating system is Windows 10 2H22, CPU is AMD Ryzen 9 5900HX, RAM is 16GB, and disk space is 933GB. Python 3.9.13 is used to code the electronic ledger, which is located in the project1.py file. The data is stored in the database.csv file.
## Flow Diagrams
[image] Fig.1 This is the flow diagram for the login system
## Record of Tasks
| Task No | Planned Action                                      | Planned Outcome                                                                                                                                 | Time estimate | Target completion date | Criterion |
|---------|-----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|---------------|------------------------|-----------|
| 1       | Create system diagram                               | To have a clear idea of the hardware and software requirements for the proposed solution                                                        | 20min         | Sep 13                 | B         |
| 2       | Create login system                                 | To have a flow diagram and the code for the login system                                                                                        | 30min         | Sep 14                 | B, C      |
| 3       | Create deposit system                               | To have a way for the user to enter deposits and store them in the user's database                                                              | 15min         | Sep 18                 | C         |
| 4       | Display balance                                     | To have a way for the user to see the total assets on their account based on deposits and withdrawals                                           | 10min         | Sep 18                 | C         |
| 5       | Show simple bar graph                               | To have a way for the user to visualize the amount of money deposited compared to money withdrawn                                               | 10min         | Sep 18                 | C         |
| 6       | Create withdrawal system                            | To have a way for the user to make withdrawals and store them in the user's database                                                            | 5min          | Sep 20                 | C         |
| 7       | Improve UI                                          | To make it easier for the user to use the program by making it more visually appealing, adding signposts, and adding more accessibility options | 25min         | Sep 29                 | C         |
| 8       | Add registration system                             | To have a registration system so new users can use the program                                                                                  | 40min         | Sep 29                 | C         |
| 9       | Research webscraping                                | To have an idea on how to use data collected from the internet later in the program                                                             | 75min         | Sep 30                 | C         |
| 10      | Create current exchange rate variable               | To have easy access to the coins current exchange rate                                                                                          | 30min         | Sep 30                 | C         |
| 11      | Create currency conversion function                 | To add multiple currencies to the program                                                                                                       | 15min         | Sep 30                 | C         |
| 12      | Introduce multiple currencies to transaction system | To allow the user to make deposits and withdrawals with multiple currencies                                                                     | 60min         | Sep 30                 | C         |
| 13      | Introduce multiple currencies to balance display    | To let the user to better visualize their total assets by allowing to display them in multiple currencies                                       | 30min         | Sep 30                 | C         |
| 14      |                                                     |                                                                                                                                                 |               |                        |           |

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


