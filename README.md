# Bank
Multi threaded java program which uses BlockingQueue interface to handle communication between the main thread and the worker threads. 

The bank tracks the balances in twenty different accounts. When the program begins, each of the accounts contains $1000. The program process a list of transactions which transfer money between the accounts. Once all transactions are processed the program goes through and for each account it prints both the account’s final balance and the number of transactions (deposits and withdrawals) which occurred on that account.

The bank program uses the main thread to read the list of banking transactions from a file. A separate set of worker threads processes the transactions and update the accounts. Java’s BlockingQueue handles most of the communication between the main thread and the worker threads.

File format: Each line in the external file represents a single transaction, and contains three numbers: the id of the account from which the money is being transferred, the id of the account to which the money is going, and the amount of money. For example the line:

17 6 104

indicates that $104 is being transferred from Account #17 to Account #6.

small.txt, 5k.txt and 100k.txt are tester files.
