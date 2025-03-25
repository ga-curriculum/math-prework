[TODO] in general need the popups for incorrect responses as well.

## Raandom Variables

### Knowledge Check

Which of the following is an example of a continuous value?

Select the best answer.

- Incorrect: The number of home runs hit by Babe Ruth.

- Correct : The volume of water in all the earth's oceans. (Because volumne is a measurement, this is indeed a continuous value.  We can always increase the decimal place to which the volume is measured to improve its accuracy.)

- Incorrect: The number of employees in a company.

- Incorrect : The number of grains of sand on earth.

### Knowledge Check

Which of the following random variables are correctly labeled as “CONTINUOUS” or “DISCRETE”?

Select all that apply.

[TODO]

Correct: That’s right! All of these are labeled correctly except for, “The length of a shadow cast by a willow tree.” This is a continuous variable, as we can always increase the decimal place to which the length is measured to improve its accuracy.

### Knowledge Check

Which of the following is an example of a discrete variable?

Select the best answer.

[TODO]

### Knowledge Check

What is the expected value of $x$?

[TODO]- image

Select the best answer.

- Incorrect: 0.35
- Incorrect: 0.75
- Incorrect: 1.5
- Correct: 1.1  The expected value of $x$ is 0+1(0.35)+2(0.15)+3(0.15) = 1.1

### Knowledge Check

Continuous data comes from quantities that can be ____________.

Select the best answer.

- Correct: Measured.  Continuous variables can be measured, while discreet variables can be counted
- Incorrect: Counted
- Incorrect: Both

### Knowledge Check

Which of the following is *not* an example of continuous data?

Select the best answer.

[TODO]

### Knowledge Check

You decide to collect several bottles of water and measure the volume of water each contains. Let $x$ be the number of milliliters of water in each bottle. What type of variable is $x$?

Select the best answer.

[TODO]

## Measures of Center and Spread

### Knowledge Check

What is the mean of the following values:

[13, 18, 13, 14, 13, 16, 14, 21, 13]

Select the best answer.

- Incorrect: 18
- Incorrect: 14
- Correct: 15
- Incorrect: 13

Correct:
(13+ 18+ 13+ 14+ 13+ 16+ 14+ 21+ 13)/ 9 = 15

### Knowledge Check

What’s the median in this set?

        [13, 13, 13, 13, 14, 14, 16, 18, 21]
Select the best answer.

- 14 (Correct)
- 13
- 18
- 21

Correct: If we line up these values from smallest to largest, we find the middle-most value is 14.

### Knowledge Check

What’s the mode in this set?

       [13, 18, 13, 14, 13, 16, 14, 21, 13]                       
Select the best answer.

- 14
- 16
- 13
- 21 (correct)

Correct: The value we see most often is the 13.

### Knowledge Check

What are the data types of `+42`, `1`, `False`, and `float(False)`, respectively?

- int, bool, bool, float
- int, int, bool, bool
- int, float, bool, bool
- int, int, bool, float (correct)

The built in float() function converts the value passed in into a float. Note that 1 by itself is an int, even though True is internally represented as 1.

### Knowledge Check

What is the variance of the values [4, 10, 16]?

Select the best answer.

[TODO]

### Knowledge Check

Suppose that we had **3** purchases at 9:00 this morning, **4** purchases at 10:00, and **5** purchases at 11:00.

This makes a data set of [3, 4, 5]. We want to calculate the standard deviation for this data.

If we want to find the distance from each data point to the mean, we first have to calculate the mean. Which of these options represents the mean?

Select the best answer.

- Correct: 4
- Incorrect: 2
- Incorrect: 7

### Knowledge Check

Given the following data set:

[11, 12, 13, 13, 14, 14, 14, 15, 15, 16, 17]

Mean = 14

Standard deviation = 1.65

Which points (if any) warrant further investigation as potential outliers?

Select the best answer.

[TODO]

## Manipulating Variables in Python

### Knowledge Check

In this exercise, you'll create three different kinds of variables and set their specific values.

Create a variable called volume and set it to 3.2.
Create a variable called greeting and set it to "hello".
Create a variable called is_learning and set it to True.

