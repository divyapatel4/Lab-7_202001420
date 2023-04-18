# IT314-Lab7

## **Name - Divya Kirtikumar Patel**

## **ID - 202001420**

## **Section A**

**Consider a program for determining the previous date. Its input is triple of day, month and year with the following ranges 1 <= month <= 12, 1 <= day <= 31, 1900 <= year <= 2015.The possible output dates would be previous date or invalid date. Design the equivalence class test cases? 
Write a set of test cases (i.e., test suite) – specific set of data – to properly test the programs. Your test suite should include both correct and incorrect inputs.** 

1. **Enlist which set of test cases have been identified using Equivalence Partitioning and Boundary ValueAnalysis separately.**
2. **Modify your programs such that it runs on eclipse IDE, and then execute your test suites on theprogram. While executing your input data in a program, check whether the identified expectedoutcome (mentioned by you) is correct or not.**

**Table 1: Equivalence Partitioning for Day**

| Partition ID | Range | Status |
| --- | --- | --- |
| EP1 | 1-28 | Valid |
| EP2 | <1 | Invalid |
| EP3 | >31 | Invalid |
| EP4 | =30 | Valid |
| EP5 | =29 | Valid for leap year |
| EP6 | =31 | Valid |

**Table 2: Equivalence Partitioning for Month**

| Partition ID | Range | Status |
| --- | --- | --- |
| EP7 | 1-12 | Valid |
| EP8 | <1 | Invalid |
| EP9 | >12 | Invalid |

**Table 3: Equivalence Partitioning for Year**

| Partition ID | Range | Status |
| --- | --- | --- |
| EP10 | 1900-2015 | Valid |
| EP11 | <1900 | Invalid |
| EP12 | >2015 | Invalid |

**Equivalence Partitioning Test Cases:**

| Test Case ID | Day | Month | Year | Expected Output |
| --- | --- | --- | --- | --- |
| 1 | 1 | 6 | 2000 | 31-5-2000 |
| 2 | 2 | 6 | 2015 | 1-6-2015 |
| 3 | 2 | 6 | 2016 | Invalid |
| 4 | 1 | 1 | 1900 | 31-12-1899 |
| 5 | 31 | 12 | 1899 | Invalid |
| 6 | 31 | 12 | 1900 | 30-12-1900 |
| 7 | 29 | 2 | 2012 | 28-2-2012 |

************************************Corner Test cases:************************************

| Test Case ID | Day | Month | Year | Expected Output |
| --- | --- | --- | --- | --- |
| 1 | 1 | 1 | 1900 | 31-12-1899 |
| 2 | 31 | 12 | 2015 | 30-12-2015 |
| 3 | 1 | 1 | 1899 | Invalid |
| 4 | 31 | 12 | 2016 | Invalid |
| 5 | 29 | 2 | 2000 | 28-2-2000 |
| 6 | 1 | 3 | 2000 | 29-2-2000 |
| 7 | 29 | 2 | 1900 | Invalid |
| 8 | 1 | 3 | 1900 | 28-2-1900 |
<img width="780" alt="image" src="https://user-images.githubusercontent.com/82770981/232835123-23f970f3-d647-49b1-afcd-8803525cdb0b.png">

Equivalence Partitioning : EP

Boundary Value Analysis : BVA

### **P1. The function linearSearch searches for a value v in an array of integers a. If v appears in the array a, then the function returns the first index i, such that a[i] == v; otherwise, -1 is returned.**

```java
int linearSearch(int v, int a[], int n) {
    int i = 0;
    while (i < n) {
        if (a[i] == v)
            return i;
        i++;
    }
    return -1;
}
```

Equivalence Partitioning(EP) and Boundary Value Analysis(BVA).

| Test Type | Tester Action and Input Data | Expected Outcome |
| --- | --- | --- |
| EP | Test with v as a non-existent value and an empty array a[] | -1 |
| EP | Test with v as a non-existent value and a non-empty array a[] | -1 |
| EP | Test with v as an existent value and an empty array a[] | -1 |
| EP | Test with v as an existent value and a non-empty array a[] where v exists | Index of v in a[] |
| EP | Test with v as an existent value and a non-empty array a[] where v does not exist | -1 |
| BVA | Test with v as a non-existent value and an empty array a[] | -1 |
| BVA | Test with v as a non-existent value and a non-empty array a[] | -1 |
| BVA | Test with v as an existent value and an array a[] of length 0 | -1 |
| BVA | Test with v as an existent value and an array a[] of length 1, where v exists | 0 |
| BVA | Test with v as an existent value and an array a[] of length 1, where v does not exist |  |

