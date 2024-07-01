# Bank-Account-Management-System
# A Python bank account management system tracks transactions and balances, making banking easier and more efficient.

acountNo = 0

CusName = " "

BCode = " "

Mobile = 0

Bal = 0

def createAcounts():

    acountNo = int(input("Enter Account Number: "))
    
    CusName = input("Enter Customer Name: ")
    
    BCode = input("Enter Bank Code: ")
    
    Mobile = int(input("Enter Mobile Number: "))
    
    print("Account Created Successfully: ")

def ShowAcountDetails():

    print("AcountNo: ",acountNo)
    
    print("CusName: ",CusName)
    
    print("BCode: ",BCode)
    
    print("Mobile: ",Mobile)

def Deposite(amount):

    global Bal
    
    Bal = Bal + amount
    
    chckbalance()

def Withdraw(amount):

    global Bal
    
    Bal = Bal - amount
    
    chckbalance()

def chckbalance():

    print("Current Balance is:",Bal)

#_Main_#

print("1.Create Account\n2.Withdraw\n3.Deposite\n4.CheckBalance")

ch=int(input("Select any option:"))

if  (ch==1):

    createAcounts()
    
elif (ch==2):

    Withdraw(int(input("Enter Amount:")))
    
elif (ch==3):

    Deposite(int(input("Enter Amount:")))
    
elif (ch==4):

    chckbalance()
    
else:

    print("Invalid Option")

