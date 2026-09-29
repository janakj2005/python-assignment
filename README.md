# python-assignment

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
