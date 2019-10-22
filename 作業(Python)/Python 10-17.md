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
```
# 21-5
def word_length(word1, word2):
    word = word1+word2
    return len(word)
    print("this never gets printed")
    
length1 = word_length("Rob", "Banks")
length2 = word_length("Barbie", "Kenn")
length3 = word_length("Holly", "Jolley")

print("One name is", length1, "letters long.")
print("Another name is", length2, "letters long.")
print("The final name is", length3, "letters long.")
```
```
One name is 8 letters long.
Another name is 10 letters long.
The final name is 11 letters long.
```
```
# 21-6
def add_sub(n1, n2):
    add = n1 + n2
    sub = n1 - n2
    return(add, sub)
(a, b)= add_sub(3, 4)
```
```
(Unknown answer)
```
```
# 21-7
def say_name(kid):
    print(kid)
def show_kid(kid):
    return kid
say_name("Dora")
show_kid("Ellie")
print(say_name("Frank"))
print(show_kid("Gus"))
```
```
Dora
Frank
None
Gus
```
```
# 21-8
def take_attendance(classroom, who_is_here):
    """
    classroom, tuple of strings
    who_is_here, tuple of strings
    Prints the names of all kids in class who are also in who_is_here
    Returns a string, "finished taking attendance"
    """
    for kid in classroom:
        if kid in who_is_here:
            print(kid)
    return "finished taking attendance"
help(take_attendance)
```
```
Help on function take_attendance in module __main__:

take_attendance(classroom, who_is_here)
    classroom, tuple of strings
    who_is_here, tuple of strings
    Prints the names of all kids in class who are also in who_is_here
    Returns a string, "finished taking attendance"


```
# CH-22
```
# 22-1
def fairy_tale():   
    peter = 5
    print(peter)   
peter = 30
fairy_tale()
print(peter)
```
```
5
30
```
```
# 22-2
def e():
    v = 5
    print(v)   
v= 1
e()
```
```
5
```
```
# 22-3
def f():
    print(v)
v= 1
f()
```
```
1
```
```
# 22-4
def g():
    print(v+x)  
v= 1
x= 2
g()
```
```
3
```
```
# 22-5
def h():
    v += 5   
v= 1
h()
```
```
UnboundLocalError                         Traceback (most recent call last)
<ipython-input-2-0b532e80723d> in <module>()
      3    v += 5
      4 v= 1
----> 5 h()

<ipython-input-2-0b532e80723d> in h()
      1 22-5
      2 def h():
----> 3    v += 5
      4 v= 1
      5 h()

UnboundLocalError: local variable 'v' referenced before assignment
```
```
# 22-6
def odd_or_even(num):
    num = num%2
    if num == 1:
        return "odd"
    else:
        return "even"
num = 4 
print(odd_or_even(num))   
odd_or_even(5)
```
```
even
'odd'
```
```
# 22-7
def sing():
    def stop(line):
        print("STOP", line)
    stop("it's hammer time")
    stop("in the name of love")
    stop("hey, what’s that sound")
sing()
stop()
```
```
NameError                                 Traceback (most recent call last)
<ipython-input-1-c843682fb486> in <module>()
      6     stop("hey, what’s that sound")
      7 sing()
----> 8 stop()

NameError: name 'stop' is not defined
```
```
# 22-8
def sandwich(kind_of_sandwich):
    print("--------")
    print(kind_of_sandwich())
    print("--------")
def blt():
    my_blt = " bacon\n lettuce\n tomato"
    return my_blt
def breakfast():
    my_ec = " eggegg\n cheese"
    return my_ec
print(sandwich(blt))
```
```
--------
 bacon
 lettuce
 tomato
--------
None
```
```
# 22-9
def grumpy():
    print("I am a grumpy cat:")
    def no_n_times(n): 
        print("No", n, "times...")
        def no_m_more_times(m): 
            print("...and no", m, "more times")
            for i in range(n+m):
                print("no")
        return no_m_more_times
    return no_n_times
grumpy()(4)(2)
```
```
I am a grumpy cat:
No 4 times...
...and no 2 more times
no
no
no
no
no
no
```
# CH-25
```
# 25-1
years = [1984, 1986, 1988, 1988]
print(len(years))
print(years.count(1988))
print(years.count(2017))
print(years.index(1986))
print(years.index(1988))
```
```
4
2
0
1
2
```
```
# 25-2
first3letters = []
first3letters.append("a")
first3letters.append("c")
first3letters.insert(1, "b")
print(first3letters)
last3letters = ["x", "y", "z"]
first3letters.extend(last3letters)
print(first3letters)
last3letters.extend(first3letters)
print(last3letters)
```
```
['a', 'b', 'c']
['a', 'b', 'c', 'x', 'y', 'z']
['x', 'y', 'z', 'a', 'b', 'c', 'x', 'y', 'z']
```
```
# 25-3
polite = ["please", "and", "thank", "you"]   
print(polite.pop())
print(polite)
print(polite.pop(1)) 
print(polite)
```
```
you
['please', 'and', 'thank']
and
['please', 'thank']
```
```
# 25-4
colors = ["red", "blue", "yellow"]
colors[0] = "orange"
print(colors)
colors[1] = "green"
print(colors)
colors[2] = "purple"
print(colors)
```
```
['orange', 'blue', 'yellow']
['orange', 'green', 'yellow']
['orange', 'green', 'purple']
```
# CH-26
```
# 26-1
heights = [1.4, 1.3, 1.5, 2, 1.4, 1.5, 1]

heights.reverse()  
print(heights)

heights.sort()  
print(heights)

heights.reverse()
print(heights)
```
```
[1, 1.5, 1.4, 2, 1.5, 1.3, 1.4]
[1, 1.3, 1.4, 1.4, 1.5, 1.5, 2]
[2, 1.5, 1.5, 1.4, 1.4, 1.3, 1]
```
```
# 26-2
L = [[], [], []]
L[0] = [1, 2, 3]
L[1].append('t')
L[1].append('o')
L[1][0] = 'd'
```
```
(Unknown answer.)
```
```
# 26-3
x = 'x' 
o = 'o'
e = '_'
board = [[x, e, o], [e, x, o], [x, e, e]]
```
```
(Unknown answer)
```
```
# 26-4
stack = []
cook = ['b', 'b', 'b']
stack.extend(cook)
stack.pop()
stack.pop()
cook = ['c', 'c']
stack.extend(cook)
stack.pop()
cook = ['b', 'b']
stack.extend(cook)
stack.pop()
stack.pop()
stack.pop()
```
```
(Unknown answer)
```
```
# 26-5
line = []
line.append('Ana')
line.append('Bob')
line.pop(0)
line.append('Claire')
line.append('Dave')
line.pop(0)
line.pop(0)
line.pop(0)
```
```
(Unknown answer)
```
# CH-27
```
# 27-1
legs = {} 
legs["human"] = 2
legs["cat"] = 4
legs["snake"] = 0
print(len(legs))
legs["cat"] = 3
print(len(legs))
print(legs)
```
```
3
3
{'human': 2, 'cat': 3, 'snake': 0}
```
```
# 27-2
household = {"person":4, "cat":2, "dog":1, "fish":2}
removed = household.pop("fish")
print(removed)
```
```
2
```
```
# 27-3
grades = {}
grades["Chris"] = [100, 70]
grades["Angela"] = [90, 100]
grades["Bruce"] = [80, 40]
grades["Stacey"] = [70, 70]
for student in grades.keys():
    print(student)
for quizzes in grades.values():
    print(sum(quizzes)/2)
for student in grades.keys():
    scores = grades[student]
    grades[student].append(sum(scores)/2)
print(grades)
```
```
Chris
Angela
Bruce
Stacey
85.0
95.0
60.0
70.0
{'Chris': [100, 70, 85.0], 'Angela': [90, 100, 95.0], 'Bruce': [80, 40, 60.0], 'Stacey': [70, 70, 70.0]}
```
```
Chris
Angela
Bruce
Stacey
85.0
95.0
60.0
70.0
{'Chris': [100, 70, 85.0], 'Angela': [90, 100, 95.0], 'Bruce': [80, 40, 60.0], 'Stacey': [70, 70, 70.0]}
```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
