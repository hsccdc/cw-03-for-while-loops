# cw-03-for-while-loops
Due end of class March 14th

# Lists

Variables hold an item.

```python
my_color = 'red'
my_peer = 'Brandi'
```

**Lists** hold *multiple items* - and lists can hold anything.

```python
# Declaring lists
colors = ['red', 'yellow', 'green']
students = ['Brandi', 'Zoe', 'Steve', 'Aleksander', 'Dasha']

# Strings
colors = ['red', 'yellow', 'green']

# Numbers
my_nums = [4, 7, 9, 1, 4]

# Both!
my_nums = ['red', 7, 'yellow', 1, 4]

# All sorts of stuff!
my_values = ['red', 7, True, 3.14159, None]
```

Remember that a variable can hold any information. So it can also hold a list.

In the same way that you recognize strings by the quotation marks around them, you can recognize a list by the square brackets that surround it.

---

# Aside: Counting from Zero

Computers and Programming Languages universally start counting from zero!

Strange, right? Actually, it's only strange if you're from the US/Canada!

In many countries, it's a fairly normal concept. This is an elevator from Ireland, for example:

<img src="assets/elevator_buttons_in_ireland.jpg" width="300">

Whereas in the US/Canada, the "2nd floor" is the floor above ground level!

---

# Accessing List Elements

## Index

The **index** means the location of an *element* in the list.

**Important**: Just like European elevators, indices start counting at 0!

| List | 'Brandi' | 'Zoe' | 'Steve' | 'Aleksander' | 'Dasha' |
| :---: | :---: | :---: | :---: | :---: | :---: |
| Index |     0    |   1   |    2    |    3   |    4   |

```python
students = ['Brandi', 'Zoe', 'Steve', 'Aleksander', 'Dasha']
print(students[0]) # Prints 'Brandi'
print(students[1]) # Prints 'Zoe'
print(students[4]) # Prints 'Dasha'
```

## Exercise 1:

1. Create a **list** with the names `'Holly'`, `'Juan'`, and `'Ming'`
1. Print the third name
1. Create a **list** with the following items: `2`,`'four'`, `6`, and `'eight'`
1. Print the first item

## Negative Index

You can use a negative index to access elements from the *back* of the list, where `-1` is the very end of the list!

```python
print(students[-1]) # Prints 'Dasha'
print(students[-3]) # Prints 'Steve'
print(students[0])  # Prints 'Brandi' -- 0 is the *start* of the list!
```

---

# Lists Inside of Lists!?

Yup, you can even put lists inside lists:

```python
some_list = [
    3.14,
    [1, 2, 3],
    'joe',
    ['four', 5, 'six']
]
```

---

# Built-in List Operations

Now that we know what lists are, what can we do with them?

## Length of a List with `len()`

`len()`: Tells us how long a list is

```python
students = ['Brandi', 'Zoe', 'Steve', 'Aleksander', 'Dasha']
num_students = len(students)
print('There are', num_students, 'students in the course')
#--> 5
```

* You put the list between the parentheses after the word `len`
* `len()` is a *built-in function*
* `len()` can be performed on any list, no matter what's in it
* `len()` can also be used on strings!
   * Example: `len('hello')` returns 5

## Adding an Element with `.append()`

Did you forget to add something to a list? No problem; you can use `.append()`.

`.append()`: Adds an element (that you provide) to the end of the list

```python
students = ['Brandi', 'Zoe', 'Steve', 'Aleksander', 'Dasha']
students.append('Sonyl')
print(students)
#--> ['Brandi', 'Zoe', 'Steve', 'Aleksander', 'Dasha', 'Sonyl']
```

Suppose a new student joins our course. We can add them to the end of the list with `append`, which is a function built directly into a list.

Notice it is called with a dot after the list, unlike the other function we've used, `len`. The reason for that will be revealed in a few days!

## Adding an Element with `.insert()`

What happens if we want to add something somewhere else? We can use `.insert()`, which specifies where (i.e., to which index) we want to add the element.

`.insert()`: Adds to any point in the list. You have to provide the element, and an index

