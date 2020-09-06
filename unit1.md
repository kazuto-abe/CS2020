# Unit1: A electronic hardware store

## Criteria A : Planning

### Context of the problem 
There is a hardware store in Karuizawa. This store is quite old, like 1000 years old. The owner, Mr Sakamoito, wants to upgrade his accounting software, which at the moment is kept on paper. He would like to have a software application the places the accounting book. Mr.Sakiamoto got a new Mac PC from his nephew, and we would like to use it.


### Justisification of the solution
***Here we will write the design statement: what will do, how, by when***

## Development

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

print("Which option do you want to get.  ")
options = int(input())

for i in range(3):
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
    options =int(input("Which option do you want to get.  "))
```
