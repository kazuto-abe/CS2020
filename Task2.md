## Programming task

Task1
```.py
# Task1 Create a program that shows the color of all the lockers from 1 to 2400

num = 0
for i in range(0,2401):
  num += 1
  if i % 4 == 1:
    print("Locker number: {} \n Color of locker: RED ".format(i))
  if i % 4 == 2:
    print("Locker number: {} \n Color of locker: WHITE ".format(i))
  if i % 4 == 3:
    print("Locker number: {} \n Color of locker: YELLOW ".format(i))
  if i % 4 == 0:
    print("Locker number: {} \n Color of locker: BLUE ".format(i))
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
