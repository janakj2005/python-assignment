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


## NUMPY ASSIGNMENT

### Question 1 – Student Marks Array
### The marks obtained by five students in a subject are given as [78, 65, 89, 56, 92]. Create a NumPy array and display the array along with its basic properties.
### Program
```
import numpy as np 
marks = np.array([78, 65, 89, 56, 92]) 
print("Marks:", marks) 
print("Number of dimensions:", marks.ndim) 
print("Shape:", marks.shape) 
print("Size:", marks.size) 
print("Data type:", marks.dtype)
```
### Output:
Marks: [78 65 89 56 92]
Number of dimensions: 1
Shape: (5,)
Size: 5
Data type: int64

### Question 2 – Student Marks Access
### The marks of five students are stored in a NumPy array as [72, 85, 64, 90, 76]. Write a program to access and display specific student marks using NumPy indexing and slicing.
### Program
```
import numpy as np
marks = np.array([72, 85, 64, 90, 76])
print("Marks:", marks)
print("First student:", marks[0])
print("Third student:", marks[2])
print("Last student:", marks[4])
print("First three students:", marks[0:3])
print("Students 2 to 4:", marks[1:4])
```
###Output:

Marks: [72 85 64 90 76]
First student: 72
Third student: 64
Last student: 76
First three students: [72 85 64]
Students 2 to 4: [85 64 90]

### Question 3 – Subject-wise Marks
### The marks obtained by five students in three subjects are given below. Create a NumPy array to represent the data and reshape it into an appropriate matrix format.
[78, 85, 90, 65, 72, 80, 88, 91, 84, 56, 62, 70, 95, 89, 92]

import numpy as np
marks = np.array([78, 85, 90, 65, 72, 80, 88, 91, 84, 56, 62, 70, 95, 89, 92])
matrix = marks.reshape(5, 3)
print("Marks:")
print(matrix)

Output:
Marks:
[[78 85 90]
 [65 72 80]
 [88 91 84]
 [56 62 70]
 [95 89 92]]

Question 4 – Internal and External Marks
The internal and external examination marks of five students are stored in two NumPy arrays. Write a program to calculate the final marks of each student using NumPy array operations.

import numpy as np
internal = np.array([20, 18, 22, 19, 21])
external = np.array([70, 65, 68, 72, 75])
final_marks = internal + external
print("Internal marks:", internal)
print("External marks:", external)
print("Final marks:", final_marks)

Output:
Internal marks: [20 18 22 19 21]
External marks: [70 65 68 72 75]
Final marks: [90 83 90 91 96]

Question 5 – Pass Percentage Analysis
The marks obtained by five students are [45, 78, 56, 32, 91]. Using NumPy Boolean masking, identify the students who have secured 50 marks or above.

import numpy as np
marks = np.array([45, 78, 56, 32, 91])
passed = marks[marks >= 50]
print("Marks:", marks)
print("Students who scored 50 or above:", passed)

Output:
Marks: [45 78 56 32 91]
Students who scored 50 or above: [78 56 91]

Question 6 – Average Marks
The marks of five students in three subjects are represented using a NumPy matrix. Write a program to calculate the average marks of each student.

import numpy as np
marks = np.array([
    [78, 85, 90],
    [65, 72, 80],
    [88, 91, 84],
    [56, 62, 70],
    [95, 89, 92]
])
average = np.mean(marks, axis=1)
print("Marks:")
print(marks)
print("Average marks of each student:", average)

Output:
Marks:
[[78 85 90]
 [65 72 80]
 [88 91 84]
 [56 62 70]
 [95 89 92]]
Average marks of each student: [84.33333333 72.33333333 87.66666667 62.66666667 92.]

Question 7 – Class Performance Statistics
The marks obtained by five students are [67, 82, 91, 74, 58]. Using NumPy statistical functions, determine the total, average, highest, lowest, and standard deviation of the marks.

import numpy as np
marks = np.array([67, 82, 91, 74, 58])
total = np.sum(marks)
average = np.mean(marks)
highest = np.max(marks)
lowest = np.min(marks)
standard_deviation = np.std(marks)
print("Marks:", marks)
print("Total:", total)
print("Average:", average)
print("Highest:", highest)
print("Lowest:", lowest)
print("Standard deviation:", standard_deviation)

Output:
Marks: [67 82 91 74 58]
Total: 372
Average: 74.4
Highest: 91
Lowest: 58
Standard deviation: 11.46472851837321

Question 8 – Subject-wise Performance
The marks of five students in three subjects are stored in a NumPy matrix. Write a program to calculate the total marks obtained in each subject using an appropriate axis operation.

import numpy as np
marks = np.array([
[78, 85, 90],
[65, 72, 80],
[88, 91, 84],
[56, 62, 70],
[95, 89, 92]
])
subject_total = np.sum(marks, axis=0)
print("Marks:")
print(marks)
print("Total marks in each subject:", subject_total)

Output:
Marks:
[[78 85 90]
 [65 72 80]
 [88 91 84]
 [56 62 70]
 [95 89 92]]
