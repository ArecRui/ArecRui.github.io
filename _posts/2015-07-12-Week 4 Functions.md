---

{% include toc %}

---

# Week 4 Functions 


标签（空格分隔）： python

----------

### 1.Stored (and reused) Steps

```
def hello(): #定义函数(store)
    print 'Hello'
    print 'Fun'
    
hello() #调用函数(reuse)
print 'Zip'
hello() #调用函数(reuse)
```

>
**Type Conversion** 
Built in functions **int()** and **float()**

----------

### 2.Python Functions

#### 2.1. **Built in functions** that are provided 

-input: raw_input()
-type conversions: type()
-string conversions: str() int()

#### 2.2. **Defined functions**

-**arguments** as input
-**def** to define

```
big= max('Hello world') #定义函数 不会执行
print big #调用函数 执行
```

>**Names** of built in function == **New reserved words**

----------

### 3.Arguments 

>- is a value pass into the function 
- need to be in the ()
 
#### 3.1 Parameters

>A parameter is a variable which we use in the functions


 definition that is a “handle” that allows the code in the function to access the arguments for a particular function invocation.


```
        def greet(lang):
            if lang == 'es':
               print 'Hola’
            elif lang == 'fr':
               print 'Bonjour’
            else:
               print 'Hello’
    greet('en')Hello
    greet('es')Hola
    greet('fr')Bonjour
```

#### 3.2 Return Values

>Often a function will take its arguments, do some computation and **return** a value to be used as the value of the function call in the **calling expression**.  The return keyword is used for this.

```
>>> def greet(lang):
...         if lang == 'es':
...            return 'Hola’
...         elif lang == 'fr':
...            return 'Bonjour’
...         else:
...            return 'Hello’
... >>> print greet('en'),'Glenn’
Hello Glenn
>>> print greet('es'),'Sally’
Hola Sally
>>> print greet('fr'),'Michael’
Bonjour Michael
>>> 
```
