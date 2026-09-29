# PYTHON ASSIGNMENT

## Python Function Assignments: -

### 1.Write a function calculate(a, b, operation) that performs addition, subtraction, multiplication, or division based on the supplied operation.

### Program

```
def calculate(a,b,operation):
    if operation=='+':
        return a+b
    elif operation=='-':
        return a-b
    elif operation=='*':
        return a*b
    elif operation=='/':
        return a/b
    else:
        return "Invalid Input"

print(calculate(5,6,'+'))
```

### 2.Write a function sum_numbers(*args) that accepts any number of arguments and returns their sum.

### Program

```
def sum_numbers(*args):
    return sum(args)
    
a=sum_numbers(5,6,7,8)
print(a)
```

### 3.Write a function employee(**args) that accepts employee information such as name, ID, department and salary, then displays the information.

### Program

```
def employee(**args):
    print("Name",args["name"])
    print("ID",args["id"])
    print("Department",args["department"])
    print("Salary",args["salary"])
 
employee(name="Jana",id=1,department="CSE",salary=50000)
```

### 4.Write a function remove_duplicates(lst) that returns a list containing only unique elements while preserving their original order.

### Program

```
lis=eval(input())
se=set()
l=[]
for i in lis:
    if i not in se:
        se.add(i)
        l.append(i)
print(l)
```

### 5.Using a lambda function, sort a list of tuples based on the second element. Example: [(1,5), (2,3), (4,1)].

### Program

```
lis=eval(input())
b=sorted(lis,key=lambda a:a[1])
print(b)
```
## Python Question

### 1.Print all prime numbers between input range (Ex – input 20 50, prints all prime numbers between 20 and 50).
### Program
```
st=int(input())
en=int(input())
l=[]
for n in range(st,en+1):
    is_prime=True
    for i in range(2,int(n**0.5)+1):
        if (n%i==0):
            is_prime=False
            break
    if is_prime:
        l.append(n)
print(l)
```
### 2.Factorial using recursion
### Program
```
def fact(n):
    if(n<=1):
        return 1
    return fact(n-1)*n
print(fact(4))
```

### 3.Square of numbers using lambda
### Program
```
a=int(input())
b=lambda a:a**2
print(b(a))
```
### 4.Find the second largest element in a list
### Program
```
a=list(map(int,input().split(",")))
a=sorted(a)
print(a[-2])
```
### 5.Count frequency of characters in a string
### Program
```
a="Jana"
a=a.lower()
di=dict()
for i in a:
    di[i]=di.get(i,0)+1
print(di)    
```
### 6.Calculate area of a circle using math library.
### Program
```
import math
r=int(input())
val=math.pi*r*r
print(val)
```
### 7.Reverse a string without using built‑in reverse
### Program
```
a=input()
print(a[::-1])
```
### 8.Remove duplicates from a list
### Program
```
a=list(map(int,input().split(",")))
l=[]
s=set()
for i in a:
    if i not in s:
        s.add(i)
        l.append(i)
print(l)        
```
### 9.Merge two dictionaries
### Program
```
a={'a':100,'name':"jana",'id':10}
b={'b':101,'nname':"jara",'iid':1}
a.update(b)
print(a)
```
### 10.Fibonacci series using recursion
### Program
```
def fib(n):
    if(n<2):
        return n
    return fib(n-1)+fib(n-2)
a=int(input())
print(fib(a))
```









