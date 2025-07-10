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
