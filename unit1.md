![](-----.jpg)
# Unit1: A electronic hardware store

## Criteria A : Planning

### Context of the problem 
There is a hardware store in Karuizawa. This store is quite old, like 1000 years old. The owner, Mr Sakamoito, wants to upgrade his accounting software, which at the moment is kept on paper. He would like to have a software application the places the accounting book. Mr.Sakiamoto got a new Mac PC from his nephew, and we would like to use it.


### Justisification of the solution
***Here we will write the design statement: what will do, how, by when***
we want to create a text based applicatgion that runs on a computer, which provides the functionality for the hardware store. The app should provide action such as record of puchases, categorization of items, record of inventory, calculation of totals, billing. We will develop this applicatiopn using python because it is  the software we are using in class at the moment. In comparison to C++ or C, pyuthon has a learn and simple programming syntax.In addition Python has become the most popular programmming language over the last years. Python has a large repository of libraries and documents.

T(techonological).E(economic).L.O.S study:

[1] MLA citation for the data supporting that Pthon is the most popular programming language.

## Criteria for Sucess

1. Provides clear feedback to the user (Usability)
2. ***There are no bugs in the application***
3. The application should allow to calculate the total and billing
4. Secure application: It allows user login/autenthication

## Criteria B: Design

![](https://github.com/kazuto-abe/CS2020/blob/master/Computer%20science_software%20organization.001.jpeg?raw=true)

### System diagram

![](https://github.com/kazuto-abe/CS2020/blob/master/Flow%20diagram__sakamoto_store.jpg?raw=true)

## Criteria: C :Development

First test of text based menu:

```.py
from datetime import datetime

date = datetime.today()

print('Welcome to Mr.Sakamoto Store Sep 4 10:29 {}'.format(date))
print("What is your name?")
name = input()
print("Hi" + " " + name + "!!")

# create a list of menu
print("This is the menu")
print("=" * 20)

print("1.{}  {}".format("Ram","3$")) 
print("2.{}  {}".format("CPU","5$")) 
print("3.{}  {}".format("Motherboard","5$")) 
print("4.{}  {}".format("GPU","8$"))

print("=" * 20)

for i in range(3):
  options =int(input("Which option do you want to get.  "))
  if options == 1 :
    print ("You chose RAM")
    break
  if options == 2 :
    print ("You chose CPU")
    break
  if options == 3 :
    print ("You chose Motherboard")
    break
  if options == 4 :
    print ("You chose GPU")
    break
  else :
    print ("Please chose a number from the list above")
```
Program to calculate the tax:

Table:
| Rate | Bill total          |
|:----:|---------------------|
| 5%   | >1000 BTC           |
| 10%  | 750 < total <= 1000 |
| 15%  | 500 < total <= 750  |
| 20%  | 250 < total <= 500  |
| 25%  | 0 < total <= 250    |

```.py
#This program calculates the taxes

while True:
  total = int(input("Please enter the total amount of BTC:  "))
  if total < 0: 
    print("The total cannot be negative. Try again")
  else:
    break

# Step2: Without using pattern recognition

for i in [0,1,2,3,4]:
  if 250 * i < total <= 250 * i + 250:
    tax = 0.25 - 0.05 * i
  if total > 1000:
    tax = 0.25
```


Warm up activity 

``` py
# This program calculates the sum of even number

sum = 0
for number in range(1000):
  if number%2 ==0 :
    sum += number

print("THe addtion is {}".format(sum))

# Write a program that ask for the first name and last Name
# and create 10 email adresses in the UWCisak domein

import random
print("what is your last name")
lastname = str(input())

print("what is your  first name")
firstname = str(input())

for email in range(10):
  print("{}.{}{}@uwcisak.jp". format(lastname, firstname, random.randint(0,10)))

```
#### Dice simulation

```.py
import random
import matplotlib.pyplot as plt
counts = [0, 0, 0, 0, 0, 0]
num_trial = 2000
for trial in range(num_trial):
  number = random.randint(0,60)
  if number < 9:
    counts[0] += 1
  elif 9 < number < 20:
    counts[1] += 1
  elif 19 < number < 30:
    counts[2] += 1
  elif 29 < number < 40:
    counts[3] += 1
  elif 39 < number < 50:
    counts[4] += 1
  elif 49 < number < 60:
    counts[5] += 1

for index, c in enumerate(counts):
  error = c - num_trial/6
  print("Number of {}s: {},expected {}, error {}".format(index+1, c, num_trial / 6,error))
```
#### Slices

```.py
a = str(input())
print(a[2])   #print the third character of this string
print(a[-2])  #print the second to last character of this string
print(a[:5])  #print the first five characters of this string
print(a[0:-2])#print all but the last two characters of this string
print(a[::2]) #print all the characters of this string with even indices
print(a[1::2])#print all the characters of this string with odd indices
print(a[::-1])#print all the characters of the string in reverse order
print(a[::-2])#print every second character of the string in reverse order, starting from the last one
print(len(a)) #print the length of the given string
```

#### Count to N

It says "This problem is available only for teachers who have a subscription and for their students." :((

#### Series - 1 (using if statement)

```.py
a = int(input("Please input a number "))
b = int(input("Please input a number, but it has to be equal or larger"))

if a <= b:
    for i in range (a, b + 1):
        print(i)
else:
    print("Please keep following conditions above")

```

#### Task for HL

Create a program that asks the user for 10 numbers and then shows those values ordered from smallest to largest.

```.py
num = (input("Please enter 10 numbers ex. 8  3  1  5  6  ... : \n "))

sorted_num = sorted(num.split())
print("This is the list of ordered numbers : \n {}" .format (sorted_num))
```
Warm up activity 8/11/ 2020

```.py
#program generates the patterns 0123401234

#step1
number_repetition = int(input("please enter number:  "))

#step2
count = 0
for i in range(number_repetition):
  print(count)
  count = count + 1
  if count == 4:
    count = 0
```