Total marks in each subject: [382 399 416]

Question 9 – Student-wise Performance
The marks of five students in three subjects are stored in a NumPy matrix. Write a program to calculate the total marks obtained by each student using an appropriate axis operation.

import numpy as np
marks = np.array([
[78, 85, 90],
[65, 72, 80],
[88, 91, 84],
[56, 62, 70],
[95, 89, 92]
])
student_total = np.sum(marks, axis=1)
print("Marks:")
print(marks)
print("Total marks of each student:", student_total)

Output:
Marks:
[[78 85 90]
 [65 72 80]
 [88 91 84]
 [56 62 70]
 [95 89 92]]
Total marks of each student: [253 217 263 188 276]

Question 10 – Student Ranking
The total marks obtained by five students are [245, 278, 219, 290, 256]. Use NumPy sorting and indexing operations to arrange the marks in order and determine the ranking of the students.

import numpy as np
marks = np.array([245, 278, 219, 290, 256])
order = np.argsort(marks)[::-1]
print("Marks:", marks)
print("Marks in descending order:", marks[order])
print("Ranking:")
for i in order:
print("Student", i + 1, "-", marks[i])

Output:
Marks: [245 278 219 290 256]
Marks in descending order: [290 278 256 245 219]
Ranking:
Student 4 - 290
Student 2 - 278
Student 5 - 256
Student 1 - 245
Student 3 - 219

Question 11 – Duplicate Marks Analysis
The marks obtained by five students are [85, 92, 85, 76, 92]. Use NumPy functions to identify the unique marks obtained by the students.

import numpy as np
marks = np.array([85, 92, 85, 76, 92])
unique_marks = np.unique(marks)
print("Marks:", marks)
print("Unique marks:", unique_marks)

Output:
Marks: [85 92 85 76 92]
Unique marks: [76 85 92]

Question 12 – Missing Marks
The marks of five students are represented as [78, 85, np.nan, 92, 67], where np.nan represents a missing mark. Write a NumPy program to calculate the average marks without considering the missing value.

import numpy as np
marks = np.array([78, 85, np.nan, 92, 67])
average = np.nanmean(marks)
print("Marks:", marks)
print("Average without missing mark:", average)

Output:
Marks: [78. 85. nan 92. 67.]
Average without missing mark: 80.5

Question 13 – Grade Classification
The marks obtained by five students are [95, 82, 74, 61, 45]. Using NumPy conditional operations, classify the students into appropriate grade categories based on their marks.

import numpy as np
marks = np.array([95, 82, 74, 61, 45])
conditions = [
    marks >= 90,
    marks >= 80,
    marks >= 70,
    marks >= 60,
    marks < 60
]
grades = ['A', 'B', 'C', 'D', 'F']
result = np.select(conditions, grades, default='F')
print("Marks:", marks)
print("Grades:", result)

Output:
Marks: [95 82 74 61 45]
Grades: ['A' 'B' 'C' 'D' 'F']

Question 14 – Random Marks Generation
Generate marks for five students using NumPy's random number generation functionality. Perform basic statistical analysis on the generated marks.

import numpy as np
marks = np.random.randint(0, 101, 5)
print("Generated marks:", marks)
print("Total:", np.sum(marks))
print("Average:", np.mean(marks))
print("Highest:", np.max(marks))
print("Lowest:", np.min(marks))
print("Standard deviation:", np.std(marks))


Output:
Generated marks: [40 16 73 99 57]
Total: 285
Average: 57.0
Highest: 99
Lowest: 16
Standard deviation: 28.24889378365107

Question 15 – Student Performance Analysis
The marks of five students in three subjects are stored in a NumPy array. Develop a program to perform a complete student performance analysis by calculating the total marks, average marks, highest marks, lowest marks, and identifying students who perform above the class average.

import numpy as np
marks = np.array([
    [78, 85, 90],
    [65, 72, 80],
    [88, 91, 84],
    [56, 62, 70],
    [95, 89, 92]
])
total = np.sum(marks, axis=1)
average = np.mean(marks, axis=1)
highest = np.max(marks, axis=1)
lowest = np.min(marks, axis=1)
class_average = np.mean(average)
above_average = average > class_average
print("Marks:")
print(marks)
print("Total marks:", total)
print("Average marks:", average)
print("Highest mark:", highest)
print("Lowest mark:", lowest)
print("Class average:", class_average)
print("Students above class average:", above_average)
print("Student numbers above class average:")
for i in range(len(average)):
    if average[i] > class_average:
        print("Student", i + 1)


Output:
Marks:
[[78 85 90]
 [65 72 80]
 [88 91 84]
 [56 62 70]
 [95 89 92]]
Total marks: [253 217 263 188 276]
Average marks: [84.33333333 72.33333333 87.66666667 62.66666667 92.        ]
Highest mark: [90 80 91 70 95]
Lowest mark: [78 65 84 56 89]
Class average: 79.8
Students above class average: [ True False  True False  True]
Student numbers above class average:
Student 1
Student 3
Student 5






