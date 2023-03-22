# Green-Coding-Competition-FY23

Welcome to the Green Coding Hackathon FY23.
The aim of this competition it's to utilize tools to analyse CO2 emissions and use methods and good practices to reduce our environmental impact into the technology world.

Our whole team wish you good luck!

## The Code

The application that are you going to run it's a solitaire game written in python.

The game runs via **solitaire.py** and uses the **card_elements.py** to produce actions on cards, piles, and deck.

Once started the application will automatically play a match and conclude it in few seconds.

The file **solitaireDONOTCHANGE.py** is an exact copy of the solitaire.py.

It will allow you to measure the original code emissions and the solitaire.py code emissions after you changes.

## Your role

Your role in this competition is to analyse **solitaire.py** and find flaws in the code causing it to produce a high level of CO2 emissions.

## Installation Guide

Before starting the competition, please follow this installation guide and **don't skip any step**.

If you have any problem during the installation, please raise your hand.

## VSCode

To modify your code you will need a python editor.

For this competition we recommend Visual Studio Code.

To install it follow the link https://code.visualstudio.com/download and click **Download**.

### Anaconda

To run the code, you will need to install **Anaconda**.

To install Anaconda follow the link https://www.anaconda.com/products/distribution and click **Download**.

Once the download is completed, install it using the default settings.

### Environment Creation

At this point you will create the environment where you are going to work.

Open your freshly installed **Anaconda Prompt**.

To do so, search for **Anaconda Prompt** in the search bar.

Your Anaconda Prompt window will look similar to this:

