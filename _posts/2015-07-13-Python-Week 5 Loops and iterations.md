Introduces loops and iterations, example of infinite loop and using break&continue.
<!--more-->

---
{% include toc %}


---
# Week 5 Loops and iterations

---
## 1. While loops (indefinite)

**Loops** (repeated steps) have **iteration variables** that change each time through a loop.  Often these iteration 

>While loops are called "indefinite loops" because they keep going until   a logical condition becomes False


```
n = 5
while n > 0 :
    print n
    n = n – 1
print 'Blastoff!'
print n

```


## 2. Infinite loops

```
n = 5
while n > 0 :
    print 'Lather’
    print 'Rinse'
print 'Dry off!'

```

## 3. Using break

 - The **break** statement **ends** the **current loop** and jumps to the statement immediately following the loop 
 - It is like a loop test that can happen anywhere in the body of the loop


``` 
while True:
    line = raw_input('> ')
    if line == 'done' :
        break
    print line
print 'Done!'
```

```
> hello there
hello there
> finished
finished
> done
Done!
```

## 4. Using continue
The **continue** statement ends the current iteration and jumps to the **top of the loop** and starts the next iteration

```
while True:
    line = raw_input('> ')
    if line[0] == '#' :
        continue
    if line == 'done' 
:        break
    print line
print 'Done!'

```

```
> hello there
hello there
> # don't print this
> print this!
print this!
> done
Done!
```


## 5. For loops (definite)

- Quite often we have a **list** of items of the **lines in a file** effectively a **finite set** of things 
- We can write a loop to run the loop once for each of the items in a set using the Python **for** construct 
- These loops are called "**definite loops**" because they execute an exact number of times 
- We say that "**definite loops iterate through the members of a set**"

```
friends = ['Joseph', 'Glenn', 'Sally']
for friend in friends : 
   print 'Happy New Year:',  friend
print 'Done!'
```

```
Happy New Year: Joseph
Happy New Year: Glenn
Happy New Year: Sally
Done!
```

## 6. Iteration variables

 - The iteration variable “iterates” though the sequence (ordered set)
 - The block (body) of code is executed once for each value in the sequence 
 - The iteration variable moves through all of the values in the sequence


### 6.1 Counting in a Loop

```
zork = 0
print 'Before', zork
for thing in [9, 41, 12, 3, 74, 15] :
    zork = zork + 1
    print zork, thing
print 'After', zork

#To count how many times we execute a loop we introduce a counter variable that starts at 0 and we add one to it each time through the loop.

$ python countloop.py
Before 0
1 9
2 41
3 12
4 3
5 74
6 15
After 6

```

### 6.2 Summing in a Loop

```
zork = 0
print 'Before', zork
for thing in [9, 41, 12, 3, 74, 15] :
    zork = zork + thing
    print zork, thing
print 'After', zork

#To add up a value we encounter in a loop,  we introduce a sum variable that starts at 0 and we add the value to the sum each time through the loop.

$ python countloop.py 
Before 0
9 9
50 41
62 12
65 3
139 74
154 15
After 154
```

### 6.3 Finding the Average in a Loop

```
count = 0
sum = 0
print 'Before', count, sum
for value in [9, 41, 12, 3, 74, 15] :
    count = count + 1
    sum = sum + value
    print count, sum, value
print 'After', count, sum, sum / count

#An average just combines the counting and sum patterns and divides when the loop is done.

$ python averageloop.py 
Before 0 0
1 9 9
2 50 41
3 62 12
4 65 3
5 139 74
6 154 15
After 6 154 25
```

### 6.4 Filtering in a Loop

```
print 'Before'
for value in [9, 41, 12, 3, 74, 15] :
    if value > 20:
 	    print 'Large number',value
print 'After'

# We use an if statement in the loop to catch / filter the values we are looking for.

$ python search1.py 
Before
Large number 41
Large number 74
After
```

### 6.5 Search Using a Boolean Variable

```
found = False
print 'Before', found
for value in [9, 41, 12, 3, 74, 15] : 
   if value == 3 :
         found = True
    print found, value
print 'After', found

#If we just want to search and know if a value was found - we use a variable that starts at False and is set to True as soon as we find what we are looking for.

$ python search1.py 
Before False
False 9
False 41
False 12
True 3
True 74
True 15
After True

```


## 7. Largest or smallest

```
smallest = None #特殊类型变量
print 'Before'
for value in [9, 41, 12, 3, 74, 15] :
    if smallest is None : #IS是逻辑运算符，少用 主要是为了检查是否是 none 或 false
        smallest = value
    elif value < smallest : 
        smallest = value
    print smallest, value
print 'After', smallest

# We still have a variable that is the smallest so far.  The first time through the loop smallest is None so we take the first value to be the smallest.

    $ python smallest.py 
    Before
    9 9
    9 41
    9 12
    3 3
    3 74
    3 15
    After 3

```
