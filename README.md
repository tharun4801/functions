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
    return A,S,M
x=int(input("enter the value of x:"))
y=int(input("enter the value of y:"))
result=arthamtic(x,y)
print(arthamtic(x,y))
OUTPUT:
enter the value of x: 4
enter the value of y: 5
(9, -1, 20)

