# Target

Japanese vending machine Ver 2.0

# Important Things
- Maximize the learning outcomes of this workshop (mob programming)
- Solving all tasks is not first priority
- Driver and Navigator should be changed frequently. About 5-10 minutes is good
- TDD aims "Clean and working codes". Try refactoring!
- Items in Object list do not correcpond to each cycles of TDD
  - Let's clarify and devide the specifications to make it easy TDD
- Let's devide and refactor Objects, modules, classes, and methods frequently (e.g. VendingMachine, InventoryManagement, MoneyManegement, and so on)

# Tasks
## Step0: Insert money and refund it
- Can insert 10 yen coin, 50 yen coin, 100 yen coin, 500 yen coin, and 1000 yen bill
- Can insert coins and bills multiple times
- Can get total amount of inserted money
- Can refund
- Can output total amount of inserted money as refund money by refund operation

## Step1: Unhandled money
- When unexpected object (1 yen coin, 5 yen coin, bills except 1000 yen) is inserted, it will not be added to the total money and refund it to user

## Step2: Drink Management
- One type of drink which has "price" and "name" attributes can be stored
- As initial state, 5 Cokes (price: 120yen, name: "Coke") are stored
- Can get information (price, name, and amount) of stored drinks
- !!Caution!! : Doesn't Class have roles too much? If so, let's devide it!

## Step3: Purchase
- Can get whether Coke can be purchased or not in terms of inserted money and stock
- If "purchase" is executed when Coke can be purchased, reduce stock of Coke and increase sales amount
- If "purchase" is executed when Coke can NOT be purchased, do nothing
- Can get current sales amount
- If "refund" is executed, refund money ("Inserted money" - "Purchase price")
- !!Caution!! : Doesn't Class have roles too much? If so, let's devide it!

## Step4:　Feature　Extension
- Three types of drink can be stored
- Can be added RedBull (price: 200yen, name: "RedBull")
- Can be added Water (price: 100yen, name: "Water")
- Can get total amount of inserted money and list of purchasable drinks

## Step5: Refund Management Sales Management
- If "purchase" is executed when a drink can be purchased, output refund (the difference between inserted money and price of purchased drink)
  - If inserted money and price of purchased drink are same, output 0 yen as refund
  - You don't need to care the type of coin for refund

# References

- http://devtesting.jp/tddbc/?TDDBC%E5%A4%A7%E9%98%AA3.0%2F%E8%AA%B2%E9%A1%8C