| Test Type | Array | Value | Expected Result |
| --- | --- | --- | --- |
| EP | [1,2,3,4] | 4 | 3 |
| EP | [1,2,3] | 4 | -1 |
| BVA | [] | 2 | -1 |
| EP | [5,6,7] | 5 | 0 |
| EP | [8,9] | 9 | 1 |
| BVA | [10] | 10 | 0 |
| BVA | [11] | 12 | -1 |
| EP | [13,14] | 15 | -1 |

<img width="780" alt="image" src="https://user-images.githubusercontent.com/82770981/232836228-de685a62-eb40-444e-9ad4-8809bb15f15b.png">

### **P2. The function countItem returns the number of times a value v appears in an array of integers**

```cpp
int countItem(int v, int a[])
{
    int count = 0;
    for (int i = 0; i < a.length; i++)
    {
        if (a[i] == v)
        count++;
    }
    return (count);
}
```

| Test Type | Tester Action and Input Data | Expected Outcome |
| --- | --- | --- |
| EP | Test with v as a non-existent value and an empty array a[] | 0 |
| EP | Test with v as a non-existent value and a non-empty array a[] | 0 |
| EP | Test with v as an existent value and an empty array a[] | 0 |
| EP | Test with v as an existent value and a non-empty array a[] where v exists | Count of v in a[] |
| EP | Test with v as an existent value and a non-empty array a[] where v does not exist | 0 |
| BVA | Test with v as a non-existent value and an empty array a[] | 0 |
| BVA | Test with v as a non-existent value and a non-empty array a[] | 0 |
| BVA | Test with v as an existent value and an array a[] of length 0 | 0 |
| BVA | Test with v as an existent value and an array a[] of length 1, where v exists | 1 |
| BVA | Test with v as an existent value and an array a[] of length 1, where v does not exist |  |

| Test Type | Array | Value | Expected Result |
| --- | --- | --- | --- |
| EP | [1,2,3,4] | 4 | 1 |
| EP | [1,2,3] | 4 | 0 |
| BVA | [] | 2 | 0 |
| EP | [5,6,7] | 5 | 1 |
| EP | [8,9] | 9 | 1 |
| BVA | [10] | 10 | 1 |
| BVA | [11] | 12 | 0 |
| EP | [13,14] | 15 | 0 |
| EP | [1,1,2,2] | 1 | 2 |
| BVA | [3,3,3] | 3 | 3 |

<img width="768" alt="image" src="https://user-images.githubusercontent.com/82770981/232836741-83979f94-6f85-42f0-9b32-462f3141c1ca.png">


### **P3. The function binarySearch searches for a value v in an ordered array of integers a. If v appears in the array a, then the function returns an index i, such that a[i] == v; otherwise, -1 is returned.**

```cpp
int binarySearch(int v, int a[])
{
    int lo,mid,hi;
    lo = 0;
    hi = a.length-1;
    while (lo <= hi)
    {
        mid = (lo+hi)/2;
        if (v == a[mid])
            return (mid);
        else if (v < a[mid])
            hi = mid-1;
        else
            lo = mid+1;
    }
    return(-1);
}
```

| Test Type | Tester Action and Input Data | Expected Outcome |
| --- | --- | --- |
| EP | Test with v as a non-existent value and an empty array a[] | -1 |
| EP | Test with v as a non-existent value and a non-empty sorted array a[] | -1 |
| EP | Test with v as an existent value and an empty array a[] | -1 |
| EP | Test with v as an existent value and a non-empty sorted array a[] where v exists | Index of v in a[] |
| EP | Test with v as an existent value and a non-empty sorted array a[] where v does not exist | -1 |
| BVA | Test with v as a non-existent value and an empty array a[] | -1 |

| Test Type | Array | Value | Expected Result |
| --- | --- | --- | --- |
| EP | [1,2,3,4] | 4 | 3 |
| EP | [1,2,3] | 4 | -1 |
| BVA | [] | 2 | -1 |
| EP | [5,6,7] | 5 | 0 |
| EP | [8,9] | 9 | 1 |
| BVA | [10] | 10 | 0 |
| BVA | [11] | 12 | -1 |
| EP | [13,14] | 15 | -1 |
<img width="759" alt="image" src="https://user-images.githubusercontent.com/82770981/232836631-d58d90a8-411f-4875-913c-452606950e22.png">


### **P4. The following problem has been adapted from The Art of Software Testing, by G. Myers (1979). The function triangle takes three integer parameters that are interpreted as the lengths of the sides of a triangle. It returns whether the triangle is equilateral (three lengths equal), isosceles (two lengths equal), scalene (no lengths equal), or invalid (impossible lengths).**

```cpp
#define EQUILATERAL 0
#define ISOSCELES 1
#define SCALENE 2
#define INVALID 3

int triangle(int a, int b, int c) {
    if (a <= 0 || b <= 0 || c <= 0)
        return INVALID;
    if (a >= b + c || b >= a + c || c >= a + b)
        return INVALID;
    if (a == b && b == c)
        return EQUILATERAL;
    if (a == b || a == c || b == c)
        return ISOSCELES;
    return SCALENE;
}
```

