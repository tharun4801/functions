# functions
#function calling and defining
def hi():
    print("good after to every one")
hi()
OUTPUT:
good after to every one
#func with parameter
def hi(name):
    print("Hello",name)
hi('gopi')
OUTPUT:
Hello gopi
#func with return values
def add(a,b):
    return a+b
x=int(input("enter the value of x:"))
y=int(input("enter the value of y:"))
result=add(x,y)
print("sum:",result)
OUTPUT:
enter the value of x: 3
enter the value of y: 4
sum: 7
#default parameters/func occupied parameters
def hi(name='doremon'):
    print("Hello",name)
hi()
hi("gopi")
OUTPUT:
Hello doremon
Hello gopi
4
'''write a function that carries and returns all the arthmetic operations to the main code(+,-,*)
pass the constraints,where all the constrants must be caliculated accordingly as return values and print
the calicu;ated by calling the same function'''
def arthamtic(a,b):
    A=a+b
    S=a-b
    M=a*b
    return f"sum:{A},diff:{S},mul:{M}"
x=int(input("enter the value of x:"))
y=int(input("enter the value of y:"))
print(arthamtic(x,y))
OUTPUT:
enter the value of x: 4
enter the value of y: 6
sum:10,diff:-2,mul:24

#functions with parameters/return values
def add(a,b):
    return a+b
student1=int(input("enter the money of student1:"))
student2=int(input("enter the money of student2:"))
total=add(student1,student2)
print("total amount of two students:",total)
OUTPUT:
enter the money of student1: 20
enter the money of student2: 30
total amount of two students: 50

def add(student1,student2):
    print("total:",student1+student2)
student1=int(input("enter the money:"))
student2=int(input("enter the money:"))
add(student1,student2)
OUTPUT:
enter the money: 20
enter the money: 30
total: 50

def get_name():
    name=input("enter the name:")
    return name
username=get_name()
print("WELCOME",username)
OUTPUT:
enter the name: Santhosh
WELCOME Santhosh

def eo(numbers):
    e=0
    o=0
    for n in numbers:
        if n % 2 == 0:
            e+=1
        else:
            o+=1
    return e,o
num=input("enter the number as space separated: ")
num_list=list(map(int,num.split()))
e,o=eo(num_list)
print("even count:",e)
print("odd count:",o)
OUTPUT:
enter the number as space separated:  44 56 77 2 8 66 999
even count: 5
odd count: 2

#functions within functions
def outer():
    print("this is a outer function .......")
    def inner():
        print("this is a inner function .......")
    inner()
outer()
OUTPUT:
this is a outer function .......
this is a inner function .......

def cal(a,b):
    def add():
        return a+b
    def sub():
        return a-b
    def mul():
        return a*b
    def div():
        return a/b if b!=0 else "cannot divide by zero" 
    print("Addition",add())
    print("Subtraction",sub())
    print("Product",mul())
    print("Division",div())
a=eval(input("enter the number:"))
b=eval(input("enter the number:"))
cal(a,b)
OUTPUT:
enter the number: 0
enter the number: 60
Addition 60
Subtraction -60
Product 0
Division 0.0

def mul_by(n):
    def inner(x):
        return x*n
    return inner
times_2=mul_by(2)
times_3=mul_by(3)
print(times_2(10))
print(times_3(15))
OUTPUT:
20
45

def greet(text):
    def inner(name):
        return f"{text},{name}!!!!!"
    return inner
hi=greet('Hello')
print(hi('santhosh'))
OUTPUT:
Hello,santhosh!!!!!

def titled(title):
    def greet(name):
        return f"Hello,{title}{name}"
    return greet
mr_greet=titled("Mr.")
dr_greet=titled("Dr.")
print(mr_greet("santhosh"))
print(dr_greet("Naga Venkata Rajesh"))
OUTPUT:
Hello,Mr.santhosh
Hello,Dr.Naga Venkata Rajesh

x=100
y=10
def display():
    x=22
    print("x= ",x)
    print("locally",x+y)
display()
print("x= ",x)
y=10
y=15
print("latest value of y globally:",y)
print("globally",x+y)
OUTPUT:
x=  22
locally 32
x=  100
latest value of y globally: 15
globally 115

total=0
def add_subject_marks():
    global total
    marks=int(input("enter the marks of a subject:"))
    total+=marks
    return marks
print("subject1 marks :",add_subject_marks())
print("subject2 marks :",add_subject_marks())
print("subject3 marks :",add_subject_marks())
print("subject4 marks :",add_subject_marks())
print("subject5 marks :",add_subject_marks())
print("total marks stored in golbal:",total)
OUTPUT:
enter the marks of a subject: 97
subject1 marks : 97
enter the marks of a subject: 98
subject2 marks : 98
enter the marks of a subject: 93
subject3 marks : 93
enter the marks of a subject: 94
subject4 marks : 94
enter the marks of a subject: 92
subject5 marks : 92
total marks stored in golbal: 474

subject_marks=[]
def add_subject_marks():
    mark=int(input("enter the,marksfor a subject:"))
    subject_marks.append(mark)
    return mark
print("Subject 1 marks:",add_subject_marks())
print("Subject 2 marks:",add_subject_marks())
print("Subject 3 marks:",add_subject_marks())
print("All subject marks",subject_marks)
total=sum(subject_marks)
l=len(subject_marks)
avg=total/l
print("Total marks",total)
print("average",avg)
OUTPUT:
enter the,marksfor a subject: 90
Subject 1 marks: 90
enter the,marksfor a subject: 90
Subject 2 marks: 90
enter the,marksfor a subject: 90
Subject 3 marks: 90
All subject marks [90, 90, 90]
Total marks 270
average 90.0

#global variables
fact=1
def factorial(n):
    global fact
    fact=1
    for i in range(1,n+1):
        fact*=i
    return fact
num=int(input("enter a number"))
if num<0:
    print("cannot derive factorial for negative number")
else:
    factorial(num)
    print(f"Factorial of {num} is {factorial(num)}")
OUTPUT:
enter a number 5
Factorial of 5 is 120

#while function
n=int(input("enter a number:"))
fact=1
i=1
while i<=n:
    fact*=i
    i+=1
print(f"Factorial of {n} is",fact)
OUTPUT:
enter a number: 4
Factorial of 4 is 24

#math function
import math
n=int(input("enter a number:"))
print(f"Factorial of {n} is {math.factorial(n)}")
OUTPUT:
enter a number: 4
Factorial of 4 is 24

# recursive function
def factorial(n):
    if n==0 or n==1:
        return 1
    return n*factorial(n-1)
num=int(input("enter a number:"))
value=factorial(num)
print(value)
OUTPUT:
enter a number: 5
120
