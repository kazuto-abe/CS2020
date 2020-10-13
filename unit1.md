![](-----.jpg)
# Unit1: A electronic hardware store

## Criteria A : Planning

### Context of the problem 
There is a hardware store in Karuizawa. This store is quite old, like 1000 years old. The owner, Mr Sakamoito, wants to upgrade his accounting software, which at the moment is kept on paper. He would like to have a software application the places the accounting book. Mr.Sakiamoto got a new Mac PC from his nephew, and we would like to use it.


### Justisification of the solution
***Here we will write the design statement: what will do, how, by when***
we want to create a text based applicatgion that runs on a computer, which provides the functionality for the hardware store. The app should provide action such as record of puchases, categorization of items, record of inventory, calculation of totals, billing. We will develop this applicatiopn using python because it is  the software we are using in class at the moment. In comparison to C++ or C, pyuthon has a learn and simple programming syntax.In addition Python has become the most popular programmming language over the last years. Python has a large repository of libraries and documents.

T.E.L.O.S study: Technological, Economic, Legal, Organiational, Scheduling.

[1] MLA citation for the data supporting that Pthon is the most popular programming language.

## Criteria for Sucess

1. Provides clear feedback to the user (Usability)
2. ***There are no bugs in the application***
3. The application should allow to calculate the total and billing
4. Secure application: It allows user login/autenthication

## Criteria B: Design

### Record of the task

| Task No |                                              Planned Action                                             |          Planned  Outcome         | Time Estimated | Target Completion Date  | Criterion |
|:-------:|:-------------------------------------------------------------------------------------------------------:|:---------------------------------:|:--------------:|:-----------------------:|:---------:|
|    1    | Planning: discuss the context of the situation. (Ideally this is the first interview with your client)  |   Write a context of the problem  |      15min     |         Sep 11th        |     A     |
|    2    |             Development: Coded a text-based menu system for some parts in the hardware store            | A working program that shows menu |      80min     |         Sep18th         |     C     |
|    3    |             Design: Create a flow diagram for the menu program            | Easy to understand and follow how the program works |      20min     |         Sep15th         |     B     |

### System diagram

