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
```
# 16-3
secret = "code"
max_tries = 100
guess = input("Guess a word: ")
tries = 1
while guess != secret:
    print("You tried to guess", tries, "times")
    if tries == max_tries:
        print("You ran out of tries.")
        break
    guess = input("Guess again: ")
    tries += 1
if tries <= max_tries and guess == secret:
    print("You got it!")
```
```
>>> %Run 1.py
Guess a word: e
You tried to guess 1 times
Guess again: s
You tried to guess 2 times
Guess again: xxs'
You tried to guess 3 times
Guess again: code
You got it!
>>> %Run 1.py
Guess a word: uUU
You tried to guess 1 times
Guess again: f
You tried to guess 2 times
Guess again: f
You tried to guess 3 times
Guess again: f
You tried to guess 4 times
Guess again: f
.
.
.
.
.
.
You tried to guess 97 times
Guess again: d
You tried to guess 98 times
Guess again: d
You tried to guess 99 times
Guess again: d
You tried to guess 100 times
You ran out of tries.
```
```
# 16-4
i= 1
while(i < 10):
    if i == 5:
        i += 1
        continue
    print(i, end=' ')
    i += 1
print("End")
```
```
1 2 3 4 6 7 8 9 End
```
```
# 16-5
s = "" 
while s != "喵喵":
    if s != "":
        print(" 不對喔!")
    s = input(" 請輸入通關密語:")
    if s == "out":
        break
else: 
    print(" 恭喜你過關了 ")
print(" 再見!")
```
```
 請輸入通關密語:X86 IS THE BEST.
 不對喔!
 請輸入通關密語:ARMV8 IS THE BEST.
 不對喔!
 請輸入通關密語:喵喵
 恭喜你過關了 
 再見!
```
# CH-17
```
# 17-1-1不使用迴圈
print("Hello Python")
print("Hello Python")
print("Hello Python")
print("Hello Python")
print("Hello Python")
print("Hello Python")
print("Hello Python")
print("Hello Python")
print("Hello Python")
print("Hello Python")
```
```
Hello Python
Hello Python
Hello Python
Hello Python
Hello Python
Hello Python
Hello Python
Hello Python
Hello Python
Hello Python
```
```
# 17-1使用for迴圈
for i in range(10):
    print("Hello Python")
```
```
Hello Python
Hello Python
Hello Python
Hello Python
Hello Python
Hello Python
Hello Python
Hello Python
Hello Python
Hello Python
```
```
# 17-3
for i in range(10, 1, -1):
    print(i, end=" ")
print()
for i in range(0, 9, 2): 
    print(i, end=" ") 

```
```
10 9 8 7 6 5 4 3 2 
0 2 4 6 8
```
```
# 17-4
for i in range(1, 10):
    for j in range(1, 10):
        print(j, "x", i, "=", j*i, end=' ')
    print()
```
```
1 x 1 = 1 2 x 1 = 2 3 x 1 = 3 4 x 1 = 4 5 x 1 = 5 6 x 1 = 6 7 x 1 = 7 8 x 1 = 8 9 x 1 = 9 
1 x 2 = 2 2 x 2 = 4 3 x 2 = 6 4 x 2 = 8 5 x 2 = 10 6 x 2 = 12 7 x 2 = 14 8 x 2 = 16 9 x 2 = 18 
1 x 3 = 3 2 x 3 = 6 3 x 3 = 9 4 x 3 = 12 5 x 3 = 15 6 x 3 = 18 7 x 3 = 21 8 x 3 = 24 9 x 3 = 27 
1 x 4 = 4 2 x 4 = 8 3 x 4 = 12 4 x 4 = 16 5 x 4 = 20 6 x 4 = 24 7 x 4 = 28 8 x 4 = 32 9 x 4 = 36 
1 x 5 = 5 2 x 5 = 10 3 x 5 = 15 4 x 5 = 20 5 x 5 = 25 6 x 5 = 30 7 x 5 = 35 8 x 5 = 40 9 x 5 = 45 
1 x 6 = 6 2 x 6 = 12 3 x 6 = 18 4 x 6 = 24 5 x 6 = 30 6 x 6 = 36 7 x 6 = 42 8 x 6 = 48 9 x 6 = 54 
1 x 7 = 7 2 x 7 = 14 3 x 7 = 21 4 x 7 = 28 5 x 7 = 35 6 x 7 = 42 7 x 7 = 49 8 x 7 = 56 9 x 7 = 63 
1 x 8 = 8 2 x 8 = 16 3 x 8 = 24 4 x 8 = 32 5 x 8 = 40 6 x 8 = 48 7 x 8 = 56 8 x 8 = 64 9 x 8 = 72 
1 x 9 = 9 2 x 9 = 18 3 x 9 = 27 4 x 9 = 36 5 x 9 = 45 6 x 9 = 54 7 x 9 = 63 8 x 9 = 72 9 x 9 = 81 
```
```
# 17-5
for i in range(1, 20):
    if i == 5:
        continue
    print(i, end=" ")
    if i == 10:
        break
print("END")
```
```
1 2 3 4 6 7 8 9 10 END
```
```
# 17-6
num = int(input("Please specify the range(0~N): "))
for i in range(2, num+1):   
    for j in range(2, i):
        if(i%j == 0): 
            break 
    else: 
        print(i)
```
```
Please specify the range(0~N): 13
2
3
5
7
11
13
```
# CH-18
```
# 18-1
for ch in "Python is fun!":
    print("the character is", ch) 
```
```
the character is P
the character is y
the character is t
the character is h
the character is o
the character is n
the character is  
the character is i
the character is s
the character is  
the character is f
the character is u
the character is n
the character is !
```
```
# 18-2
my_string = "Python is fun!"
len_s = len(my_string)
for i in range(len_s):
    print("the character is", my_string[i]) 
```
```
the character is P
the character is y
the character is t
the character is h
the character is o
the character is n
the character is  
the character is i
the character is s
the character is  
the character is f
the character is u
the character is n
the character is !
```
```
# 18-3
winners =("Peter", "Mark", "Joy")
print(" 恭喜以下得獎人:")
for name in winners:
    print(name)
```
```
恭喜以下得獎人:
Peter
Mark
Joy
```
```
# 18-4
prizes =(" 頭獎 ", " 二獎 ", " 三獎 ")
winners =("Peter", "Mark", "Joy")
print(" 恭喜以下得獎人:")
for i in range(3):
    print(prizes[i]+ ":" + winners[i]) 
```
```
恭喜以下得獎人:
 頭獎 :Peter
 二獎 :Mark
 三獎 :Joy
 ```
 ```
 # 18-5
winners =((" 頭獎 ", "Peter"),(" 二獎 ", "Mark"),(" 三獎 ", "Joy"))
print(" 恭喜以下得獎人:")
for e in winners: 
    print(e[0]+ ":" + e[1])
 ```
 ```
 恭喜以下得獎人:
 頭獎 :Peter
 二獎 :Mark
 三獎 :Joy
 ```
 ```
 # 18-6
winners =((" 頭獎 ", "Peter"),(" 二獎 ", "Mark"),(" 三獎 ", "Joy"))
print(" 恭喜以下獎人:")
for prize, winner in winners:
    print(prize+ ":" + winner) 
 ```
 ```
 恭喜以下獎人:
 頭獎 :Peter
 二獎 :Mark
 三獎 :Joy
 ```
 ```
 # 18-7for迴圈
for x in range(3):
    print("var x is", x)
 ```
 ```
 var x is 0
var x is 1
var x is 2
 ```
 ```
 # 18-7while迴圈
 x = 0
while x < 3:
    print("var x is", x)
    x += 1
```
# CH-19
```
# 19-1
words = """art
hue
ink
...
crosshatching
"""
tiles = "hijklmnop"
all_valid_words =()
start = 0
end = 0
found_words =()   
```
```
(Unknown answer.)
```
```
# 19-2
words = """art hue
ink
...
crosshatching
"""
tiles = "hijklmnop"
all_valid_words =()
start = 0
end = 0
found_words =() 

for char in words:
    if char == "\n":
        all_valid_words = all_valid_words +(words[start:end], )
        start = end + 1
        end = end +1
    else:
        end = end + 1 
```
```
(Unknown answer.)
```
```
# 19-3
words = """art hue
ink
...
crosshatching
"""
tiles = "hijklmnop"
all_valid_words =()
start = 0
end = 0
found_words =() 

for char in words:
    if char == "\n":
        all_valid_words = all_valid_words +(words[start:end], )
        start = end + 1
        end = end +1
    else:
        end = end + 1

for word in all_valid_words:
    tiles_left = tiles
for letter in word:
    if letter not in tiles_left:
        break
    else:
        index = tiles_left.find(letter)
        tiles_left = tiles_left[:index]+tiles_left[index+1:]
    if len(word)== len(tiles)-len(tiles_left):
        found_words = found_words +(word, )
print(found_words)
```
```
()
```
# CH-20
```
# 20-1
a= 1
b= 2
print(a+b)
print(a-b)
print(a*b)
print(a/b)
```
```
3
-1
2
0.5
```
```
# 20-2
a= 1
b= 2
print(a+b)
print(a-b)
print(a*b)
print(a/b)
a= 3
b= 4
print(a+b)
print(a-b)
print(a*b)
print(a/b)
a= 5
b= 6
print(a+b)
print(a-b)
print(a*b)
print(a/b)
```
```
3
-1
2
0.5
7
-1
12
0.75
11
-1
30
0.8333333333333334
```
# CH-21
```
# 21-1
def take_attendance(classroom, who_is_here):
    """
    classroom, tuple
    who_is_here, tuple
    Checks if every item in classroom is in who_is_here
    And prints their name if so.
    Returns "finished taking attendance"
    """
    for kid in classroom:
        if kid in who_is_here:
            print(kid)   
    return "finished taking attendance"
```
```
(Unknown answer.)
```
```
# 21-2
def hello():
    print('Hello!')

hello()
def sayHi(name, title):
    print(name + title +' 你好!')
sayHi(' 王小明 ', ' 同學 ')
```
```
Hello!
 王小明  同學  你好!
```
```
# 21-3
sayHi(' 王小明 ', title=' 同學 ')
sayHi(title=' 同學 ', name=' 王小明 ')
sayHi(title=' 同學 ', ' 王小明 ')
```
```
(SyntaxError: positional argument follows keyword argument)
```
```
# 21-4
def get_word_length(word1, word2): 
    word = word1+word2  
    return len(word) 
    print("this never gets printed") 
```
```
(Unknown answer)
```