```python
students = ['Brandi', 'Zoe', 'Steve', 'Aleksander', 'Dasha', 'Sonyl']
students.insert(1, 'Sanju')
print(students)
#--> ['Brandi', 'Sanju', 'Zoe', 'Steve', 'Aleksander', 'Dasha', 'Sonyl']
```

## Removing elements with `.pop()`

What if someone leaves our course? We need to remove them from the list. We can do this with `pop`.

Pop drops the last thing off the list. It gives us back the value that it removed. This is called a **return value**. We can take that value and assign it to a new variable, `student_that_left`. 

`.pop()`: Removes an item from the end of the list

```python
students = ['Brandi', 'Sanju', 'Zoe', 'Steve', 'Aleksander', 'Dasha', 'Sonyl']
student_that_left = students.pop()
print('The student', student_that_left, 'has left the course.')
#--> 'The student Sonyl has left the course.'
print(students)
#--> ['Brandi', 'Sanju', 'Zoe', 'Steve', 'Aleksander', 'Dasha']
```

## Removing elements with `.pop(index)`

What if someone specific leaves the course?

We can do this with `pop` again. Here, we can give pop the index we want removed. It gives us back the value that it removed. We can take that value and assign it to a new variable, `student that left`.

`.pop(index)`: Removes an item from the list, from the provided index

```python
students = ['Brandi', 'Sanju', 'Zoe', 'Steve', 'Aleksander', 'Dasha']
student_that_left = students.pop(2) # Remember to count from 0!
print('The student', student_that_left, 'has left the course.')
#--> 'The student Zoe has left the course.'
print(students)
#--> ['Brandi', 'Sanju', 'Steve', 'Aleksander', 'Dasha']
```

## Exercise 2: Pop, Insert, and Append

Partner up! Choose one person to be the driver and one to be the navigator, and do the following:

1. Declare a list with the names of your classmates
1. Print out the length of that list
1. Print the 3rd name on the list
1. Delete the first name on the list
1. Re-add the name you deleted to the end of the list

<details>
<summary>Answer (SPOILER!)</summary>
<pre>
students = ['Brandi', 'Sanju', 'Zoe', 'Steve', 'Aleksander', 'Dasha']
print(len(students))
print(students[2])
deleted_classmate = students.pop(0)
students.append(deleted_classmate)
print(students)
</pre>
</details>

---

# Numerical List Operations

If you have a list containing only numbers, you can perform some special numerical operations on it.

## Sum

`sum()`: Adds the entire list together.

```python
team_members_count = [7, 2, 4, 3]
total_company_size = sum(team_members_count)
print('The size of our company is', total_company_size)
#--> 16
```

## Max/Min

We might want to simply know what is the largest or smallest item in a list. In this case, we can use the built-in functions `max()` and `min()`.

`max()` or `min()`: Finds highest (or lowest) number in the list.

```python
team_batting_avgs = [.328, .299, .208, .301, .275, .226, .253, .232, .287]
print('The highest batting average is', max(team_batting_avgs))
#--> 0.328
print('The lowest batting average is', min(team_batting_avgs))
#--> 0.208
```

## Exercise 3: Everything Regarding Lists

Create a `list_practice.py` file.

In it:

1. Save a list with the numbers `2`, `4`, `6`, and `8` into a variable called `numbers`
1. Print the max of `numbers`
1. Pop the last element in `numbers` off; re-insert it at index `2`
1. Pop the second number in `numbers` off (**Note:** I mean human-ese "second", **not** index `2`)
1. Append `3` to `numbers`
1. Print out the average number (divide the sum of `numbers` by the length)
1. Print `numbers`

The expected output is:

<pre>
Max: 8
Average: 4.75
Final list: [2 8 6 3]
</pre>

<details>
<summary>Answer (SPOILER ALERT)</summary>
<pre>
numbers = [2,4,6,8]
print(max(numbers))
el = numbers.pop()
numbers.insert(2, el)
numbers.pop(1) # human-ese "second" == computer-ese "first"
numbers.append(3)
print(sum(numbers)/len(numbers))
print(numbers)
</pre>
</details>