![](https://github.com/kazuto-abe/CS2020/blob/master/Computer%20science_software%20organization.001.jpeg?raw=true)

### Flow diagram

![](https://github.com/kazuto-abe/CS2020/blob/master/Flow%20diagram__sakamoto_store.jpg?raw=true)

## Criteria: C :Development

First test of text based menu:

```.py
# Get the information about year, month,date, and minute time.
from datetime import datetime
date = datetime.today()

print('Welcome to Mr.Sakamoto Store {}'.format(date))
# Let users enter their name
print("What is your name?")
name = input()
print("Hi" + " " + name + "!!")

# create a list of menu
print("This is the menu")
print("=" * 20)

print("1.{}  {}".format("Ram","3BTC"))
print("2.{}  {}".format("CPU","5BTC"))
print("3.{}  {}".format("Motherboard","5BTC"))
print("4.{}  {}".format("GPU","8BTC"))

print("=" * 20)

# Loop back 3 times maximum if the user put wrong option
for i in range(3):
  options =int(input("Which option do you want to get.  "))
  if options == 1:
    print("You chose RAM")
    while True:
        num_ram = int(input("How many RAMs you would purchase "))
        # Loop back if the user enter the negative integer
        if num_ram > 0:
            print("Your total amount of RAMs are {}.".format(num_ram))
            break
        else:
            print("Please input a POSITIVE integer")
    break
  if options == 2 :
    print("You chose CPU")
    while True:
        num_cpu = int(input("How many CPUs you would purchase "))
        # Loop back if the user enter the negative integer
        if num_cpu > 0:
            print("Your total amount of CPUs are {}.".format(num_cpu))
            break
        else:
            print("Please input a POSITIVE integer")
    break
  if options == 3:
    print("You chose Motherboard")
    while True:
        num_motherboard = int(input("How many Motherboard you would purchase "))
        # Loop back if the user enter the negative integer
        if num_motherboard > 0:
            print("Your total amount of Motherboard are {}.".format(num_motherboard))
            break
        else:
            print("Please input a POSITIVE integer")
    break

  if options == 4:
    print("You chose GPU")
    while True:
        num_gpu = int(input("How many GPUs you would purchase "))
        # Loop back if the user enter the negative integer
        if num_gpu > 0:
            print("Your total amount of GPUS are {}.".format(num_gpu))
            break
        else:
            print("Please chose a number from the list above")
    break

# Let the user input the total amount of BTC
while True:
  total_num = int(input("Please enter the total amount (BTC) "))
  # Loop it back if it's negative integer
  if total_num < 0:
    print("The total cannot be negative integer. Please try again")
  else:
      break

# Computes the taxes
for i in range(4):
  if 250 * i < total_num <= 250 * i + 250:
    tax = 0.25 - (0.05 * i)
  if total_num > 1000:
    tax = 0.25

# Get the final price result
taxincluded_price = round(total_num * (tax + 1))
print("Your final price(tax included) will be {} {} BTC".format("."*20,taxincluded_price))

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


### Algorithm for encrypting the database
#### Flow diagram

![](https://github.com/kazuto-abe/CS2020/blob/master/Securing_database_flowdiagram.png?raw=true)

#### Main.py


```.py
# Algorithm for encrypting the database

# Read database from the .txt file
all_lines_of_db = open("cypher_database.txt", "r").readlines()


for line in all_lines_of_db:
    encrypt_line = ""
    decrypt_line = ""
    len_line = len(line)
    for l in range(len_line):
        # print("Line number: {} out of {} {} completion {:.2f}%".format(l + 1, len_line,"."*30 , (l + 1) / len_line * 100))
        new_l = chr(ord(line[l]) + 2)
        encrypt_line += new_l
        previous_l = chr(ord(encrypt_line[l]) - 2)
        decrypt_line += previous_l
    print("Your encrypted line is ... {}".format(encrypt_line))
    print("Your decrypted line is ... {}".format(decrypt_line))
        # print("Line number: {} out of {} {} completion {:.2f}%".format(l + 1, len_line,"."*30 , (l + 1) / len_line * 100))
    with open("cypher_database.txt", "a") as wfile:
        wfile.write(encrypt_line + "\n")
        wfile.write(decrypt_line + "\n")

```

## Computer Architecture 

![](https://github.com/kazuto-abe/CS2020/blob/master/Computer_figure2.jpg?raw=true)

Figure 2, created by Kazu, Luke, Ben, Salma, Zoe, and Guan



As an overview of this illustration, this shows the basic structure of the GAMING computer(at this time our team supposed) includes a common input source and output source. Before executing their program in the computer, signal input by users is required such as a keyboard, touch screen, mouse, microphone, etc...
(Commonly these input information will be transferred via USB port) There is also another type of signal input, called ethernet, which transmits network information toward to motherboard using a cable. All input slots are attached to the motherboard so that it directly connects to their program.

Aside from the input source, this gaming computer basically consists of 4 main components: Motherboard, HDD, SDD, and Power supply. 

Since this computer is for gaming stuff, there are two types of storage devices called HDD and SSD, where the data can be stored. In general, SSD, the newer type of flash memory,  is more competent than HDD except for their prices; it is faster, requires less power supply(it obviously contributes to long battery life), and shock-resistant. Most common laptops, however, have only one flash memory either HDD or SSD but our computer has “hybrid memory” because of a gaming computer. 
These mass storage devices are connected to the host bus by a computer bus interface called SATA cable. On the other hand, the power supply provides enough electronic power to the motherboard through a different cable, it’s called PSU cable. 

In the motherboard, there are mainly 4 components: CPU, GPU, RAM, and PCH.
(As this diagram indicates that the motherboard is DDR4 which is a newer model, It has no NorthBridge and SouthBridge.)

In order to make it more specific, details are written following bullet points below:


* CPU core i9 <br>
CPU is simply defined as the primary component of a computer that processes instructions; it executes the operating program and application, continuously receiving input source from the users. Also our CPU is named Intel core i9, which is the most powerful intel processor on the mainstream market. It is faster and smarter than previous models. The fan is attached to the CPU.

* RAM  <br>
This is a temporary storage in general, and it’s stored on the motherboard
in modules that are called DIMMs. RAM needs constant electrical power to
store data, and if the power supply is gone then the data is erased.
The motherboard is able to have between 2 and 4 of memory slots on average, so 
our computer has 4 RAM slots to store more data.

* GPU <br>
GPU, graphic processing unit, as a co-processor to accelerate CPUs for 
engineering computing.
In addition, GPU is good at parallel processing at once.

* PCH <br>
PCH stands for the platform controller hub, and it is known for one of the Intel chipsets.
These include the system clock, FDI, and DMI.



Eventually, results (output) will be shown to the users. (Screen, speakers, text, images, etc.. for instance)

## Criteria D: Functionality 
This is a video 

## Criteria E: Evaluation
