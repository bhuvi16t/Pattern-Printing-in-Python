
# Pattern Printing in Python

This project consists of Python code for printing various patterns using nested loops. It demonstrates how to print different shapes and patterns like triangles, pyramids, and squares, using basic concepts of loops and conditionals in Python.

## Patterns Included

### 1. Right-Angled Triangle

This pattern forms a right-angled triangle of stars (`*`), where the number of stars increases with each row.

Example output:

```
* 
* * 
* * * 
* * * * 
* * * * *
```

Code:
```python
def Right_angle(n):
    for i in range(n):
        for j in range(i+1):
            print('*', end=' ')
        print()
```

### 2. Inverted Right-Angled Triangle

This pattern forms an inverted right-angled triangle, with the number of stars decreasing with each row.

Example output:

```
* * * * * 
* * * * 
* * * 
* * 
* 
```

Code:
```python
def Inverted_Right_angle(n):
    for i in range(n):
        for j in range(n-i):
            print('*', end=' ')
        print()
```

### 3. Pyramid Pattern

This pattern creates a pyramid shape with stars.

Example output:

```
    *    
   * *   
  * * *  
 * * * * 
* * * * *
```

Code:
```python
def pyramiid(n):
    for i in range(n):
        for j in range(n-i):
            print('', end=' ')
        for k in range(i+1):
            print('*', end=' ')
        print()
```

### 4. Diamond Pattern

This pattern forms a diamond shape with stars.

Example output:

```
    *    
   * *   
  * * *  
 * * * * 
* * * * *
 * * * * 
  * * *  
   * *   
    *    
```

Code:
```python
def diamond(n):
    for i in range(n):
        for j in range(n-i):
            print('', end=' ')
        for k in range(i+1):
            print('*', end=' ')
        print()
    for i in range(n - 1, 0, -1):
        print(" " * (n - i) + " *" * i)
```

### 5. Hollow Square Pattern

This pattern forms a square with stars, with hollow spaces in the middle.

Example output:

```
* * * * *
*       *
*       *
*       *
* * * * *
```

Code:
```python
def hollowSquare(n):
    for i in range(n):
        if i == 0 or i == n-1:
            print("* " * n)
        else:
            print("* " + "  " * (n - 2) + "*")
```

### 6. Floyd’s Triangle

This pattern creates a triangle where each row has consecutive numbers starting from 1.

Example output:

```
1
2 3
4 5 6
7 8 9 10
```

Code:
```python
def floyds(row):
    n = 1
    for i in range(1, row + 1):
        for j in range(i):
            print(n, end=" ")
            n += 1
        print()
```

### 7. Number Pyramid

This pattern forms a pyramid where each row is filled with the row number repeated multiple times.

Example output:

```
    1    
   2 2   
  3 3 3  
 4 4 4 4 
5 5 5 5 5
```

Code:
```python
def numberPyramid(n):
    for i in range(1, n+1):
        for j in range(n-i):
            print(' ', end='')
        for k in range(i):
            print(i, end=' ')
        print()
```

### 8. Pascal's Triangle

This pattern prints Pascal's Triangle, where each number is the sum of the two numbers directly above it.

Example output:

```
        1
       1 1
      1 2 1
     1 3 3 1
    1 4 6 4 1
```

Code:
```python
def pascal_triangle(n):
    for i in range(n):
        print(" " * (n - i), end="")
        val = 1
        for j in range(i + 1):
            print(val, end=" ")
            val = val * (i - j) // (j + 1)
        print()
```

## Author

Bhoopendra Vishwakarma

[LinkedIn Profile](https://www.linkedin.com/in/bhoopendra-vishwakarma-0951b3296/)