Enter your response using Python 3.6.

[Open Code Response]

### Knowledge Check

Suppose birds = ['parrot', 'crow', 'owl']. What is birds[2]?

Select the best answer.

- 'parrot'
- 'crow'
- 'owl' (correct)
- IndexError: list index out of range

Hint: Remember : Indexing starts at 0, so 'parrot' is 0, 'crow' is 1 and 'owl' is 2

### Knowledge Check

You're writing a program that provides restaurant suggestions to users based on survey results. Users are asked to indicate their preference on a variety of flavors and textures by selecting the options "Love it!," "Meh, it's OK," and "No way!"

Which complex data type should you use to store the answer options?

Select the best answer.

- List
- Tuple
- Set

Hint: Because the three rankings users can select from are fixed options -- meaning we don't plan to add or delete more -- we'd use a tuple.

### Knowledge Check

Suppose you're implementing a spell checker. You want to test whether or not a word is contained inside a collection of known words.

Which data structure should you use to store the words? Why?

Select the best answer.

- A list, because the words are all the same data type and have an alphabetical order.
- A list, because the index of each word is important.
- A set, because the word order is not important for a spell checker, and checking to see if an element is in a set is more efficient than doing the same for a list.
- A string, because each word is a string and storing the words in a simpler data type is fast.

