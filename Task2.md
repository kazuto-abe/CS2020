## Worksheet
Question 1: <br>
Describe the four core computational thinking skills?

1. Decomposition<br>
This idea is to break complex problems down into more manageable parts

2. Pattern recognition<br>
This idea refers to figure out the similarity between different types of problems. (focus on what the common issues are)

3. Abstraction<br>
This idea implies to focus on important information only, then ignoring irreverent problems.

4. Algorithmic thinking<br>
In this context, basically algorithm means a set of rules and developing a step by step solutions in order to achieve the goals.

Question 2: <br>
What is the most powerful computer? Glad you asked. Watch this video about Sierra Computer. Describe the below points that surprised you the most.

The supercomputer called “Summit” made in the USA was the previous model of the most powerful computer in the world, “Fugaku” made in Japan, however, is currently the latest version of the supercomputer now.

In terms of the video called “Sierra Computer”, things that surprised me are: <br>
- It can manage anything we want such as cancer simulations, modeling earthquakes, exploring the cause of brain injuries, etc…
- There is a link between a supercomputer called “Sierra” and US nuclear bomb, 
and the supercomputer is able to simulate questions the military might have about its arsenal. <br>
→Sierra will predict the consequence of whether anything would break in a real detonation.

Question 3: <br>
Supercomputers are currently used to investigate solutions to real-life problems from cancer research, Ai, economics, or brain stimulation. Military uses are also one major force behind the development of these machines. Analyze the benefits and possible drawbacks of developing supercomputers in our modern world? Should we do it?

In order to clarify both positive aspects and negative aspects, here are the pros and cons below.
At this time, I basically focused on micro area of pros and cons. <br>

Pros: <br>
- They can help analyzing and predicting catastrophic disaster such as earthquake, climate change, and brain simulation. 
- The supercomputer can complete tasks in seconds that normal computer takes hour or day to finish up.
- Supercomputer can decrypt any encrypted passwords or phrases used in electric devices.

Cons: <br>
- A lot of electricity required <br>
The constant power supply is needed, they approximately consume energy 
equal to 5000 houses.
- Maintenance <br>
This includes financial problems, land, and staff. Since supercomputer consists of a dozen of components such as processor,

Based on both side of aspects, Supercomputer might bring some positive consequences more than negative consequences in the future.

Question 4: <br> 
Identify the most advanced computer in Japan (What, specs, location, uses). We might go and visit it :-) 

As I claim in question 2, the most advanced computer in Japan is “Fugaku” at the moment. 

Specs: 158976 nodes, 48 cores(CPU A64FX), Java, Python, Numpy, and Scipy are used as a programming language and its library. (provided by Fujitsu)
OSs are, Red Hat Enterprise Linux8 and McKernel. (provided by RIKEN)

Location: Hyogo prefecture

Uses: most well-known supercomputers can be used to simulate nuclear explosions, and model climate systems in general, Fugaku in japan, furthermore, can be used to analyze the impact of a tsunami triggered by a huge earthquake, and map out an evacuation route.




## Programming task
In a school there are 2400 students and each student uses one locker. Each locker has a unique number from 1 to 2400. The lockers are to be painted in four colours: red, white, yellow and blue, in order of locker numbers, as shown in the following table.link

The pattern of colours continues in this manner. For example, locker number 15 will be painted yellow.


Task1: <br>
Create a program that shows the colors of all the lockers from 1 to 2400


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

Task2:<br>
Using the program above, create another program that allows the user to enter a number and the program outputs the color that should be used in the locker.


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