| Test Type | Tester Action and Input Data | Expected Outcome |
| --- | --- | --- |
| EP | Test with a, b, and c as the sides of an equilateral triangle | EQUILATERAL |
| EP | Test with a, b, and c as the sides of an isosceles triangle | ISOSCELES |
| EP | Test with a, b, and c as the sides of a scalene triangle | SCALENE |
| EP | Test with a, b, and c as the sides of an invalid triangle | INVALID |
| BVA | Test with a = 0, b = 1, c = 1 | INVALID |
| BVA | Test with a = -1, b = 1, c = 1 | INVALID |

| Test Type | Input (a,b,c) | Expected Output |
| --- | --- | --- |
| EP | (3,3,3) | EQUILATERAL |
| EP | (3,4,5) | SCALENE |
| EP | (3,3,5) | ISOSCELES |
| EP | (0,3,5) | INVALID |
| BVA | (1,1,2) | INVALID |
| BVA | (1,1,1) | EQUILATERAL |
| BVA | (1,2,2) | ISOSCELES |
| BVA | (2,2,3) | ISOSCELES |
<img width="773" alt="image" src="https://user-images.githubusercontent.com/82770981/232837187-b6e85cd3-f6cd-478c-a4a9-58849529ae1b.png">


### **P5. The function prefix (String s1, String s2) returns whether or not the string s1 is a prefix of string s2 (you may assume that neither s1 nor s2 is null).**

```cpp
public static boolean prefix(String s1, String s2) {
    if (s1.length() > s2.length()) {
        return false;
    }
    for (int i = 0; i < s1.length(); i++) {
        if (s1.charAt(i) != s2.charAt(i)) {
            return false;
        }
    }
    return true;
}
```

| Test Type | Tester Action and Input Data | Expected Outcome |
| --- | --- | --- |
| EP | Test with s1 as a prefix of s2 | true |
| EP | Test with s1 not a prefix of s2 | false |
| EP | Test with s1 longer than s2 | false |
| BVA | Test with s1 as an empty string | true |
| BVA | Test with s1 as a one character prefix of s2 | true |
| BVA | Test with s1 as a one character non-prefix of s2 | false |

| Test Type | Input (s1,s2) | Expected Output |
| --- | --- | --- |
| EP | (“pre”, “prefix”) | true |
| EP | (“pre”, “postfix”) | false |
| EP | (“prefix”, “pre”) | false |
| BVA | (“”, “prefix”) | true |
| BVA | (“p”, “prefix”) | true |
| BVA | (“pr”, “prefix”) | true |
| BVA | (“p”, “postfix”) | false |
<img width="767" alt="image" src="https://user-images.githubusercontent.com/82770981/232836911-50629f45-27c4-4519-9722-9ebd6ce4a1b4.png">

### **P6: Consider again the triangle classification program (P4) with a slightly different specification: The program reads floating values from the standard input. The three values A, B, and C are interpreted as representing the lengths of the sides of a triangle. The program then prints a message to the standard output that states whether the triangle, if it can be formed, is scalene, isosceles, equilateral, or right angled. 
Determine the following for the above program:**

**a) Identify the equivalence classes for the system**

The equivalence classes for the system are:

- Equilateral triangle: A = B = C
- Isosceles triangle: A = B ≠ C or A = C ≠ B or B = C ≠ A
- Scalene triangle: A ≠ B ≠ C
- Right angled triangle: $A^2 + B^2 = C^2 or A^2 + C^2 = B^2 or B^2 + C^2 = A^2$
- Non-triangle: $A + B ≤ C or A + C ≤ B or B + C ≤ A$
- Non-positive input: $A ≤ 0  or  B ≤ 0  or  C ≤ 0$

**b) Identify test cases to cover the identified equivalence classes. Also, explicitly mention which test case would cover which equivalence class.**

Test cases to cover the identified equivalence classes:

- Equilateral triangle: (3.0, 3.0, 3.0)
- Isosceles triangle: (3.0, 3.0, 4.0)
- Scalene triangle: (3.0, 4.0, 5.0)
- Right angled triangle: (3.0, 4.0, 5.0)
- Non-triangle: (1.0, 2.0, 4.0)
- Non-positive input: (-1.0, 2.0, 3.0)

**c) For the boundary condition A + B > C case (scalene triangle), identify test cases to verify the boundary.**

Test cases to verify the boundary for the scalene triangle (A + B > C):

- (3.1, 4.1, 7.1)
- (3.1, 4.1, 7.2)