Answer: In this case, a set is preferable to a list because membership lookup is faster for sets. Each word will be unique in the set, and a word's position in the set doesn't matter for a spell check (only that it's contained in the set).

### Knowledge Check

1. Change the starter code to create an empty list called packing_list.
1. Insert the string shirt into packing_list. Then, save packing_list to a new variable called packing_list_2.
1. Insert the string pants into packing_list_2. Also, save the result as a new variable called packing_list_3.
1. Insert the string socks into packing_list.
1. Print each list on a new line. If you’ve done this exercise correctly, their values should all be identical.

Hint: Write out your code using repl.it before pasting it into the box below so that you can practice reading the errors that Python typically gives you.

Enter your response using Python 3.6.

[Open Code Response]

answer:

```python
packing_list = []
packing_list.append('shirt')

packing_list_2 = packing_list
packing_list_2.append('pants')

packing_list_3 = packing_list_2

packing_list.append('socks')

print(packing_list)
print(packing_list_2)
print(packing_list_3)
```

### Knowledge Check

Suppose we have a set containing categories of houses. How might we determine the number of unique categories?

For example:

```python
house_categories = {'Single-Family Home', 'Condo', 'Duplex'}
```

Select the best answer.

- house_categories.count()
- len(list(house_categories))
- set(house_categories)
- len(house_categories) (correct)

Hint: Sets only contain unique values, so finding the number of unique items in a set is as easy as computing the length of the set.

### Knowledge Check

What would be the result of evaluating the following code?

```python
len({3, 2, 9, 5, 3, 6, 2}) + len([3, 2, 9, 5, 3, 6, 2])
```

Select the best answer.

- 7
- 10
- 12
- 14

Hint: A set does not contain duplicate values. Therefore, the set contains a total of five unique values, while the list contains a total of seven values. Summed together, this equals 12.

## Control Flow in Python

### Knowledge Check

Which of the following would be a good use of the while loop when we don't know the number of iterations in advance?

Select all that apply.

- Loop while less than 33 milliseconds have elapsed, then continue.
- Loop while we have not received the entire downloaded file.
- Loop until a new random number between 0 and 1 is greater than 0.9
- Loop through each element of a Python list.

Correct: Python lists have a finite size, which we know in advance. (We'll cover looping through them using the for loop in the next section). In video games, a while loop is often used to wait until 33 milliseconds have elapse. This guarantees an exact 30 frames per second. We don’t know the number of iterations in advance here because execution speed can vary between computers — even on a single processor.

### Knowledge Check

What is stored in x after evaluating the following code?

```python
x = 1

while x < 10:
    x = x * 2
```

Select the best answer.

- The largest power of 2 less than 10
- 16 (correct)
- 10
- The first even number greater than 10

Hint: In each iteration x is doubled and we only exit the while loop if x is at least 10. Therefore, when we exit the loop x will equal 16.

## Functions in Python

### Knowledge Check

Observe the Python function below.

If we call this function with `calculator("*", 10, 5)`, what will be the output?

```python
def calculator(operation, value1, value2):
    if operation == "+": return value1 + value2
    if operation == "-": return value1 - value2
    if operation == "*": return value1 * value2
    if operation == "/": return value1 / value2
```

Select the best answer.

- 15
- 5
- 2
- 50 (correct)

### Knowledge Check

Check out the `compound()` function below.

```python
def compound(word1, word2):
    return word1 + word2
```

What would we need to write in order to get a return value of `'bookshelf'`?

Hint: Our arguments are strings.

Select the best answer.

- `compound('book', 'shelf')` (correct)
- `compound(book + " " + shelf)`
- `compound(book, shelf)`
- `compound('book' + " " + 'shelf')`

### Knowledge Check

You begin writing a function that’s designed to multiply two numbers together:

```python
def multiply(a, b):
    output = a * b
```

You want to assign the output number to a variable, like so: `var = multiply(3, 4)`. What line needs to be added to the function to make `var` the output number?

Select the best answer.

- return output (correct)
- return: output
- print(output)
- return

## Objects in Classes

### Knowledge Check

Recall that a class is essentially the blueprint of a provided object, which is created using the process of instantiation.

Imagine that you are working with music data and you want to define a class to represent a band. The class should have two attributes that describe the object being assigned to that class — the name of the band (`band`) and the band’s genre (`genre`).

Task: For this challenge, write the code needed to define a class for a band, initiate it for the band Queen, and fill in the `give_stats()` method to have it return a string in the following format: `band: Queen genre: Rock`

Hint: You call the string method `.format()` within the `give_stats()` method to help you return the full set of information.

Enter your response using Python 3.6.

[Open Code Response]

### Knowledge Check

You would like to define a class called Bird() that inherits from a class called Animal(). What is the correct syntax for the first line of the class definition?

Select the best answer.

- `def Bird(Animal)`
- `class Bird from Animal`
- `class Bird(Animal)` (correct)
- `Class Animal(Bird)`

Hint: Class is lowercase and the parent class is put in the parentheses following the name of the defined class.

### Knowledge Check

Consider the following class definition for `Cat()`:

```python
class Cat(Animal):
    def __init__(self, name='Lucky'):
        self.name = name
```

How would you instantiate a `Cat()` object with a `name` attribute of `'Furball'`?

Select the best answer.

- `mycat = Cat(name='Furball')` (correct)
- `furball = Cat()`
- `mycat = Cat(self, name='Furball')`
- `mycat = Cat.init(name='Furball')`

Hint: The `__init__()` function is automatically called when we create an object with the `Cat(name='Furball')` syntax

### Knowledge Check

Which of the following statements are true of the `self` argument in class definitions?

Select all that apply.

- Correct : The user does not need to supply `self` when using instance methods, only when defining them.
- Correct : The `self` argument is a reference to the instance object.
- Incorrect: Any variable assigned with `self` (e.g. `self.var`) will be shared across instances of the class.
- Incorrect: With an instance, `obj`, entering `obj.self.var` will provide the value of `var` for that instance

Hint: `self` is automatically passed into an instance method when you call it. It refers to the instance, and not the class. `self.var` will not be shared between instances, as `self` refers only to the specific instance.


## Error Handling in Python

### Knowledge Check

Consider the following code:

```python
for i in 1 to 10:
    print(i)
```

Which of the following error types will occur?

Select the best answer.

- TypeError
- SyntaxError (correct)
- NameError
- ValueError

### Knowledge Check

You are writing a function that adds numbers together. The output should only be a positive number or zero. If it isn’t, you would like to throw a `ValueError`:

```python
def positive_only(a, b):
    output = a + b
    if output >= 0:
        return output
    else:
        # Your code here.
```

What code should be placed in the `else` statement to give a `ValueError`?

Select the best answer.

- throw ValueError
- raise ValueError (correct)
- return ValueError
- except ValueError

Hint: To throw an error to a user use the `raise` keyword followed by the error type.