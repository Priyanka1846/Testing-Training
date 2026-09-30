# HCL Automation Testing Training

## 17 September 2026

### Test Case Documentation

Created and documented test cases based on application requirements using a structured test case format.

#### Concepts Covered

- Test Case ID
- Test Case Description
- Preconditions
- Test Steps
- Test Data
- Expected Result
- Actual Result
- Test Status

**Task:** [Test Case Documentation](https://docs.google.com/spreadsheets/d/1RXd-QSDysk9iYf62sDZA2-BzGseUhxkbaIV3ppgLlEo/edit?gid=0#gid=0)

---

## 18 September 2026

### Test Case Using Jira

Created and managed test cases using Jira as part of the software testing workflow.

#### Concepts Covered

- Jira Issues
- Test Case Tracking
- Issue Identification
- Test Execution
- Status Tracking
- Defect Management

**Task:** [Jira Issue T1-22](https://priyankasworkspace-34516593.atlassian.net/browse/T1-22)

---

## 22 September 2026

### Equivalence Partition Test Case Exercises

Practiced designing test cases using the Equivalence Partitioning test design technique.

Equivalence Partitioning divides input data into different groups, or equivalence classes, where the system is expected to behave similarly for values within the same class.

#### Example

For an input field that accepts values from 1 to 100:

| Partition | Range | Classification |
|---|---|---|
| Partition 1 | Less than 1 | Invalid |
| Partition 2 | 1–100 | Valid |
| Partition 3 | Greater than 100 | Invalid |

**Task:** [Equivalence Partition Exercises](https://docs.google.com/spreadsheets/d/16cv3-dBqDuVq0QTk5Pfz7ul7JH2lY7xcsgbYGzAl4gM/edit?gid=0#gid=0)

---

## 23 September 2026

### Python Code Implementation

Implemented Python programs as part of the programming and automation testing training.

#### 1. Binary Numbers Divisible by 5

**Problem**

Write a Python program that accepts a sequence of comma-separated 4-digit binary numbers and checks whether they are divisible by 5. The numbers divisible by 5 should be printed.

**Example Input**

```text
0100,0011,1010,1001
```

**Expected Output**

```text
1010
```

**Implementation**

```python
num = input().split()

for i in num:
    if int(i, 2) % 5 == 0:
        print(i)
```
---

#### 2. Count Letters and Digits

**Problem**

Write a Python program that accepts a sentence and calculates the number of letters and digits.

**Example Input**

```text
hello world! 123
```

**Expected Output**

```text
LETTERS 10
DIGITS 3
```

**Implementation**

```python
sentence = input()

letters = 0
digit = 0

for i in sentence:
    if i.isalpha():
        letters += 1
    elif i.isdigit():
        digit += 1

print("LETTER: ", letters)
print("DIGIT: ", digit)
```
---

#### 3. Factorial of a Number

**Problem**

Write a Python program to calculate the factorial of a given number.

**Example Input**

```text
8
```

**Expected Output**

```text
40320
```

**Implementation**

```python
n = int(input())

fact = 1

for i in range(1, n + 1):
    fact *= i

print(fact)
```
---
## 24 September 2026

### Test Metrix

Created and documented the test matrix with requirements and test cases.

#### Metrics Covered
- Test Coverage
- Test Execution Percentage
- Pass Rate
- Fail Rate
- Total Defects
- Critical Defect Percentage
- Defect Distribution
- Mean Response Time
- Median Response Time

**Task:** [Test Metrics](https://docs.google.com/spreadsheets/d/1kFllSGDlt9accJvxfsRuHqLC3M2HJn2ZAn0iDP76MyY/edit?gid=0#gid=0)

---

## 25 September 2026

### Python Code Implementation

## 1. Student Attendance Analysis

A college maintains the daily attendance details of its students in the form of a list containing student IDs. Some students may have attended multiple sessions on the same day. The administration wants to identify the longest continuous sequence of sessions in which no student ID is repeated. Develop a solution that determines the maximum length of such a sequence.

### Implementation

```python
l1 = input().split(",")

longest = 0

for i in range(len(l1)):
    arr = []

    for j in range(i, len(l1)):
        if l1[j] in arr:
            break

        arr.append(l1[j])

    if len(arr) > longest:
        longest = len(arr)

print(longest)
```

---

## 2. Online Shopping Price Analysis

An online shopping application stores the prices of products viewed by a customer during a browsing session. The customer wants to identify a continuous range of products that provides the maximum possible total discount value. Given the discount values, determine the maximum value that can be obtained from any continuous range.

### Implementation

```python
arr = list(map(int, input().split()))

curr = arr[0]
maxSum = arr[0]

for i in range(1, len(arr)):
    curr = max(arr[i], curr + arr[i])
    maxSum = max(maxSum, curr)

print(maxSum)
```

---

## 3. Rainwater Collection System

A city installs buildings of different heights along a straight road. During rainfall, water gets collected between taller buildings. The engineering team needs to calculate the total amount of water that can remain trapped after heavy rainfall based on the heights of the buildings.

### Implementation

```python
arr = list(map(int, input().split()))

water = 0

for i in range(len(arr)):
    left = max(arr[:i+1])
    right = max(arr[i:])

    level = min(left, right)

    if level >= arr[i]:
        water += level - arr[i]

print(water)
```

---

## 4. Employee Performance Analysis

A company stores the monthly performance scores of an employee for several months. The scores may contain both positive and negative values depending on the employee's performance. Management wants to identify the continuous period during which the employee achieved the highest overall performance.

### Implementation

```python
arr = list(map(int, input().split()))

curr = arr[0]
maxSum = arr[0]

for i in range(1, len(arr)):
    curr = max(arr[i], curr + arr[i])
    maxSum = max(maxSum, curr)

print(maxSum)
```

---

## 5. Product Sales Analysis

A retail company stores the daily sales quantity of a product for several consecutive days. Due to seasonal changes, some days may have negative adjustments. The company wants to identify the period that produced the highest multiplication of sales-related values. Develop a solution to determine this maximum product.

### Implementation

```python
arr = list(map(int, input().split()))

maximum = arr[0]
minimum = arr[0]
answer = arr[0]

for i in range(1, len(arr)):
    x = arr[i]

    if x < 0:
        maximum, minimum = minimum, maximum

    maximum = max(x, maximum * x)
    minimum = min(x, minimum * x)

    answer = max(answer, maximum)

print(answer)
```

---

## 6. Customer Purchase History

An e-commerce application stores the product IDs purchased by a customer in chronological order. The same product may appear multiple times. The system needs to determine the longest sequence of consecutive purchases in which every product ID is unique.

### Implementation

```python
l1 = input().split(",")

longest = 0

for i in range(len(l1)):
    arr = []

    for j in range(i, len(l1)):
        if l1[j] in arr:
            break

        arr.append(l1[j])

    if len(arr) > longest:
        longest = len(arr)

print(longest)
```

---

## 7. Bank Transaction Analysis

A bank stores transaction amounts for a customer's account. A continuous group of transactions may add up to a specific target amount. The auditing system needs to determine how many different continuous transaction groups produce exactly the specified amount.

### Implementation

```python
arr = list(map(int, input().split()))

target = int(input())

count = 0

for i in range(len(arr)):
    total = 0

    for j in range(i, len(arr)):
        total += arr[j]

        if total == target:
            count += 1

print(count)
```

---

## 8. Employee Skill Grouping

A company receives a list of employee skill codes represented as strings. Employees having the same set of characters in their skill codes belong to the same skill category, even if the characters appear in a different order. The HR system needs to organize employees into appropriate skill groups.

### Implementation

```python
arr = input().split()

groups = {}

for word in arr:
    key = ''.join(sorted(word))

    if key not in groups:
        groups[key] = []

    groups[key].append(word)

for group in groups.values():
    print(group)
```

---

## 9. Network Packet Analysis

A network monitoring system receives packet identifiers in chronological order. The system must determine the longest sequence of consecutive packets whose identifiers form a continuous numerical sequence, regardless of their original order in the incoming data.

### Implementation

```python
arr = list(map(int, input().split()))

nums = set(arr)

longest = 0

for x in nums:

    if x - 1 not in nums:

        current = x
        length = 1

        while current + 1 in nums:
            current += 1
            length += 1

        longest = max(longest, length)

print(longest)
```

---

## 10. Hospital Appointment Scheduling

A hospital receives appointment requests represented by starting and ending times. Some appointments overlap with each other. The scheduling system needs to combine overlapping appointment periods so that the final schedule contains only non-overlapping time ranges.

### Implementation

```python
n = int(input())

arr = []

for i in range(n):
    start, end = map(int, input().split())
    arr.append([start, end])

arr.sort()

result = [arr[0]]

for i in range(1, n):
    start = arr[i][0]
    end = arr[i][1]

    if start <= result[-1][1]:
        result[-1][1] = max(result[-1][1], end)

    else:
        result.append([start, end])

for x in result:
    print(x[0], x[1])
```
---

## 29 September 2026

### Python Code Implementation

#### 1. NumPy-based assignment

```python
scores = np.array([78, 65, 89, 56, 92])

print("Q1 - Student Marks Array")
print("Array:", scores)
print("Dimensions:", scores.ndim)
print("Shape:", scores.shape)
print("Number of elements:", scores.size)
print("Data type:", scores.dtype)
```


#### 2. Calculate area of a circle

```python
student_scores = np.array([72, 85, 64, 90, 76])

print("\nQ2 - Student Marks Access")

for number, score in enumerate(student_scores, start=1):
    print(f"Student {number}: {score}")

print("Students 2 to 4:", student_scores[1:4])
```


#### 3. Count character frequency in a string

```python
all_marks = np.array([
    78, 85, 90,
    65, 72, 80,
    88, 91, 84,
    56, 62, 70,
    95, 89, 92
])

marks_table = all_marks.reshape(5, 3)

print("\nQ3 - Subject-wise Marks")
print(marks_table)
```


#### 4. Calculate factorial

```python
internal_marks = np.array([25, 38, 42, 30, 41])
external_marks = np.array([45, 30, 40, 45, 44])

combined_marks = internal_marks + external_marks

print("\nQ4 - Final Marks")
print("Final marks:", combined_marks)
```

#### 5. Generate Fibonacci series

```python
test_scores = np.array([45, 78, 56, 32, 91])
student_numbers = np.arange(1, len(test_scores) + 1)

passed = test_scores >= 50

print("\nQ5 - Students Scoring 50 or Above")
print("Marks:", test_scores[passed])
print("Student numbers:", student_numbers[passed])
```


#### 6. Merge two dictionaries

```python
marks_matrix = np.array([
    [78, 85, 90],
    [65, 72, 80],
    [88, 91, 84],
    [56, 62, 70],
    [95, 89, 92]
])

student_averages = np.mean(marks_matrix, axis=1)

print("\nQ6 - Average Marks")
for i, average in enumerate(student_averages, start=1):
    print(f"Student {i} average: {average:.2f}")
```

#### 7. Check prime numbers

```python
class_marks = np.array([67, 82, 91, 74, 58])

print("\nQ7 - Class Performance Statistics")
print("Total:", np.sum(class_marks))
print("Average:", np.mean(class_marks))
print("Highest:", np.max(class_marks))
print("Lowest:", np.min(class_marks))
print("Standard deviation:", np.std(class_marks))
```

#### 8. Reverse a string

```python
subject_totals = np.sum(marks_matrix, axis=0)

print("\nQ8 - Subject-wise Performance")
print("Total marks in each subject:", subject_totals)
```

#### 9. Remove duplicate elements from a list

```python
individual_totals = np.sum(marks_matrix, axis=1)

print("\nQ9 - Student-wise Performance")
for i, total in enumerate(individual_totals, start=1):
    print(f"Student {i} total: {total}")
```

#### 10. Find the second-largest element

```python
total_scores = np.array([245, 278, 219, 290, 256])

ordered_scores = np.sort(total_scores)[::-1]

print("\nQ10 - Student Ranking")
for position, score in enumerate(ordered_scores, start=1):
    print(f"Rank {position}: {score}")
```

#### 11. Calculate square using lambda

```python
duplicate_scores = np.array([85, 92, 85, 76, 92])

different_scores = np.unique(duplicate_scores)

print("\nQ11 - Unique Marks")
print("Unique marks:", different_scores)
```

#### 12. Display employee information using functions

```python
scores_with_missing = np.array([78, 85, np.nan, 92, 67])

valid_average = np.nanmean(scores_with_missing)

print("\nQ12 - Average Without Missing Value")
print("Average marks:", valid_average)
```

#### 13. Perform mathematical operations using functions

```python
grade_marks = np.array([95, 82, 74, 61, 45])

grades = np.select(
    [
        grade_marks >= 90,
        grade_marks >= 80,
        grade_marks >= 70,
        grade_marks >= 60
    ],
    [
        "A",
        "B",
        "C",
        "D"
    ],
    default="F"
)

print("\nQ13 - Grade Classification")
print("Marks:", grade_marks)
print("Grades:", grades)
```

#### 14. Remove duplicates using a function

```python
random_scores = np.random.randint(0, 101, size=5)

print("\nQ14 - Random Marks")
print("Generated marks:", random_scores)
print("Total:", np.sum(random_scores))
print("Average:", np.mean(random_scores))
print("Highest:", np.max(random_scores))
print("Lowest:", np.min(random_scores))
print("Standard deviation:", np.std(random_scores))
```

#### 15. Sort tuple elements using a function

```python
performance_data = np.array([
    [78, 85, 90],
    [65, 72, 80],
    [88, 91, 84],
    [56, 62, 70],
    [95, 89, 92]
])

totals = np.sum(performance_data, axis=1)
averages = np.mean(performance_data, axis=1)
highest_scores = np.max(performance_data, axis=1)
lowest_scores = np.min(performance_data, axis=1)

class_average = np.mean(averages)
above_average = averages > class_average

print("\nQ15 - Student Performance Analysis")

for i in range(len(performance_data)):
    print(
        f"Student {i + 1}: "
        f"Total = {totals[i]}, "
        f"Average = {averages[i]:.2f}, "
        f"Highest = {highest_scores[i]}, "
        f"Lowest = {lowest_scores[i]}"
    )

print("Class average:", round(class_average, 2))
print("Students above class average:",
      np.where(above_average)[0] + 1)
```
