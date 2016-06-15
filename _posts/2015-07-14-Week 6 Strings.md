---

{% include toc %}

---

# Week 6 Strings

标签（空格分隔）： python



---

## 1.String type

- A string is a **sequence of characters**
- A string literal **uses quotes**  'Hello' or “Hello”
- For strings, **+ means “concatenate”**
- When a string contains numbers, it is still a string
- We can convert numbers in a string into a number using int()

```
>>> str1 = "Hello"
>>> str2 = 'there'
>>> bob = str1 + str2
>>> print bob
Hellothere
>>> str3 = '123'
>>> str3 = str3 + 1
Traceback (most recent call last):  File "<stdin>", line 1, in <module>TypeError: cannot concatenate 'str' and 'int' objects
>>> x = int(str3) + 1
>>> print x
124
>>> 

```

---

## 2.Read/Convert

- We prefer to read data in using strings and then parse and convert the data as we need
- This gives us more control over error situations and/or bad user input
- Raw input numbers must be converted from strings

```
>>> name = raw_input('Enter:')
Enter:Chuck
>>> print name
Chuck
>>> apple = raw_input('Enter:')
Enter:100
>>> x = apple – 10
Traceback (most recent call last):  File "<stdin>", line 1, in <module>TypeError: unsupported operand type(s) for -: 'str' and 'int'
>>> x = int(apple) – 10
>>> print x
90

```

---

## 3.Indexing strings []

- We can get at any ***single character*** in a string using an index specified in square brackets
- The index value must be an ***integer*** and starts at ***zero***
- The index value can be an expression that is computed

```
>>> fruit = 'banana'
>>> letter = fruit[1]
>>> print letter
a
>>> n = 3
>>> w = fruit[n - 1]
>>> print w
n

```

- You will get a python error if you attempt to index beyond the end of a string.
- So be careful when constructing index values and slices

```
>>> zot = 'abc'
>>> print zot[5]
Traceback (most recent call last):  File "<stdin>", line 1, in <module>IndexError: string index out of range
>>> 

```

### 3.1 length of strings

There is a built-in function len that gives us the length of a string

```
>>> fruit = 'banana'
>>> print len(fruit)
6
```
```
>>> fruit = 'banana'
>>> x = len(fruit)
>>> print x
6

```

> A function is some **stored code** that we use. A function takes some **input** and produces an **output**.


---

## 4.Slicing strings [2:4]

- We can also look at any continuous section of a string using a colon operator
- The second number is one beyond the end of the slice - “up to but not including”
- If the second number is beyond the end of the string, it stops at the end 

```
>>> s = 'Monty Python'
>>> print s[0:4]
Mont
>>> print s[6:7]
P
>>> print s[6:20]
Python
```

- If we leave off the first number or the last number of the slice, it is assumed to be the beginning or end of the string respectively

```
>>> s = 'Monty Python'
>>> print s[:2]
Mo
>>> print s[8:]
Thon
>>> print s[:]
Monty Python
```

---

## 5.Looping through strings with for and while

- Using a while statement and an iteration variable, and the len function, we can construct a loop to look at each of the letters in a string individually

```
fruit = 'banana'
index = 0
while index < len(fruit) : 
   letter = fruit[index]
    print index, letter
    index = index + 1

0 b
1 a
2 n
3 a
4 n
5 a

```

- A definite loop using a for statement is much more elegant
The iteration variable is completely taken care of by the for loop

```
fruit = 'banana'
for letter in fruit : 
   print letter

b
a
n
a
n
a

```

- This is a simple loop that loops through each letter in a string and counts the number of times the loop encounters the 'a' character.

```
word = 'banana'
count = 0
for letter in word :
    if letter == 'a' : 
       count = count + 1
print count

```

- The **iteration variable** “iterates” through the **sequence** (ordered set)
- The **block (body)** of code is executed once for each value **in** the **sequence**
- The **iteration variable** moves through all of the values **in** the **sequence**

---

## 6.Concatenating strings with +

- When the + operator is applied to strings, it means "concatenation"

```
>>> a = 'Hello'
>>> b = a + 'There'
>>> print b
HelloThere
>>> c = a + '  ' + 'There'
>>> print c
Hello There
>>> 
```

---

## 7.String operations 

- Python has a number of ***string functions*** which are in the string library
- These functions are ***already built*** into every string - we invoke them by appending the function to the string variable
- These functions ***do not modify*** the original string, instead they ***return a new string*** that has been altered

```
>>> stuff = 'Hello world’
>>> type(stuff)<type 'str'>
>>> dir(stuff)
['capitalize', 'center', 'count', 'decode', 'encode', 'endswith', 'expandtabs', 'find', 'format', 'index', 'isalnum', 'isalpha', 'isdigit', 'islower', 'isspace', 'istitle', 'isupper', 'join', 'ljust', 'lower', 'lstrip', 'partition', 'replace', 'rfind', 'rindex', 'rjust', 'rpartition', 'rsplit', 'rstrip', 'split', 'splitlines', 'startswith', 'strip', 'swapcase', 'title', 'translate', 'upper', 'zfill']

```

### 7.1 String Comparison

```
if word == 'banana':
    print  'All right, bananas.'

if word < 'banana':
    print 'Your word,' + word + ', comes before banana.’
elif word > 'banana':
    print 'Your word,' + word + ', comes after banana.’
else:
    print 'All right, bananas.'
```

### 7.2 Searching a String

- We use the find() function to search for a substring within another string
- ***find()*** finds the first occurance of the substring
If the substring is not found, find() returns -1
Remember that string position starts at zero

```
>>> fruit = 'banana'
>>> pos = fruit.find('na')
>>> print pos
2
>>> aa = fruit.find('z')
>>> print aa
-1
```

### 7.3 Making everything UPPER CASE

- You can make a copy of a string in lower case or upper case
- Often when we are searching for a string using find()- we first convert the string to lower case so we can search a string regardless of case

```
>>> greet = 'Hello Bob'
>>> nnn = greet.upper()
>>> print nnn
HELLO BOB
>>> www = greet.lower()
>>> print www
hello bob
>>> 

```

### 7.4 Search and Replace

- The ***replace()*** function is like a “search and replace” operation in a word processor
- It replaces *all occurrences* of the search string with the ***replacement string***

```
>>> greet = 'Hello Bob'
>>> nstr = greet.replace('Bob','Jane')
>>> print nstr
Hello Jane
>>> nstr = greet.replace('o','X')
>>> print nstrHellX BXb
>>> 
```

### 7.5 Stripping Whitespace

- Sometimes we want to take a string and remove whitespace at the beginning and/or end
- ***lstrip()*** and ***rstrip()*** to the left and right only
- ***strip()*** Removes both begin and ending whitespace


```
>>> greet = '   Hello Bob  '
>>> greet.lstrip()
'Hello Bob  '
>>> greet.rstrip()
'   Hello Bob'
>>> greet.strip()
'Hello Bob'
>>> 
```

### 7.6 Prefixes

```
>>> line = 'Please have a nice day’
>>> line.startswith('Please')
True
>>> line.startswith('p')
False
```

### 7.7 Parsing and Extracting

From stephen.marquard@uct.ac.za Sat Jan  5 09:14:16 2008

```
>>> data = 'From stephen.marquard@uct.ac.za Sat Jan  5 09:14:16 2008’
>>> atpos = data.find('@')
>>> print atpos
21
>>> sppos = data.find(' ',atpos)
>>> print sppos
31
>>> host = data[atpos+1 : sppos]
>>> print host
uct.ac.za

```















