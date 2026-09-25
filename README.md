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
