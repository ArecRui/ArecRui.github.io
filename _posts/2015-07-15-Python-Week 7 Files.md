﻿How to open & read & oprate a file.
<!--more-->

---
{% include toc %}

---

# Week7 Files

---
## 1.Secondary storage

---
## 2.Opening a file - file handle

 1. Before we can read the contents of the file we must tell Python which file we are going to work with and what we will be doing with the file
 2. This is done with the ***open()*** function
 3. ***open()*** returns a “***file handle***” - a variable used to perform operations on the file
 4. Kind of like “File -> Open” in a Word Processor

### 2.1 Using open()

handle = open(filename, mode)

```
fhand = open('mbox.txt', 'r')
```

 1. returns a handle use to manipulate the file 
 2. filename is a string
 3. mode is optional and should be 'r' if we are planning reading the file and 'w' if we are going to write to the file.

```
>>> fhand = open('mbox.txt')
>>> print fhand
<open file 'mbox.txt', mode 'r' at 0x1005088b0>\
```

### 2.3 When files are missing

```
>>> fhand = open('stuff.txt')
Traceback (most recent call last):  File "<stdin>", line 1, in <module>IOError: [Errno 2] No such file or directory: 'stuff.txt'
```

---

## 3.File structure - newline character

1. We use a special character to indicate when a line ends called the "newline"
1. We represent it as \n in strings 
1. Newline is still one character - not two

```
>>> stuff = 'Hello\nWorld!’
>>> stuff'Hello\nWorld!’
>>> print stuff
HelloWorld!
>>> stuff = 'X\nY’
>>> print stuff
X
Y
>>> len(stuff)3
```

---

## 4.Reading a file line-by-line with a for loop

 1. A file handle open for read can be treated as a sequence of strings where each line in the file is a string in the sequence
 2. We can use the for statement to iterate through a sequence
 3. Remember - a sequence is an ordered set

```
xfile = open('mbox.txt')
for cheese in xfile:
    print cheese
```

### 4.1 Counting Lines in a File

 1. Open a file read-only
 2. Use a for loop to read each line
 3. Count the lines and print out the number of lines

```
fhand = open('mbox.txt')
count = 0
for line in fhand:
     count = count + 1
print 'Line Count:', count

$ python open.py
Line Count: 132045

```

### 4.2 Reading the *Whole* File

We can read the whole file (newlines and all) into a single string.

```
>>> fhand = open('mbox-short.txt')
>>> inp = fhand.read()
>>> print len(inp)94626
>>> print inp[:20]From stephen.marquar
```

---

## 5.Searching for lines

### 5.1 using if to select

We can put an if statement in our for loop to only print lines that meet some criteria

```
fhand = open('mbox-short.txt')
for line in fhand:
      if line.startswith('From:') :
            print line
            
            
From: stephen.marquard@uct.ac.za

From: louis@media.berkeley.edu

From: zqian@umich.edu

From: rjlowe@iupui.edu

            
```

>Each line from the file has a newline at the end.
The print statement adds a newline to each line.

```
From: stephen.marquard@uct.ac.za\n
\n
From: louis@media.berkeley.edu\n
\n
From: zqian@umich.edu\n
\n
From: rjlowe@iupui.edu\n
\n
```

- We can strip the whitespace from the right hand side of the string using rstrip() from the string library
- The newline is considered "white space" and is stripped

```
fhand = open('mbox-short.txt')
for line in fhand:
      line = line.rstrip()
      if line.startswith('From:') :            
      
      
From: stephen.marquard@uct.ac.za
From: louis@media.berkeley.edu
From: zqian@umich.edu
From: rjlowe@iupui.edu
```

### 5.2 Skipping with continue

We can convienently skip a line by using the continue statement

```
fhand = open('mbox-short.txt')
for line in fhand:
    line = line.rstrip()
    if not line.startswith('From:') :
        continue
    print line
```

### 5.3 Using in to select lines

- We can look for a string anywhere in a line as our selection criteria

```
fhand = open('mbox-short.txt')
for line in fhand:
    line = line.rstrip()
    if not '@uct.ac.za' in line : 
        continue
    print line
```

---

## 6.Reading file names

Prompt for File Name

```
fname = raw_input('Enter the file name:  ')
fhand = open(fname)
count = 0
for line in fhand:
    if line.startswith('Subject:') :
        count = count + 1
print 'There were', count, 'subject lines in', fname

Enter the file name:  mbox.txt
There were 1797 subject lines in mbox.txt

Enter the file name: mbox-short.txt
There were 27 subject lines in mbox-short.txt
```

---

## 7.Dealing with bad files

```
fname = raw_input('Enter the file name:  ')
try:
    fhand = open(fname)
except:
    print 'File cannot be opened:', fname
    exit()
count = 0
for line in fhand:
    if line.startswith('Subject:') :
        count = count + 1
print 'There were', count, 'subject lines in', fname

Enter the file name: mbox.txt
There were 1797 subject lines in mbox.txt

Enter the file name: na na boo boo
File cannot be opened: na na boo boo
```


