# Green-Coding-Competition-FY23

Welcome to the Green Coding Hackathon FY23.
The aim of this competition it's to utilize tools to analyse CO2 emissions and use methods and good practices to reduce our environmental impact into the technology world.

Our whole team wish you good luck!

## The Code

The application that are you going to run it's a solitaire game written in python.

The game runs via **solitaire.py** and uses the **card_elements.py** to produce actions on cards, piles, and deck.

Once started the application will automatically play a match and conclude it in few seconds.

The file **solitaireDONOTCHANGE.py** it's an exact copy of the solitaire.py.

It will allow you to measure the original code emissions and the solitaire.py code emissions after you changes.

## Your role

Your role in this competition is to analyse **solitaire.py** and find flaws in the code causing it to produce a high level of CO2 emissions.

## Installation Guide

Before starting the competition, please follow this installation guide and **don't skip any step**.

If you have any problem during the installation, please raise your hand.

## VSCode

To modify your code you will need a python editor.

For this competition we recommend Visual Studio Code.

To install it follow the link https://code.visualstudio.com/download and click ** Download **.

### Anaconda

To run the code, you will need to install **Anaconda**.

to install Anaconda follow the link https://www.anaconda.com/products/distribution and click **Download**.

Once the download  it's completed install it using the default settings.

### Environment Creation

At this point you will create the environment where you are going to work.

Open your freshly installed **Anaconda Prompt**.

To do so, search for **Anaconda Prompt** in the search bar.

Your Anaconda Prompt window will look similar to this:

