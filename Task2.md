## Programming task

Task1
```.py
# Task1 Create a program that shows the color of all the lockers from 1 to 2400

color_list = ["red", "white", "yellow", "blue"] * 600

for i in range(2400):
  print("Locker number: {} \n Color of locker: {} ".format(i + 1, color_list[i]))
```

Task2
```.py
# Task2 Using the program above, create another program that allows thee user to enter a number and the program outputs the color that should be used in the locker.

user = int(input("Please enter your locker number \n"))

if user % 4 == 1:
  print("The color is ... Red")
if user % 4 == 2:
  print("The color is ... white")
if user % 4 == 3:
  print("The color is ... yellow")
if user % 4 == 0:
  print("The color is ... blue")
```

Task3
Still developing...
