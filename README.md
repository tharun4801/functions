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
