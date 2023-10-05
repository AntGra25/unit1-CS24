![image](https://github.com/AntGra25/unit1-CS24/assets/142757981/acc07ecb-80b4-40b4-a2bc-5e710753c651)

<sub>Illustration by Eddie Lobanovskiy</sub>

# Criteria A: Planning

## Problem definition

Ms. Sato is a local trader who is interested in the emerging market of cryptocurrencies. She has started to buy and sell electronic currencies, however at the moment she is tracking all her transactions using a ledger in a spreadsheet which is starting to become burdensome and too disorganized. It is also difficult for Ms Sato to find past transactions or important statistics about the currency. Ms Sato is in need of a digital ledger that helps her track the amount of the cryptocurrency, the transactions, along with useful statistics.

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
![image](https://github.com/AntGra25/unit1-CS24/assets/142757981/c6481a11-b757-4974-834f-9952685a5091)
**Fig 1** This is the system diagram

The program receives the input from the keyboard and projects its output on the screen while accessing data from the internet. The electronic ledger was programmed on a laptop whose operating system is Windows 10 2H22, CPU is AMD Ryzen 9 5900HX, RAM is 16GB, and disk space is 933GB. Python 3.9.13 is used to code the electronic ledger, which is located in the project1.py file. The program accesses libraries created by me which are located in my_lib.py. The transaction data is stored in the 'transactions.csv' file, the users' account data is stored in the 'users.csv' file, and the XRP exchange rates dating back a year are stored in the 'year_rates.csv' file.
## Flow Diagrams
[image] **Fig.2** This is the flow diagram for the login and registration systems
Ms. Sato requires a system that protects private data. I thought about using login and registration systems so that she can enter the data thanks to the registration and keep it protected using the login, fulfilling this requirement.
As you can see by the flow diagram in **Fig. 2**, the program begins by displaying the 'Login' and 'Registration' options in a numbered list, setting the value of the 'selection' variable to 0, and asking the user to input a number corresponding to the options on the list. The input is stored in 'selection' and is asked from the user until it is equal to either 1 or 2. The program then checks whether 'selection' is equal to 2, and if it is not, it is assumed that the value is equal to 1 and the user is directed straight towards the login system. If it is equal to 2, the program proceeds to the registration system and the user is asked to input a username for their account. The user will be kept being asked for the username until it is unique from all the other usernames stored in the 'users.csv' file. When it is unique, the user is asked to enter the password for their account and to confirm it by typing it in again. These inputs are stored in the 'new_pass' and 'confirm_pass' variables, and if they are not equal to each other, the program prints 'password not matching' asks the user to enter one of two options: try to confirm the password again or create a different one. Until the user inputs 1 or 2 into the 'answer' variable, they will be asked for a new input. Once 'answer' is equal to one of the numbers, the program checks if it is equal to 2. If it is not, the user is asked for the input to the 'confirm_pass' variable, and if it is, they are asked for the input to the 'new_pass' variable before proceeding to 'confirm_pass'. When the two variables are equal, the account puts the account data into the 'users.csv' file, prints 'Account created successfully, and moves on to the login system. The 'attempts' variable is set to three and the user is asked to input a username and a password, which are stored in the 'u_name' and 'u_pass' variables respectively. While 'u_name' and 'u_pass' are different from the set of usernames and passwords stored in 'users.csv' and there are still 'attempts' left, the user is asked to input 'u_name' and 'u_pass' again and 1 is subtracted from 'attempts. If after exiting the while loop the 'u_name' and 'u_pass' still differ from those in 'users.csv', the program prints 'Sayonara' and forces itself to close without error by using 'exit(1)'. If they values are equal though, the user is welcomed to the XRP digital ledger.

![Flowchart2](https://github.com/AntGra25/unit1-CS24/assets/142757981/1b4ed971-eb57-4a78-9b3b-3d0f2a6668bd)

**Fig.3** This is the flow diagram of the exchange rate information display system

Ms Sato requires a system that tracks useful statistics about the cryptocurrency that is being used. I thought about using an exchange rate information display system to fulfill this requirement.
As you can see by the flow diagram in **Fig.3**, the program begins by defining 2 empty lists and storing all the lines from the 'year_rates.csv' file into the 'data' variable. Next, it uses a for loop to iterate over each of the lines, splitting them by the ';' symbol. The loop then appends the first element of the line rounded to the 4th decimal place to the 'e_rates' list. It also appends the seventh element of the line to the 'dates' list after formatting it. The program proceeds to divide the current exchange rate of XRP by the exchange rate from one year earlier, formatting the result to have only 2 decimal points, and storing it in the 'first_percent' variable. It then checks if the variable is higher or lower than 0. If it is higher, it sets the status to 'higher', and if it is lower, it sets the status to 'lower', while also multiplying the variable by -1 to make it positive. These two operations are done so that the program can determine by how many percent the current exchange rate is higher or lower than the one from a year earlier. The program then proceeds to divide the current exchange rate by the lowest and highest rates from the year, formats the results in the same way as before, a stores them in the 'min_percent' and 'max_percent' variables, respectively. Finally, the program includes all of this information in a single print statement, also adding the dates on which the four different exchange rates were measured.
![Flowchart3](https://github.com/AntGra25/unit1-CS24/assets/142757981/73dbdb84-1f1d-45cf-8f7c-01e50e5069b7)

**Fig.4** This is the flow diagram of the balance display system

Ms. Sato requires a system that tracks the amount of cryptocurrency she possesses at a given moment. I thought about using a balance display system to fulfill this requirement, with the option to display this information in 4 different currencies as additional accessibility.
As you can see by the flow diagram in **Fig.4**, the program begins by storing all lines from the 'transactions.csv' file into the 'data' variable and setting the value of the 'balance' variable to 0. Next, it uses a for loop to over each of the lines in the 'data' variable, splitting them by comma. It then sets the first element as 'date and and second element as 'amount', which it adds to the balance variable. After finishing iterating over the for loop, the program sets the current date as the 'today' variable and prints 'XRP', 'USD', 'EUR', and 'JPY' in a numbered list, asking the user to input a number corresponding to their desired balance display method. This input is stored in the 'dbalance' variable and is asked from the user until it is equal to either 1, 2, 3, or 4. When it is equal, the proceeds to set the 'symbol' variable as the USD symbol and sets the 'value' variable as 0. The program then checks whether the 'dbalance' variable is equal to 2. If it is, the 'balance' variable is multiplied by the current exchange rate, and if it is not, the program checks if 'dbalance' is equal to either 3 or 4. If it is not, the 'balance' variable is not modified, but if it is, the balance is multiplied by the exchange rate and then converted into either EUR or JPY, depending on the value of 'dbalance'. Next, if the value of 'dbalance' is equal to 3, the 'symbol' variable is set to the EUR symbol and the 'value' variable is set to the 'balance' variable rounded to 2 decimal places. If it is not, it can be assumed that 'dbalance' is equal to 4 because of the earlier 'if' condition, and 'symbol' is set to the JPY symbol and 'value' is set to the 'balance' rounded to the first digit. This is because the with JPY, unlike with the EUR and the USD, the lowest coin is 1JPY, meaning there is no such thing as 'half a yen'. Finally, the program takes the value of 'balance' and prints it according to the method chosen earlier by the user along with the current date. The print statement is surrounded by a frame composed of the corresponding symbol (if EUR was chosen as the method of display, the frame will consist of EUR symbols).

## Record of Tasks
| Task No | Planned Action                                         | Planned Outcome                                                                                                                                     | Time estimate | Target completion date | Criterion |
|---------|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|---------------|------------------------|-----------|
| 1       | Create system diagram                                  | To have a clear idea of the hardware and software requirements for the proposed solution                                                            | 20min         | Sep 13                 | B         |
| 2       | Create login system                                    | To have a flow diagram and the code for the login system                                                                                            | 30min         | Sep 14                 | B, C      |
| 3       | Create deposit system                                  | To have a way for the user to enter deposits and store them in the user's database                                                                  | 15min         | Sep 18                 | C         |
| 4       | Display balance                                        | To have a way for the user to see the total assets on their account based on deposits and withdrawals                                               | 10min         | Sep 18                 | C         |
| 5       | Show simple bar graph                                  | To have a way for the user to visualize the amount of money deposited compared to money withdrawn                                                   | 10min         | Sep 18                 | C         |
| 6       | Create withdrawal system                               | To have a way for the user to make withdrawals and store them in the user's database                                                                | 5min          | Sep 20                 | C         |
| 7       | Improve UI                                             | To make it easier for the user to use the program by making it more visually appealing, adding signposts, and adding more accessibility options     | 25min         | Sep 29                 | C         |
| 8       | Add registration system                                | To have a registration system so new users can use the program                                                                                      | 40min         | Sep 29                 | C         |
| 9       | Research webscraping                                   | To have an idea on how to use data collected from the internet later in the program                                                                 | 75min         | Sep 30                 | C         |
| 10      | Create current exchange rate variable                  | To have easy access to the coins current exchange rate                                                                                              | 30min         | Sep 30                 | C         |
| 11      | Create currency conversion function                    | To add multiple currencies to the program                                                                                                           | 15min         | Sep 30                 | C         |
| 12      | Introduce multiple currencies to transaction system    | To allow the user to make deposits and withdrawals with multiple currencies                                                                         | 60min         | Oct 01                 | C         |
| 13      | Introduce multiple currencies to balance display       | To let the user to better visualize their total assets by allowing to display them in multiple currencies                                           | 30min         | Oct 01                 | C         |
| 14      | Add basic description of XRP                           | To allow the user to know more about the cryptocurrency used in the digital ledger                                                                  | 15min         | Oct 02                 | C         |
| 15      | Add 'reason' and 'category' to withdrawal system       | To have a more detailed account of the user's withdrawal                                                                                            | 10min         | Oct 02                 | C         |
| 16      | Create table displaying withdrawals                    | To create a table displaying withdrawal history in an organized manner                                                                              | 30min         | Oct 02                 | C         |
| 17      | Create 'year_rates' csv file                           | To have access to XRP's exchange rates dating back to a year                                                                                        | 5min          | Oct 03                 | C         |
| 18      | Display exchange rate information                      | To have a way for the user to view XRP's current exchange rate and how it compares to the rate from a year ago, the 1-year low, and the 1-year high | 75min         | Oct 03                 | C         |
| 19      | Edit proposed solution                                 | To have an more accurate picture of the solution                                                                                                    | 40min         | Oct 04                 | A         |
| 20      | Edit system diagram                                    | To have a more accurate system diagram after creating the 'my_lib.py' file and new csv files                                                        | 15min         | Oct 04                 | B         |
| 21      | Improve UI again                                       | To make the program more visually appealing                                                                                                         | 15min         | Oct 04                 | C         |
| 22      | Create flow diagrams for 3 different parts of the code | To allow the user to know how the program works and what the reasoning behind the proposed solutions is                                             | 120min        | Oct 05                 | B         |
| 23      | Create descriptions for flow diagrams                  | To make understanding the flow charts easier                                                                                                        | 60min         | Oct 05                 | B         |
# Criteria C: Development

## Code snippets

### Transaction system
Ms. Sato requires a system that the transactions made with the cryptocurrency used in the digital ledger. I thought about using a deposit and withdrawal system to fulfill this requirement, using a single function to facilitate both types of transactions.

In the first line, i am defining a function called 'transaction'. It has two inputs of type string, which are expected to be either 'deposit' or 'withdraw'. These are saved in the 'type' variable. In lines 2-3 the program provides the user with a numbered list encompassing the options 'Use XRP directly', 'USD', 'EUR', and 'JPY'. Then in lines 4-8 the program makes sure that the user's input which is set as the value of the 'currencies' variable is an integer from 1 to 4. This is done by using a while loop and the 'validate_int' library which is imported from 'my_lib.py'. If 'currencies' = 1 (Use XRP directly), the program asks the user enter the amount of XRP for the transaction, storing the input in the 'amount' variable. If 'currencies' = 2, 3, or 4 (fiat currency options), the program asks the user to enter the amount in the chosen currency and stores it in 'amount'. This is contained in lines 10-15. Next, the program checks which currency was chosen. If option 2 is selected (USD), the 'amount' is divided by the current exchange rate, converting it to XRP. If options 3 or 4 are selected (EUR or JPY), the currency_covert library makes the 'amount' variable converted to its USD counterpart, which is divided by the current exchange rate turning 'amount' into XRP. This is because the exchange rate of XRP is represented in USD terms, meaning EUR and JPY need to be converted to USD first before that is converted to XRP. This is contained in lines  16-20. Then in line 22 the program saves the current date in the 'date' variable by using the 'datetime' library. Next, the program checks whether the 'type' variable is equal to 'deposit' or 'withdraw'. If it is 'deposit', the variable 'line' is set to 'date' and 'amount', separated by a comma. This is decsribed in lines 23-24. If 'type' is equal to 'withdraw', the program first asks the user to input a reason and category of withdrawal, making sure they do not exceed 100 and 30 characters respectively by using a while loop. These inputs are stored in the 'description' and 'category' variables and are set as the value for 'line' along with the current date and a positive value of 'amount'. This process is described by lines 25-33. Finally the program uses the open command in line 34 to work with 'transactions.csv', it appends the 'line' variable to the csv file in line 35, and prints 'Saved' in line 36 so that the user knows the process was successful.

```.py
def transaction(type:str):  # type = "deposit" or "withdraw"
    currencies = ["Use XRP directly", "USD", "EUR", "JPY"]
    print_menu(currencies)
    currency = validate_int(msg=f"Please enter an option to {type} in XRP (1-4): ", menu="",
                            error_msg="[Error] Please enter valid option (1-4): ")
    while currency not in [1, 2, 3, 4]:
        currency = validate_int(msg=f"Please enter an option to {type} in XRP (1-4): ", menu="",
                                error_msg="[Error] Please enter valid option (1-4): ")
    print("")
    if currency == 1:
        amount = validate_int(msg=f"Please enter amount of XRP to {type}: ", menu="",
                              error_msg=f"[Error] Please enter valid amount to {type}: ")
    else:
        amount = validate_int(msg=f"Please enter amount of {currencies[currency - 1]} to {type} in XRP: ", menu="",
                              error_msg=f"[Error] Please enter valid amount to {type}: ")
    if currency == 2:
        amount /= float(rate[1:])
    if currency == 3 or currency == 4:
        amount = currency_convert(amount=amount, from_currency=currencies[currency - 1],
                                  to_currency="USD")/float(rate[1:])

    date = datetime.date.today()  # today's date
    if type == "deposit":
        line = f"{date},{amount}\n"
    if type == "withdraw":
        description = input("Please enter a short reason for withdrawal (e.g. 'bought a house')."
                            " Do not exceed 100 characters: ")
        while len(description) > 100:
            description = input("[Error] Exceeded 100 characters. Please enter a short reason for withdrawal: ")
        category = input("Please categorise the transaction (e.g. 'expenses' or 'food'). Do not exceed 30 characters: ")
        while len(category) > 30:
            category = input("[Error] Exceeded 30 characters. Please categorise the transaction: ")
        line = f"{date},{-amount},{description},{category}\n"
    with open('transactions.csv', mode='a') as f:
        f.writelines(line)
    print("Saved\n")
```

### Bar graph display system

Ms. Sato requires a system that records transactions and helps her keep track of how much cryptocurrency she has. I thought about using a bar graph display system to fulfill this requirement, since it displays the value of deposits compared to the value of withdrawals in an easy to understand manner.

The program begins by opening the 'transactions.csv' file in read mode ('r') and reads all lines from the file (lines 1-2). The data is stored in the 'data' variable, with each line representing a transaction. Next, the program initializes the 'deposits' and 'withdrawals' variables, setting their values to 0 (lines 3-4). Then, a for loop iterates through each line of 'data'. For each line, it uses split(",") to split the line into elements separated by commas. The date and amount are extracted from the line and stored in the 'date' and 'amount' variables. Then, an if/else statement is used to check if the value of 'amount' is greater or smaller than 0. If its greater (deposit) the value is added to 'deposits', and if its smaller (withdrawal) the absolute value is added to withdrawals (whole process described by lines 5-10). After that, the 'divisor' variable is initially set to 100 and is adjusted by a while loop making sure that the values of 'deposits' and 'withdrawals' divided by the divisor are less than or equal to 100 (lines 12-14). This is done to maintain a manageable graph. Next, the number of bars for deposits and withdrawals is calculated by dividing 'deposits' and 'withdrawals' by the divisor. Strings 'bar_deposits' and 'bar_withdrawals' are also initialized with a label and formatting for the graph (lines 15-18). Then, two for loops run to create a visual representation of the data using square blocks. The number of blocks represents the relative count of deposits and withdrawals (lines 19-22). Finally, the graph is printed in color. There is also a message indicating the value of each square block (23-25).

```.py
        with open('transactions.csv', mode='r') as f:
            data = f.readlines()
        deposits = 0
        withdrawals = 0
        for line in data:
            date, amount = line.strip().split(",")[0], line.strip().split(",")[1]
            if float(amount) > 0:
                deposits += float(amount)
            else:
                withdrawals += -1*float(amount)
        # create a simple graph
        divisor = 100
        while int(deposits // divisor) > 100 or int(withdrawals // 100) > 100:
            divisor *= 10
        deposits = int(deposits // divisor)
        withdrawals = int(withdrawals // divisor)
        bar_deposits = "deposits".ljust(20)
        bar_withdrawals = "withdrawals".ljust(20)
        for x in range(deposits):
            bar_deposits += "■"
        for x in range(withdrawals):
            bar_withdrawals += "■"
        print(colors(color="green", msg=f"{bar_deposits} {deposits}"))
        print(colors(color="red", msg=f"{bar_withdrawals} {withdrawals}"))
        print(colors(color="yellow", msg=f"■ = {divisor}XRP\n"))
```

### Withdrawal table display system

Ms. Sato requires a system that helps her keep track of transactions, including withdrawals. I thought about using a withdrawal table display system to fulfill this requirement, since it presents the data to the user in an organized manner.

The program begins by initializing the 'withdrawal_data' variable and setting its value as an empty list (line 1). The program proceeds to open the 'transactions.csv' file in read mode ('r') a reads all lines in the file. The data is stored in the 'data' variable, with each line representing a transaction (lines 2-3). Then, a for loop iterates through each line in 'data', using an if statement to check whether the line has 4 elements (indicating a withdrawal). If it does, the program spilts the line by comma and rearranges the second, third, and fourth elements to represent 'Description', 'Category', and 'Amount' respectively. 'Amount' is also changed by being negated, rounded to 2 decimal places, and reoresented in XRP. The modified line is then appended to the 'withdrawal_data' list (the whole process is contained within lines 4-9). Next, the column names for the table are defined in the 'col_names' variable (line 10). Finally, the 'tabulate' function from the 'tabulate' library is used to print 'withdrawal_data' in a table, with 'col_names' as the headers and 'fancy_grid' as the formatting style (line 11).

The task of putting data into a tabular format, which could have taken an hour or more to make by myself, took only around 3 minutes. This shows how useful external libraries are in programming and specifically in this code.

```.py
withdrawal_data = []
        with open('transactions.csv', mode='r') as f:
            data = f.readlines()
            for line in data:
                if len(line.split(",")) == 4:
                    line_a = line.split(",")
                    line_a[1], line_a[2], line_a[3] = (line_a[2], line_a[3].strip(),
                                                       str(round(-1*float(line_a[1]), 2)) + "XRP")
                    withdrawal_data.append(line_a)
        col_names = ["Date", "Description", "Category", "Amount"]
        print(tabulate(withdrawal_data, headers=col_names, tablefmt="fancy_grid"))
        print("")
```

## Sources

[XRP exchange rate](https://coinmarketcap.com/currencies/xrp/)

[XRP information](https://www.forbes.com/advisor/investing/cryptocurrency/what-is-ripple-xrp/)

[tabulate library](https://www.statology.org/create-table-in-python/)

[currency_converter library](https://pypi.org/project/CurrencyConverter/)

[Lucidchart](https://www.lucidchart.com)

