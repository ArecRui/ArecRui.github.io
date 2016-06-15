{% include toc %}

# Week 2 expressions


标签（空格分隔）： python

---
### 1. Values and types
### 15. Exercises
2.2 Write a program that uses raw_input to prompt a user for their name and then welcomes them.
```
Name=raw_input('Hi! What is your name?\n')
print 'Hello '+ Name + ', welcome to the new world !'
```
2.3 Write a program to prompt the user for hours and rate per hour to compute gross pay
```
Hours=raw_input("How many hours do you work per day?\n")
Rate=raw_input("How much do you get paid for an hours?\n")
TotalHours=float(Hours)* float(Rate)
print "So, you work " + str(TotalHours) + " hours per week?"
```
2.5 Write a program to prompt the user for a Celsius temperature, convert the temperature to Fahrenheit and print out the converted temperature.
```
Ctemp=raw_input("Please enter the Celsius temperature:\n")
Ftemp=(int(Ctemp)*9/5)+32
print str(Ctemp) + ' degree celsius is ' + str(Ftemp) + ' degree fahrenheit!\n '
```