**d) For the boundary condition A = C case (isosceles triangle), identify test cases to verify the boundary.**

 Test cases to verify the boundary for the isosceles triangle (A = C):

- (3.1, 4.1, 3.1)
- (3.1, 4.2, 3.1)

**e)  For the boundary condition A = B = C case (equilateral triangle), identify test cases to verify the boundary.**

Test cases to verify the boundary for the equilateral triangle (A = B = C):

- (3.1, 3.1, 3.1)
- (3.2, 3.2, 3.2)

**f) For the boundary condition A^2 + B^2 = C^2 case (right-angle triangle), identify test cases to the boundary.** 

Test cases to verify the boundary for the right angled triangle $(A^2 + B^2 = C^2):$

- (3.0, 4.0, 5.0)
- (5.0, 12.0, 13.0)

**g) For the non-triangle case, identify test cases to explore the boundary.**

Test cases to explore the boundary for the non-triangle case:

- (1.1, 2.1, 4.1)
- (1.1, 2.1, 3.2)

**h) For non-positive input, identify test points.**

- (A=0, B=1, C=2)
- (A=-1, B=2, C=3)
- (A=1, B=-2, C=3)
- (A=1, B=2, C=-3)

## **Section B**

**The code below is part of a method in the ConvexHull class in the VMAP system. The following is a small fragment of a method in the ConvexHull class. For the purposes of this exercise you do not need to know the intended function of the method. The parameter p is a Vector of Point objects, p.size() is the size of the vector p, (p.get(i)).x is the x component of the ith point appearing in p, similarly for (p.get(i)).y. This exercise is concerned with structural testing of code and so the focus is on creating test sets that satisfy some particular coverage criterion.**

<img width="639" alt="Untitled" src="https://user-images.githubusercontent.com/82770981/232833976-e846513e-a4df-441f-9f0d-6f2989f6908d.png">

### 1. Convert the Java code comprising the beginning of the doGraham method into a control flow graph (CFG)
#### Control Flow Graph

![Untitled Diagram drawio (1)](https://user-images.githubusercontent.com/82770981/232841181-56a5bf6e-0d75-4bc7-adac-f754f6f55710.png)

### 2. Construct test sets for your flow graph that are adequate for the following criteria:
##### a. Statement Coverage.
##### b. Branch Coverage.
##### c. Basic Condition Coverage.

```
1.  int i, j, min, M;
2.  Point t;
3.  min = 0;
4.  for(i=1; i < p.size(); ++i) {
5.      if (p.get(i).y < p.get(min).y) {
6.          min = i;
7.      }
8.  }
9.  for (i=0; i < p.size(); ++i) {
10.     if ((p.get(i).y == p.get(min).y) && (p.get(i).x < p.get(min).x)) {
11.         min = i;
12.     }
13. }
```

| Test Case | p | Statements Covered | Branches Covered | Basic Conditions Covered |
| --- | --- | --- | --- | --- |
| 1 | [(2,2), (2,3), (1,3), (1,4)] | {1,2,3,4,5,7,8} | {5F,8F} | {5F,8F} |
| 2 | [(2,3), (3,4), (1,2), (5,6)] | {1,2,3,4,5,6,7} | {5F} | {5F} |
| 3 | [(1,5), (2,7), (3,5), (4,5), (5,6)] | {1,2,3,4,5-13} | {5T,F} | {5T,F} |
| 4 | [(1,2)] | {1-8} | {5F} | {5F} |
| 5 | [] | {1-3} | {} | {} |
| 6 | [(1,2), (2,3), (3,4)] | {1-8} | {5F} | {5F} |
| 7 | [(3,4), (2,3), (1,2)] | {1-13} | {5T,F} | {5T,F} |
| 8 | [(1,2), (2,3), (3,4), (4,5)] | {1-8} | {5F} | {5F} |
| 9 | [(4,5), (3,4), (2,3), (1,2)] | {1-13} | {5T,F} | {5T,F} |
| 10 | [(1,2), (2,3), (3,4), (4,5), (5,6)] | {1-8} | {5F} | {5F} |

In this table:

- “p” refers to the input vector for the **`doGraham`** method.
- “Statements Covered” refers to the statements in the code fragment that are executed by the test case.
- “Branches Covered” refers to the branches in the control flow graph that are executed by the test case. The outcome of each branch is shown in parentheses.
- “Basic Conditions Covered” refers to the conditions in the code fragment that are evaluated by the test case. The outcome of each condition is shown in parentheses.


##### Testing 
<img width="767" alt="image" src="https://user-images.githubusercontent.com/82770981/232846905-d34903a0-7b0d-4050-a495-9882fd5df697.png">
<img width="772" alt="image" src="https://user-images.githubusercontent.com/82770981/232846680-19aa44ed-409a-48df-8b49-3137ea4e2d7a.png">