![Capture](https://user-images.githubusercontent.com/89920701/225885480-b0cbe1bf-0989-4822-b575-a71a06b95d35.PNG)

Once you are in your Anaconda Prompt run the following command:

``` conda create --name codecarbon python=3.10 ```

If a certificate error appears, please run the following command and than re-run the conda create command:

```conda config --set ssl_verify no```

During the creation of the environment you will be prompted with the following question:

![Capture2](https://user-images.githubusercontent.com/89920701/225888641-e691bf31-a7db-40eb-b628-c812bbbe2fd8.PNG)

Type **y** and press **Enter**.

The operation will take a couple of minutes to complete.

### Accessing your Environment

Now that the environment is created, we can access it running the following command:

```conda activate codecarbon```

Your command line should have **(codecarbon)** instead of **(base)** as below:
![Capture3](https://user-images.githubusercontent.com/89920701/225889381-b5c0d5bd-87b6-431f-8054-e9b72d33095c.PNG)

### Download the repository

In your command line run the following commands:

```pip install git```

```git clone https://github.com/GiuseppePerugia/Green-Coding-Competition-FY23.git```

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

*Note: If your code gets stuck due to Codecarbon, press Ctrl+C to stop the process and run it again*

## Visualize your emissions (Optional)

CodeCarbon produce a **csv** emissions file with detailed information regarding the emissions produced by the code.

To have a visualization of those information run the following command:

```carbonboard --filepath="emissions.csv" --port=8050```

If the default port 8050 is occupied, use another port (such as 3333).

The command will produce an host link to show the visualization of the emissions as shown below:
![Capture4](https://user-images.githubusercontent.com/89920701/225894254-ee2c13a0-271c-47d5-b1bb-a124378d8f5c.PNG)

Copy and paste the link into your preferred  browser.
At the bottom of the page you will see a bar chart that shows the emissions similar to the one shown below:
![224378880-fb3f0081-2b58-497a-b771-390f5c38a33d](https://user-images.githubusercontent.com/89920701/225897882-79d5daf7-b142-4795-9f14-12a1cde71b7a.png)

*Note: You will have a new bar in your chart for each time that you run the code*

## Code comparison

To be able to efficiently compare the code emissions be sure to:
1 Close the browser
2 Be sure to press Ctrl+C into the Anaconda Prompt Windows to stop the visualization of the emissions.
3 Delete the **emissions.csv** file to be able to create a new one.
4 Run the solitaireDONOTCHANGE.py one time.
5 Run the solitaire.py with your code improvement one time.
6 Run the *carbonboard --filepath="emissions.csv" --port=8050*
7 Copy and paste the link into your browser.
8 Navigate at the bottom of the page to see the bar chart with two code compared.

*Alternative: Instead of step 6, 7 and 8 open the emissions.csv file and change the "emissions" column to decimal format with 12 decimal places.*

## Accessing your code

You can access your code by double clicking into the **solitaire.py** and use *Visual Studio Code* as chosen program.

Alternatively, you can first open *Visual Studio Code*, click *Open*, and select the **solitaire.py** code.

# Green Coding Guide

Here you will find a list of good practice and guide to apply to your code.

The code contains one or more bad coding technique for each of the category listed in the guide below.

## 1. Eliminate unnecessary operations

Reduce the number of if-else blocks. The evaluation of each additional if-else condition increases the computational workload. 
The number of if-else blocks can be reduced by applying alternate logic.

Reduce the number of function calls wherever possible. The following example
uses the print function. Calling print statements multiple times takes longer
compared to calling a single print statement with line breaks or dynamic
variables. Also, print and debugging information are sometimes left in code
unnecessarily and do not add value in production.

## 2. Avoid unnecessary variables
It is not always essential to store a value in a variable if it is not going to be used elsewhere. 
Both the additional assignment operation and storing the variable in memory add to the computational load. 
Reducing unnecessary variables also allows the code to be more succinct and readable.

## 3. Use appropriate algorithms
There may be several algorithms or strategies for solving a specific problem (e.g. search, sorting). 
It is best to ensure that the algorithm you choose matches the use case appropriately but is also efficient enough as to not waste resources. 
The example below compares two popular sorting algorithms: bubble sort and quick sort. 
Bubble sort uses nested for loops whereas quick sort uses partitioning and recursion. 
The nested for loop in bubble sort makes it very inefficient. 
One important takeaway is to avoid nested loops altogether wherever possible ( for , while etc.).

## 4. Use language specific features
Some languages have built-in strategies for improving code efficiency which are useful to use.
List comprehensions in Python for example are faster in most use cases.

## 5. Avoid using global variables
Functions should be defined as pure components as far as possible, i.e. they should be independent and modular blocks of code. 
Global variables can occupy excessive memory unnecessarily and they can also cause undesirable effects and bugs in code.

## 6. Consider Libraries Integrations
Libraries are very beneficial as they help to implement functionalities faster compared to writing code from scratch. 
On the other hand, importing additional libraries into an application can increase its size and execution time. 
There are several websites to compare the sizes of different libraries for different programming languages.
The following are some comparison websites.
Python: https://pypi.org/
JavaScript: https://packaging.python.org/en/latest/tutorials/packaging-projects/

*Suggestion: Try to find information regarding* **itertools** *and how to use it in your code*

# Code Analysis
In the following you can find bad and good practices of the codes provided.

## Eliminate unnecessary operations
In code1 a series of useless else are scattered through the code causing dealys and multiple print statements. In code2 does not happens reducing the computational workload.

## Avoiding unnecessary functions calls
In code1 we call same functions multiple times which requires power and energy to access them. We can simply call a function once, store it in a variable and use that variable when you need the function. We save energy and the code looks more tidy. Also in code1 we have a series of debuginning printing statement which do not add any value in production.

## Avoid unnecessary variables
Unnecessary variables have been placed at the beginning of code1. These variables stores cards values, colours, and symbols. In code2 this does not happens and the cards values, colours, and symbols are simply added to a list. Although this does not have an huge impact due to the low numbers of elements in the deck, the power consumption would grow in case of a bigger deck of cards.

## Use appropriate algorithms
In code1 we’re using a bogo sort to list our cards left in the deck. In code2 we’re implementing a merge sort. It’s well known that a merge sort and quick sort are the most efficient sort methods to save energy and resources.

## Use language specific features
Using proper comprehensive lists to avoid useless methods to list the cards. In code1 we’re using 1 for loop with 2 nested for loops to list the cards while in code2 we use a comprehensive list, which is makes spare an enormous amounts of energy.

##Avoiding using global variables
In code1 we have a global variable declared which is used in different methods. This can occupy excessive memory unnecessarely. In code2 this does not happens. This because the functions should be defined aspure components as far as possible.

## Libraries
Labriaries are very beneficial as they help to implement functionalities faster compared to write code from scratch. In code2 we use itertool library to achieve a better comprehensive listing of our cards.
