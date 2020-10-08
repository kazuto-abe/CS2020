#### Warmup activity

```.py
number = (input("enter the numbers ex.. 4156980:  "))

devided_num = str(number)
print(devided_num)

first_num = number[0:3]
last_num = number[3:]

print (first_num, last_num)

add_first = 0
for f in first_num:
  add_first += int(f)

add_last = 0
for l in last_num:
  add_last += int(l)
print(add_first == add_last)
```

#### Warm up activity2 

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
#### Warmup acitivity3

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
```.py
msg = input("enter a message:  ")
n = int(input("Put an integer:  "))

encrypted_msg = ""

for i in msg :
  i = chr(ord(i) + n)
  encrypted_msg += i # concatenate text

print(msg + " → " + encrypted_msg)
```

#### judge whether users input perfect number or not

```.py
num = int(input("please enter a number:   "))

sum = 0
for i in range(num - 1, 1, -1):
  if num % i == 0:
    sum += i
    print(i,"it is a factor")

sum_factor = sum + 1
print("This is sum of factor: {}".format(sum_factor))

if sum_factor == num :
  print("You chose perfect number")
else:
  print("You did not chose perfect number")
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

