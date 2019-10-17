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
Where do you live? <Tainan>
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
Where do you live? <kaohsiung>
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
Enter a number to find the square of:< 2>
Enter a integer to find the square of: <6>
36
```
```
# 10-6
num1 = float(input("Enter a number: "))
num2 = float(input("Enter another number: "))
print(num1, "*", num2, "=", num1*num2)
```
```
Enter a number: <8>
Enter another number:<4>
8.0 * 4.0 = 32.0
```
# CH13
```
# 13-1
num = int(input("Enter a number: "))
if num > 0:
    print("num is positive")
print("finished comparing num to 0") 
```
```
>>> %Run 1.py
Enter a number: <6>
num is positive
finished comparing num to 0
>>> %Run 1.py
Enter a number: <-1>
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
