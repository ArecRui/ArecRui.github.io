This course introduces the concept of collection/list etc.
<!--more-->

---
{% include toc %}
teaser: Python.jpg

---


## 1. Concept of a collection

- A collection ***allows*** us to ***put many values*** in a ***single “variable”***
- A collection is nice because we can carry all many values around in one convenient package.

```python
friends = [ 'Joseph', 'Glenn', 'Sally' ]

carryon = [ 'socks', 'shirt', 'perfume' ]
```

- What is not a “Collection”
   - Most of our variables have one value in them - when we put a new value in the variable - the old value is over written

```
$ python
Python 2.5.2 (r252:60911, Feb 22 2008, 07:57:53)
[GCC 4.0.1 (Apple Computer, Inc. build 5363)] on darwin
>>> x = 2
>>> x = 4
>>> print x
4
```

---

## 2. Lists and definite loops

- List constants are surrounded by square brackets and the elements in the list are separated by commas.
- A list element can be any Python object - even another list
- A list can be empty

```
>>> print [1, 24, 76]
[1, 24, 76]
>>> print ['red', 'yellow', 'blue']
['red', 'yellow', 'blue']
>>> print ['red', 24, 98.6]
['red', 24, 98.599999999999994]
>>> print [ 1, [5, 6], 7]
[1, [5, 6], 7]
>>> print []
[]
```

---

## 3. Indexing and lookup

```
friends = ['Joseph', 'Glenn', 'Sally']
for friend in friends :
    print 'Happy New Year:',  friend
print 'Done!'

Happy New Year: Joseph
Happy New Year: Glenn
Happy New Year: SallyDone!
```

- Just like strings, we can get at any single element in a list using an index specified in square brackets

```
>>> friends = [ 'Joseph', 'Glenn', 'Sally' ]
>>> print friends[1]
Glenn
>>>
```


---

## 4. List mutability

- Strings are "immutable" - we cannot change the contents of a string - we must make a new string to make any change
- Lists are "mutable" - we can change an element of a list using the index operator

```
>>> fruit = 'Banana’
>>> fruit[0] = 'b’
Traceback
TypeError: 'str' object does not
support item assignment
>>> x = fruit.lower()
>>> print x
banana
>>> lotto = [2, 14, 26, 41, 63]
>>> print lotto[2, 14, 26, 41, 63]
>>> lotto[2] = 28
>>> print lotto
[2, 14, 28, 41, 63]
```

---

## 5. Functions: len, min, max, sum

- The len() function takes a list as a parameter and returns the number of elements in the list
- Actually len() tells us the number of elements of any set or sequence (i.e. such as a string...)

```
>>> greet = 'Hello Bob'
>>> print len(greet)
9
>>> x = [ 1, 2, 'joe', 99]
>>> print len(x)
4
>>>
```


---

## 6. Slicing lists

---

## 7. List methods: append, remove

---

## 8. Sorting lists

---

## 9. Splitting strings into lists of words

---

## 10. Using split to parse strings
