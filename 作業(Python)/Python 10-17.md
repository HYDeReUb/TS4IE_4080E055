# CH-10
```
# 10-1
print("hello!")
print(3*2*(17-2.1))
print("abc"+"def")
word = "art"
print(word.replace("r", "n"))
```
```
hello!
89.4
abcdef
ant
```
```
# 10-2
a= 1
b= 2
c = a/b
print(a, "/", b, "=", c) 
add = str(a)+"/"+str(b)+"="+str(c)
print(add)
```
```
1 / 2 = 0.5
1/2=0.5
```
```
# 10-3
input("Where do you live? ")
print("I live in Boston. ")
```
```
Where do you live?  Tainan
I live in Boston. 
```
```
# 10-4
user_place = input("Where do you live? ")
text = user_place.capitalize()+ "!"
print(text) 
print("I hear it's nice there!") 
```
```
Where do you live?  kaohsiung
Kaohsiung!
I hear it's nice there!
```
```
# 10-5
num = int(input ("Enter a number to find the square of: "))
user_input = input("Enter a integer to find the square of: ")
num = int(user_input) 
print(num*num)
```
```
Enter a number to find the square of: 2
Enter a integer to find the square of: 6
36
```
```
# 10-6
num1 = float(input("Enter a number: "))
num2 = float(input("Enter another number: "))
print(num1, "*", num2, "=", num1*num2)
```
```
Enter a number: 8
Enter another number: 4
8.0 * 4.0 = 32.0
```
# CH-13
```
# 13-1
num = int(input("Enter a number: "))
if num > 0:
    print("num is positive")
print("finished comparing num to 0") 
```
```
>>> %Run 1.py
Enter a number: 6
num is positive
finished comparing num to 0
>>> %Run 1.py
Enter a number: -1
finished comparing num to 0
```
```
# 13-2
num_a = int(input("Pick a number: "))   
if num_a > 0:
    print("Your number is positive")   
if num_a < 0:
    print("Your number is negative ") 
if num_a == 0: 
    print("Your number is zero")
print("Finished!")
```
```
>>> %Run 1.py
Pick a number: 1
Your number is positive
Finished!
>>> %Run 1.py
Pick a number: -1
Your number is negative 
Finished!
>>> %Run 1.py
Pick a number: 0
Your number is zero
Finished!
```
```
# 13-3非巢狀條件式
num_a = int(input("Number? "))
num_b = int(input("Number? "))
if num_a < 0:
   print("num_a is negative") 
if num_b < 0:
    print("num_b is negative")
print("Finished")
```
```
>>> %Run 1.py
Number? 5
Number? 2
Finished
>>> %Run 1.py
Number? -8
Number? -4
num_a is negative
num_b is negative
Finished
```
```
# 13-3巢狀條件式
num_a = int(input("Number? "))
num_b = int(input("Number? "))
if num_a < 0:      
    print("num_a is negative")
    if num_b < 0:
        print("num_b is negative")
print("Finished")
```
```
>>> %Run 1.py
Number? 5
Number? 5
Finished
>>> %Run 1.py
Number? -1
Number? -1
num_a is negative
num_b is negative
Finished
```
```
# 13-4
price = float(input("How much does a chocolate bar cost? "))
hungry = input("Are you hungry(yes or no)? ")

bars = 0
if hungry == "yes": 
    if price < 10:
        print("Buy all chocolate bars.")
        bars = 100
    if 10 <= price <= 50:
        print("Buy 10 chocolate bars.")     
        bars = 10
    if price > 50:
        print("Buy only one chocolate bar.")
        bars = 1
if hungry == "no":
    print("Stick to the shopping list.")
if bars > 10:
    print("Cashier says: someone's hungry!")
    ```
    ```
    >>> %Run 1.py
How much does a chocolate bar cost? 5
Are you hungry(yes or no)? yes
Buy all chocolate bars.
Cashier says: someone's hungry!
>>> %Run 1.py
How much does a chocolate bar cost? 10
Are you hungry(yes or no)? yes
Buy 10 chocolate bars.
>>> %Run 1.py
How much does a chocolate bar cost? 51
Are you hungry(yes or no)? yes
Buy only one chocolate bar.
>>> %Run 1.py
How much does a chocolate bar cost? 5
Are you hungry(yes or no)? no
Stick to the shopping list.
```
```
# 13-5
num_a = int(input("pick a number:"))
num_b = int(input("pick a number:"))
if num_a < 0 and num_b < 0: 
    print("both negative")
```
```
pick a number:-1
pick a number:-1
both negative
```
# CH-14
```
# 14-1
Num=int(input("please pick a number: "))
if Num%2==0:
    print("Even Number")
else:
    print("Odd Number")
```
```
>>> %Run 1.py
please pick a number: 8
Even Number
>>> %Run 1.py
please pick a number: 3
Odd Number
```
```
# 14-2
num = int(input("Enter a number: "))
if num > 0:
    print("num is positive")
elif num < 0:
    print("num is negative")
else:
    print("num is zero")
```
```
>>> %Run 1.py
Enter a number: 5
num is positive
>>> %Run 1.py
Enter a number: -1
num is negative
>>> %Run 1.py
Enter a number: 0
num is zero
```
```
# 14-3
num_a = int(input("pick a number: "))
num_b = int(input("pick another number: "))
lucky_num = 7
if num_a==num_b:
    print("You enter the same number")
else:
    if num_a > 0 and num_b > 0:
        print("both numbers are positive")
    elif num_a < 0 and num_b < 0:
        print("both numbers are negative")
    else:
        print("numbers have opposite sign")
if num_a == lucky_num or num_b == lucky_num:
    print("you also guessed my lucky number!")
else:
    print("I have a secret number in mind...")
```
```
>>> %Run 1.py
pick a number: 4
pick another number: 4
You enter the same number
I have a secret number in mind...
>>> %Run 1.py
pick a number: -1
pick another number: -8
both numbers are negative
I have a secret number in mind...
>>> %Run 1.py
pick a number: 4
pick another number: 7
both numbers are positive
you also guessed my lucky number!
>>> %Run 1.py
pick a number: 5
pick another number: 2
both numbers are positive
I have a secret number in mind...
```
```
隨機取數版本
# 14-3
import random
lucky_num = random.randint(0,9)
num_a = int(input("pick a number: "))
num_b = int(input("pick another number: "))
if num_a==num_b:
    print("You enter the same number")
else:
    if num_a > 0 and num_b > 0:
        print("both numbers are positive")
    elif num_a < 0 and num_b < 0:
        print("both numbers are negative")
    else:
        print("numbers have opposite sign")
if num_a == lucky_num or num_b == lucky_num:
   print("You guess it! The lucky number is",lucky_num)
else:
    print("I have a secret number in mind...")
```
```
>>> %Run 1.py
pick a number: 7
pick another number: 2
both numbers are positive
you also guessed my lucky number!
>>> %Run 1.py
pick a number: 5
pick another number: 2
both numbers are positive
I have a secret number in mind...
>>> %Run 1.py
pick a number: 8
pick another number: 2
both numbers are positive
I have a secret number in mind...
>>> %Run 1.py
pick a number: 7
pick another number: 6
both numbers are positive
I have a secret number in mind...
>>> %Run 1.py
pick a number: 9
pick another number: 2
both numbers are positive
I have a secret number in mind...
>>> %Run 1.py
pick a number: 1
pick another number: 5
both numbers are positive
I have a secret number in mind...
>>> %Run 1.py
pick a number: 6
pick another number: 3
both numbers are positive
I have a secret number in mind...
>>> %Run 1.py
pick a number: 7
pick another number: 6
both numbers are positive
I have a secret number in mind...
>>> %Run 1.py
pick a number: 0
pick another number: 2
numbers have opposite sign
You guess it! The lucky number is 2
```
```
>>> %Run 1.py
Say hi in English or Spanish! Hi
Enter 1 or 2: 1
You speak English!
one
>>> %Run 1.py
Say hi in English or Spanish! hello
Enter 1 or 2: 2
You speak English!
two
>>> %Run 1.py
Say hi in English or Spanish! hola
Enter 1 or 2: 2
You speak Spanish!
dos
>>> %Run 1.py
Say hi in English or Spanish! Hola
Enter 1 or 2: 1
You speak Spanish!
uno
```
# CH-16
```
# 16-1
s = input(" 請輸入顯示內容 : ")
n = int(input(" 請輸入顯示次數 : "))
while n > 0:
    print(s)
    n = n-1
```
```
 請輸入顯示內容 : 9
 請輸入顯示次數 : 5
9
9
9
9
9
```
```
# 16-2
lucky_num = 77
guess = int(input("Guess a Number(0-99): "))
tries = 1
while guess != lucky_num:
    print("You tried to guess", tries, "times")
    guess = int(input("Guess again: "))
    tries += 1
print("You got it!")
```
```
Guess a Number(0-99): 8
You tried to guess 1 times
Guess again: 6
You tried to guess 2 times
Guess again: 77
You got it!
```