![Capture](https://user-images.githubusercontent.com/89920701/225885480-b0cbe1bf-0989-4822-b575-a71a06b95d35.PNG)

Once you are in your Anaconda Prompt run the following command:

``` conda create --name codecarbon python=3.10 ```

During the creation of the environment you will be prompted with the following question:

![Capture2](https://user-images.githubusercontent.com/89920701/225888641-e691bf31-a7db-40eb-b628-c812bbbe2fd8.PNG)

Type **y** and press **Enter**.

The operation will take a couple of minutes to complete.

### Accessing your Environment

Now that the environment it's create we can access it running the following command:

```conda activate codecarbone```

Your command line should have **(codecarbon)** instead of **(base)** as below:
![Capture3](https://user-images.githubusercontent.com/89920701/225889381-b5c0d5bd-87b6-431f-8054-e9b72d33095c.PNG)

### Download the repository

In your command line run the following command:

```git clone https://github.com/GiuseppePerugia/Green-Coding-Competition-FY23.git```

If you receive and error  message run:

```pip install git```

### Requirement Installation

Before opening or interact with the repository you will need to install a couple of requirements.

Follow the commands below and run them in sequence to successfully install the requirements:
1. ```cd Green-Coding-Competition-FY23```

2. ```pip install -r requirements.txt```

After a couple of minutes all the requirements will be installed.

## Run the code

We're ready to run the code!

Everytime you want to run the code use the following command:

```python solitaire.py```

*Note: If you're code gets stuck due to Codecarbon, press Ctrl+C to stop the process and run it again*

## Visualize your emissions

CodeCarbon produce a ** csv ** emissions file with all detailed information regarding the emissions of the code.

To have a visualization of those information run the following command:

```carbonboard --filepath="emissions.csv" --port=8050```

If the default port 8050 it's occupied, use another port (such as 3333).

The command will produce an host link to show the visualization of the emissions as shown below:
![Capture4](https://user-images.githubusercontent.com/89920701/225894254-ee2c13a0-271c-47d5-b1bb-a124378d8f5c.PNG)

Copy and paste the link into your preferred  browser.
At the bottom of the page you will se a bar chart that show the emissions similar to the one shown below:
![224378880-fb3f0081-2b58-497a-b771-390f5c38a33d](https://user-images.githubusercontent.com/89920701/225897882-79d5daf7-b142-4795-9f14-12a1cde71b7a.png)

*Note: You will have a new bar in your chart for each time that you run the code*

## Code comparison

To be able to efficiently compare the code emissions efficiently be sure to:
- Close the browser
- Be sure to press Ctrl+C into the Anaconda Prompt Windows to stop the visualization of the emissions.
- Delete the ** emissions.csv ** file to be able to create a new one.
- Run the solitaireDONOTCHANGE.py one time
- Run the solitaire.py with your code improvement one time.
- Run the * carbonboard --filepath="emissions.csv" --port=8050 *
- Copy and paste the link into your browser.
- Navigate at the bottom of the page to see the bar chart with two code compared.

*Alternative: If you don't want to see a graphical interface for your emissions, open the emissions.csv file and change the "emissions" column to decimal format with 12 decimal places.*

## Accessing your code

You can access your code by double clicking into the ** solitaire.py ** and use * Visual Studio Code * as chosen program.

Alternatively, you can first open * Visual Studio Code *, click * Open *, and select the ** solitaire.py ** code.

# Green Coding Guide

Here you will find a list of good practice and guide to apply to your code.

The code contains one or more bad coding technique for each of the category listed in the guide below.

## 1. Eliminate unnecessary operations

Reduce the number of if-else blocks. The evaluation of each additional if-else condition increases the computational workload. 
The number of if-else blocks can be reduced by applying alternate logic.

### This is computationally expensive
```
def pet_noise(pet)
  if pet == 'cat':
    return 'meow'
  elif pet == 'dog':
    return 'woof'
  else:
    return 'unknown'
```

### This is better
```
def pet_noise(pet):
  if pet == 'cat':
    return 'meow'
  if pet == 'dog':
    return 'woof'
  return 'unknown'
```
Reduce the number of function calls wherever possible. The following example
uses the print function. Calling print statements multiple times takes longer
compared to calling a single print statement with line breaks or dynamic
variables. Also, print and debugging information are sometimes left in code
unnecessarily and do not add value in production.

### This is computationally expensive
```
numberOfApples = 2
numberOfOranges = 3
numberOfPears = 4
print("Number of apples: ", numberOfApples)
print("Number of oranges: ", numberOfOranges)
print("Number of pears: ", numberOfPears)
```

### This is better
```
numberOfApples = 2
numberOfOranges = 3
numberOfPears = 4
print("Number of apples: {}\nNumber of oranges: {}\nNumber of pears:
{}".format(numberOfApples, numberOfOranges, numberOfPears))
```

## 2. Avoid unnecessary variables
It is not always essential to store a value in a variable if it is not going to be used elsewhere. 
Both the additional assignment operation and storing the variable in memory add to the computational load. 
Reducing unnecessary variables also allows the code to be more succinct and readable.

### This is computationally expensive
```
def function(a,b):
  result = max(a,b)
  return result
```

### This is better
```
def function(a,b):
  return max(a,b)
```
## 3. Use appropriate algorithms
There may be several algorithms or strategies for solving a specific problem (e.g. search, sorting). 
It is best to ensure that the algorithm you choose matches the use case appropriately but is also efficient enough as to not waste resources. 
The example below compares two popular sorting algorithms: bubble sort and quick sort. 
Bubble sort uses nested for loops whereas quick sort uses partitioning and recursion. 
The nested for loop in bubble sort makes it very inefficient. 
One important takeaway is to avoid nested loops altogether wherever possible ( for , while etc.).

### This is computationally expensive
```
def bubble_sort(array):
  n = len(array)
# nested for loop creates lots of overhead
  for i in range(n-1):
    for j in range(n-i-1):
      if(array[j] > array[j+1]):
        array[j], array[j+1] = array[j+1], array[j]
   return array
```

### This is better
```
def quick_sort(array):
  less = []
  equal = []
  greater = []
# divide and conquer approach to sorting
  if len(array) > 1:
    pivot = array[0]
    for x in array:
      if x < pivot:
        less.append(x)
      elif x == pivot:
        equal.append(x)
      elif x > pivot:
        greater.append(x)
    return quick_sort(less)+equal+quick_sort(greater)
  else:
    return array
```

## 4. Use language specific features
Some languages have built-in strategies for improving code efficiency which are useful to use.
List comprehensions in Python for example are faster in most use cases.

### This is computationally expensive
```
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newList = []
for x in fruits:
  if "a" in x:
    newList.append(x)
    
print(newList)
```

### This is better
```
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]

newList = [x for x in fruits if "a" in x]

print(newList)
```

## 5. Avoid using global variables
Functions should be defined as pure components as far as possible, i.e. they should be independent and modular blocks of code. 
Global variables can occupy excessive memory unnecessarily and they can also cause undesirable effects and bugs in code.

### This is computationally expensive
```
FIRST_INTEGER = 5
SECOND_INTEGER = 10

def function():
    return FIRST_INTEGER + SECOND_INTEGER
```

### This is better
```
def function(firstInteger, secondInteger):
  return firstInteger + secondInteger
```

## 6. Libraries
Libraries are very beneficial as they help to implement functionalities faster compared to writing code from scratch. 
On the other hand, importing additional libraries into an application can increase its size and execution time. 
There are several websites to compare the sizes of different libraries for different programming languages.
The following are some comparison websites.
Python: https://pypi.org/
JavaScript: https://packaging.python.org/en/latest/tutorials/packaging-projects/

*Suggestion: Try to find information regarding* **itertools** *and how to use it in your code*
