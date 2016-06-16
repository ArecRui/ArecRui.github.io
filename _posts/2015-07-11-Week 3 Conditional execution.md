The concept of conditional execution and basic examples.
<!--more-->

---
{% include toc %}
teaser: "Python.jpg"

---
# Week 3 Conditional execution

----------
### 1. Conditional Steps

```flow
st=>start: x=5
e=>end: print 'finis'
cond1=>condition: x<10?
op1=>operation: print 'Smaller'
cond2=>condition: x>20?
op2=>operation: print 'Bigger'
st->cond1->cond2
cond1(yes)->op1->e
cond1(no)->cond2
cond2(yes)->op2->e
cond2(no)->e
```

----------

### 2. Comparison Operators

    <     less than
    <=	  less than or equal
    ==    equal to
    >=    greater than or equal
    >     greater than 
    !=    not equal
    
1. **Boolean expressions** ask a question and produce a Yes or No result which we use to control program flow
2. **Boolean expressions** using ***comparison operators***  evaluate to - **True / False** - **Yes / No**
3. **Comparison operators** look at variables but **do not** change the variables

----------  

### 3. Logical operators: and or not


----------

### 4. Indentation

`Indentation` **DO** `matter in python.`
1. **Increase indent** after an if statement or for statement (after : )
2. **Maintain indent** to indicate the scope of the block (which lines are affected by the if/for)
3. **Reduce indent** to back to the level of the if statement or for statement to indicate the end of the block
4. ***Blank lines are ignored*** - they do not affect indentation
5. **Comments** on a line by themselves **are ignored**
>**Warning: Turn Off Tabs** 
Or change the editor setting
                
----------

### 5. One Way Decisions


#### 5.1 流程图如下


```flow
st=>start: x=5
e=>end: print 'Afterwards 5'
cond1=>condition: x==5?
op1=>operation: print 'is 5'
op2=>operation: print 'Still 5'
op3=>operation: print 'Third 5'
op4=>operation: print 'Before 5'
st->op4->cond1->e
cond1(yes)->op1->op2->op3->e
cond1(no)->e
```


#### 5.2 代码如下：

```python
    x = 5
	print 'Before 5’
	if  x == 5 :
	    print 'Is 5’
	    print 'Is Still 5’
	    print 'Third 5’
	print 'Afterwards 5’
```



#### 5.3 显示结果如下：


```
    Before 5
	Is 5
	Is Still 5
	Third 5
	Afterwards 5
```

----------

### 6. Two way Decisions  if :  and else :


#### 6.1 流程图如下：

```flow
st=>start: x=4
e=>end: print 'All Done'
op1=>operation: print 'Smaller'
op2=>operation: print 'Bigger'
cond1=>condition: x>2
st->cond1
cond1(yes)->op2->e
cond1(no)->op1->e
```

#### 6.2 代码如下：

```python
    x=4
    if x>2:
	    print 'Bigger'
	else:
		print 'Smaller'
	print 'All Done'
```


----------

### 7. Nested Decisions(嵌套)

#### 7.1 流程图如下：

```flow
st=>start: start
e=>end: end
cond1=>condition: x>1
cond2=>condition: x<100
op1=>operation: print 'More than one'
op2=>operation: print 'Less than 100'
op2=>operation: print 'All Done'
st->cond1->e
cond1(no)->e
cond1(yes)->op1->cond2
cond2(yes)->op2->e
cond2(no)->e

```

#### 7.2 代码如下：

```python
    x = 42

	if x > 1 :
	    print 'More than one'
	    if x < 100 : 
	        print 'Less than 100'

	print 'All done'
```


----------

### 8. Multiway decisions using elif

#### 8.1 流程图如下:

```flow
st=>start: start
cond1=>condition: x<2
cond2=>condition: x<10
cond3=>condition: x<20
cond4=>condition: x<40
cond5=>condition: x<100
op1=>operation: print 'Small'
op2=>operation: print 'Medium'
op3=>operation: print 'Big'
op4=>operation: print 'Large'
op5=>operation: print 'Huge'
op6=>operation: print 'Ginormous'
st->cond1
cond1(yes)->op1
cond2(yes)->op2
cond3(yes)->op3
cond4(yes)->op4
cond5(yes)->op5
cond1(no)->cond2
cond2(no)->cond3
cond3(no)->cond4
cond4(no)->cond5
cond5(no)->op6->e
```

#### 8.2代码如下：

```python
    if x < 2 :
	    print 'Small'
	elif x < 10 :
	    print 'Medium'
	elif x < 20 : 
	    print 'Big'
	elif x< 40 : 
	    print 'Large'
	elif x < 100:
	    print 'Huge'
	else :
    print 'Ginormous'
```    

#### 8.3 Multi-way Puzzles-Which will never print?

```python
if x < 2 :
    print 'Below 2'
elif x >= 2 : 
    print 'Two or more'
**else : #此行之后不执行
    print 'Something else'** 
```

```python
if x < 2 :
    print 'Below 2'
elif x < 20 :
    print 'Below 20'
**elif x < 10 :  #以下两行不执行
    print 'Below 10'**
else :
    print 'Something else'
```

----------

### 9. Try / Except to compensate for errors

1. You surround a dangerous section of code with **try and except**.
2. If the code in the try **works** - the except is skipped
3. If the code in the try **fails** - it jumps to the except section

#### 9.1 示例代码如下：

```python
rawstr = raw_input('Enter a number:')
try: 
    ival = int(rawstr)
except: 
    ival = -1

if ival > 0 :  
    print 'Nice work'else:  
    print 'Not a number'
```

----------

### 10. Exercise

#### 10.1 Exercise 3.1 

Rewrite your pay computation to give the employee 1.5 times the hourly rate for hours worked above40 hours.

```python
hours=raw_input("How many hours do you work per week?\n")
try: 
    Hours = float(hours)
    rate=raw_input("How much do you get paid per hour?\n")
    try: 
        Rate = float(rate)
        if Hours < 40 :
            TotalPay=float(Hours)* float(Rate)
            print "So, you get paid " + str(TotalPay) + " per week?" 
        else:
            TotalPay=(float(Hours)-40)*1.5*float(Rate)+40*float(Rate)
            print "So, you get paid " + str(TotalPay) + " dollars per week?"
    except: 
        Rate = -1
    if Rate <0 :
        print "Please enter numeric input!"
except: 
    Hours = -1
if Hours <0 :
    print "Please enter numeric input!"
```

#### 10.2 Exercise 3.3 

Write a program to prompt for a score between 0.0 and 1.0. If the score is out of range print an error. If the score is between 0.0 and 1.0, print a grade using the following table:

```python
score=raw_input("Please input the score!\n")
try:
    Score = float(score)
    if Score < 0.6 :
        print "Your Grade is F!"
    elif Score < 0.7 :
        print "Your Grade is D!"
    elif Score < 0.8 :
        print "Your Grade is C!"
    elif Score < 0.9 :
        print "Your Grade is B!"
    elif Score < 1.0 :
        print "Your Grade is A!"
    else :
        print "Please enter the right score!"
except:
    Score = -1
if Score < 0 :
    print "Error, please enter numeric input!"
```