---

# More Exercises

## Partner Exercise: Building a Copy (5 mins)

Get with a partner. Decide who will drive and who will navigate.

* In a new file (name it on your own), write a function, `copy_list`, that takes in a list, `original_list`, as a parameter
* Your function should create a new list, `my_new_list` with the contents of the original list
* Your function should return `my_new_list`

An example of how this function can be used:

```python
my_list = [1, 2, 3]
my_new_list = copy_list(my_list)
print(my_new_list)
#--> [1, 2, 3]
```

Make sure you run your code to check that it works!

Some hints are provided below; try to open just one of them at a time!

<details>
<summary><strong>Hint 1</strong></summary>
You'll need a `for` loop
</details>
<details>
<summary><strong>Hint 2</strong></summary>
You'll need to declare <code>my_new_list</code> above (outside of) your <code>for</code> loop
</details>

<details>
<summary>Answer (SPOILER!)</summary>
def copy_list(original_list):
    my_new_list = []
    for item in original_list:
        my_new_list.append(item)
    return my_new_list
</details>

## Partner Exercise: Comparing two Lists (5 mins)

Awesome job! Let's try a harder one. With the same partner, switch driver and navigator, and take a few minutes to try and solve this one. 

In a file (it can be the same one as before, if you'd like), write a function, `check_list_equality`, that takes in two lists, `first_list` and `second_list`, as parameters. Your function should return  `True` if the two lists contain the same elements in the same order. Otherwise, it returns `False`.

Examples of how this function can be used:

```python
list_one   = [1, 2, 3]
list_two   = [1, 2, 3]
list_three = [3, 2, 1]
list_four  = [1, 2, 3, 4]
print(check_list_equality(list_one, list_two))   # True
print(check_list_equality(list_one, list_three)) # False
print(check_list_equality(list_one, list_four))  # False
```

<details>
<summary><strong>Hint 1</strong></summary>
Start by making sure the lists have the same length!
</details>
<details>
<summary><strong>Hint 2</strong></summary>
You'll only need one <code>for</code> loop
</details>
<details>
<summary><strong>Hint 3</strong></summary>
You'll certainly need to use <code>range</code> and <code>len</code>
</details>

<details>
<summary>Answer (SPOILER!)</summary>
def check_list_equality(first_list, second_list):
    if len(first_list) != len(second_list):
        return False
    for i in range(len(first_list)):
        if first_list[i] != second_list[i]:
            return False
    return True
</details>

## You Do: Reversing a List (STRETCH, Take-Home Exercise)

This is a more challenging take-home exercise.

In a file (it can be the same one as before, if you'd like), write a function, `reverse_list`, that takes in a list, `my_list`, as a parameter.

Your function should reverse the list *in place* and return it.

An example of how this function can be used:

```python
my_list = [1, 2, 3, 4, 5]
reverse_list(my_list)
print(my_list)
#--> [5, 4, 3, 2, 1]
```

<details>
<summary><strong>Hint 1</strong></summary>
Do not declare another list -- your function should *modify* the existing list
</details>
<details>
<summary><strong>Hint 2</strong></summary>
Remember that you can access an item from the end of a list with a negative index. Example: <code>my_list[-2]</code> is 4, in the example above.
</details>
<details>
<summary><strong>Hint 3</strong></summary>
You'll certainly need to use <code>range</code> and <code>len</code>
</details>
<details>
<summary><strong>Hint 4</strong></summary>
Make sure your function works with lists that are both <em>even</em> and <em>odd</em> lengths
</details>

<details>
<summary>Answer (SPOILER!)</summary>
def reverse_list(my_list):
    for i in range(len(my_list) // 2):
        temp = my_list[i]
        my_list[i] = my_list[-i-1]
        my_list[-i-1] = temp
</details>


---

# Additional Resources

* [Python Lists - Khan Academy Video](https://www.youtube.com/watch?v=zEyEC34MY1A)
* [Google For Education: Python Lists](https://developers.google.com/edu/python/lists)
* [Python-Lists](https://www.tutorialspoint.com/python/python_lists.htm)
