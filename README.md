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

#### 1. NumPy-based Assignment

```python
import numpy as np

scores = np.array([78, 65, 89, 56, 92])

print("Q1 - Student Marks Array")
print("Array:", scores)
print("Dimensions:", scores.ndim)
print("Shape:", scores.shape)
print("Number of elements:", scores.size)
print("Data type:", scores.dtype)
```

#### 2. Calculate Area of a Circle

```python
import math

radius = float(input())

area = math.pi * radius * radius

print("Area of circle:", round(area, 2))
```

#### 3. Count Character Frequency in a String

```python
text = input()

frequency = {}

for char in text:
    if char != " ":
        frequency[char] = frequency.get(char, 0) + 1

print("Character frequency:")

for char, count in frequency.items():
    print(char, ":", count)
```

#### 4. Calculate Factorial

```python
number = int(input())

factorial = 1

for value in range(2, number + 1):
    factorial *= value

print("Factorial:", factorial)
```

#### 5. Generate Fibonacci Series

```python
num = int(input())

first, second = 0, 1
series = []

for _ in range(num):
    series.append(first)
    first, second = second, first + second

print("Fibonacci series:", series)
```

#### 6. Merge Two Dictionaries

```python
dict_one = {
    "name": "Priyanka",
    "age": 20
}

dict_two = {
    "course": "AI & DS",
    "year": 3
}

merged = {**dict_one, **dict_two}

print("Merged dictionary:", merged)
```

#### 7. Check Prime Numbers

```python
n = int(input())

if n < 2:
    is_prime = False
else:
    is_prime = True

    for divisor in range(2, int(n ** 0.5) + 1):
        if n % divisor == 0:
            is_prime = False
            break

if is_prime:
    print(n, "is a prime number")
else:
    print(n, "is not a prime number")
```

#### 8. Reverse a String

```python
text = input()

reversed_text = text[::-1]

print("Reversed string:", reversed_text)
```

#### 9. Remove Duplicate Elements from a List

```python
numbers = [10, 20, 10, 30, 20, 40, 30]

unique_values = list(dict.fromkeys(numbers))

print("Original list:", numbers)
print("After removing duplicates:", unique_values)
```

#### 10. Find the Second-Largest Element

```python
numbers = [45, 12, 78, 34, 90, 56]

distinct_numbers = sorted(set(numbers), reverse=True)

if len(distinct_numbers) >= 2:
    print("Second-largest element:", distinct_numbers[1])
else:
    print("Second-largest element does not exist")
```

#### 11. Calculate Square Using Lambda

```python
number = float(input())

square = lambda x: x * x

print("Square:", square(number))
```

#### 12. Display Employee Information Using Functions

```python
def show_employee(name, employee_id, department):
    print("Employee Name:", name)
    print("Employee ID:", employee_id)
    print("Department:", department)


show_employee(
    "Priyanka",
    "EMP101",
    "Automation Testing"
)
```

#### 13. Perform Mathematical Operations Using Functions

```python
def addition(a, b):
    return a + b


def subtraction(a, b):
    return a - b


def multiplication(a, b):
    return a * b


def division(a, b):
    if b == 0:
        return "Division by zero is not possible"
    return a / b


x = float(input())
y = float(input())

print("Addition:", addition(x, y))
print("Subtraction:", subtraction(x, y))
print("Multiplication:", multiplication(x, y))
print("Division:", division(x, y))
```

#### 14. Remove Duplicates Using a Function

```python
def remove_duplicates(items):
    result = []

    for item in items:
        if item not in result:
            result.append(item)

    return result


data = [5, 8, 5, 2, 8, 9, 2, 10]

print("Original data:", data)
print("Unique data:", remove_duplicates(data))
```

#### 15. Sort Tuple Elements Using a Function

```python
def sort_tuple(values):
    return tuple(sorted(values))


data = (45, 12, 78, 23, 9, 56)

print("Original tuple:", data)
print("Sorted tuple:", sort_tuple(data))
```

### Task Link : https://colab.research.google.com/drive/1sJAqmzjsZ4H8vlmJKtSrZD4V_94SqlBd#scrollTo=hLvtyjwqdykZ
---
## 05 October 2026
### Selenium Practice

### 1. SauceDemo Login Automation

```python
from selenium import webdriver
from selenium.webdriver.common.by import By

driver = webdriver.Chrome()

driver.get("https://www.saucedemo.com/")

username = driver.find_element(By.ID, "user-name")
password = driver.find_element(By.NAME, "password")
login = driver.find_element(By.ID, "login-button")

username.send_keys("standard_user")
password.send_keys("secret_sauce")

print(username.get_attribute("placeholder"))
print(login.is_enabled())
print(username.is_displayed())

login.click()

driver.quit()
```

---

### 2. Google Search Automation

```python
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.common.keys import Keys
import time

driver = webdriver.Chrome()

driver.get("https://www.google.com/")

search = driver.find_element(By.NAME, "q")

search.send_keys("Actor Vijay Deverakonda")

print(search.get_attribute("value"))

search.send_keys(Keys.ENTER)

time.sleep(3)

driver.get("https://www.google.com/search?sca_esv=a2875db628506375&rlz=1C1YTUH_en-GBIN1186IN1186&sxsrf=APpeQntHcHn-8xyZ42s969XnPjuHh18nmw:1791179420776&udm=2&fbs=ABfTbFVyMZGZf1hfvX9uKjN_-G8c4u0nXx4bEIpwm1lnNH832QGGMdFXpDyzkQgEdtB8w9zZ67Faapx8wIWp8O3JpX8ZbooJTg6IC0i9eLmD380spMllksdFpgm79ImriDjfCnTBYJEsBPGPiZmxyursypEsGL2FRhZVp5hPiM06simLt3pas0OhU38U7j6-7ppr8W_hIPQMf58dcF_rZDpJ3v86825oJA&q=vijay+deverakonda&sa=X&ved=2ahUKEwjSuOqol6KXAxVOjOEIHVLmM80QtKgLegQIFRAB&biw=1707&bih=825&dpr=1.13#sv=CAMSUxoyKhBlF5eTE0TzVsZWZkZ1hNMg5ReXkxNE81bGVmZGdYTToORThhOGRFUU9fS3dXRU0gBCoXCgFzEhBlLVF5eTE0TzVsZWZkZ1hNGAEwAVACGAcgj_vkogdKCBACGAEgAigB")

time.sleep(5)
```

---

### 3. SauceDemo Product List

```python
from selenium import webdriver
from selenium.webdriver.common.by import By

driver = webdriver.Chrome()

driver.get("https://www.saucedemo.com/")

username = driver.find_element(By.ID, "user-name")
password = driver.find_element(By.ID, "password")
login = driver.find_element(By.ID, "login-button")

username.send_keys("standard_user")
password.send_keys("secret_sauce")

login.click()

products = driver.find_elements(By.CLASS_NAME, "inventory_item_name")

for product in products:
    print(product.text)

driver.quit()
```

---

### 4. Flipkart Login Automation

```python
from selenium import webdriver
from selenium.webdriver.common.by import By
import time

driver = webdriver.Chrome()
driver.maximize_window()

driver.get("https://www.flipkart.com/account/login")

time.sleep(3)

mobile = input("Enter your mobile number: ")

mobile_box = driver.find_element(
    By.XPATH,
    "//input[@type='text' or @type='tel' or @type='number']"
)

mobile_box.send_keys(mobile)

time.sleep(2)

continue_button = driver.find_element(
    By.XPATH,
    "//button[contains(., 'Continue')]"
)

continue_button.click()

time.sleep(5)

print("Continue clicked successfully.")

input("Press Enter to close the browser...")

driver.quit()
```
---
## 06 October 2026
### Selenium-Python Practice 

```python
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
from selenium.webdriver.support.ui import Select
import time

driver = webdriver.Chrome()
driver.get("https://vinothqaacademy.com/demo-site/")

wait = WebDriverWait(driver, 15)

first_name = wait.until(EC.presence_of_element_located((By.ID, "vfb-5")))
first_name.send_keys("Priyanka")

last_name = wait.until(EC.presence_of_element_located((By.ID, "vfb-7")))
last_name.send_keys("K")

wait.until(EC.element_to_be_clickable((By.ID, "vfb-31-2"))).click()

address = wait.until(EC.presence_of_element_located((By.ID, "vfb-13-address")))
address.send_keys("123 Main Street")

driver.find_element(By.ID, "vfb-13-address-2").send_keys("Apt 101")
driver.find_element(By.ID, "vfb-13-city").send_keys("Chennai")
driver.find_element(By.ID, "vfb-13-state").send_keys("Tamil Nadu")
driver.find_element(By.ID, "vfb-13-zip").send_keys("600001")

country = Select(driver.find_element(By.ID, "vfb-13-country"))
country.select_by_visible_text("India")
time.sleep(2)

driver.find_element(By.ID, "vfb-14").send_keys("priyanka.student@saveetha.ac.in")

time.sleep(10)
```

### Task -2 (Amazon: Add to Cart and Display Payment Details)

```python
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.common.keys import Keys
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
from getpass import getpass
import time

options = webdriver.ChromeOptions()
options.page_load_strategy = "eager"

driver = webdriver.Chrome(options=options)

wait = WebDriverWait(driver, 20)

driver.maximize_window()

driver.get("https://www.amazon.in/")

search = wait.until(
    EC.element_to_be_clickable(
        (By.ID, "twotabsearchtextbox")
    )
)

search.send_keys("Women watches")
search.send_keys(Keys.ENTER)

add_buttons = wait.until(
    EC.presence_of_all_elements_located(
        (By.CSS_SELECTOR, "input[name='submit.addToCart']")
    )
)

for button in add_buttons:
    if button.is_displayed():
        driver.execute_script(
            "arguments[0].click();",
            button
        )
        break

time.sleep(3)

print("Wireless mouse added to cart")

driver.get("https://www.amazon.in/gp/cart/view.html")

time.sleep(4)

print("Cart opened")

checkout = wait.until(
    EC.element_to_be_clickable(
        (By.NAME, "proceedToRetailCheckout")
    )
)

checkout.click()

time.sleep(5)

print("Checkout page opened")

mobile_number = input("Enter your Amazon mobile number: ")

mobile_box = wait.until(
    EC.element_to_be_clickable(
        (By.ID, "ap_email_login")
    )
)

mobile_box.clear()
mobile_box.send_keys(mobile_number)

print("Mobile number entered")

continue_button = wait.until(
    EC.element_to_be_clickable(
        (By.ID, "continue")
    )
)

continue_button.click()

time.sleep(4)

print("Password page opened")

password = getpass("Enter your Amazon password: ")

password_box = wait.until(
    EC.element_to_be_clickable(
        (By.NAME, "password")
    )
)

password_box.clear()
password_box.send_keys(password)

print("Password entered")

sign_in = wait.until(
    EC.element_to_be_clickable(
        (By.ID, "signInSubmit")
    )
)

sign_in.click()

time.sleep(5)

print("Sign in submitted")

security_code = input(
    "Enter the security code received from Amazon: "
)

otp_box = wait.until(
    EC.element_to_be_clickable(
        (By.ID, "input-box-otp")
    )
)

otp_box.clear()
otp_box.send_keys(security_code)

print("Security code entered")

submit_code = wait.until(
    EC.element_to_be_clickable(
        (By.ID, "cvf-submit-otp-button")
    )
)

submit_code.click()

time.sleep(7)

print("Security verification completed")

print("Reached checkout/payment page")

input("Press Enter to close the browser...")

driver.quit()
```

---
# 7th October 2026
### Sauce Demo Automation Task

```python
import time

from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.common.action_chains import ActionChains
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC

# TC01 - Open the online shopping website
# Selenium Concept: driver.get()

driver = webdriver.Chrome()
driver.maximize_window()
driver.get("https://www.saucedemo.com/")

print("TC01: Shopping website opened successfully")

time.sleep(3)

driver.quit()
```

```python
# TC02 - Customer clicks Delete/Remove Product
# Selenium Concept: Alert - accept()

driver = webdriver.Chrome()
driver.maximize_window()
driver.get("https://www.saucedemo.com/")

wait = WebDriverWait(driver, 10)

wait.until(EC.visibility_of_element_located((By.ID, "user-name"))).send_keys("standard_user")

driver.find_element(By.ID, "password").send_keys("secret_sauce")
driver.find_element(By.ID, "login-button").click()

wait.until(EC.element_to_be_clickable((By.ID, "add-to-cart-sauce-labs-backpack"))).click()

driver.find_element(By.CLASS_NAME, "shopping_cart_link").click()

time.sleep(2)
driver.find_element(By.ID, "remove-sauce-labs-backpack").click()

print("TC02: Product deletion confirmed")

time.sleep(3)

time.sleep(3)

driver.quit()
```

```python
# TC03 - Customer clicks Delete/Remove Product but chooses Cancel
# Selenium Concept: Alert - dismiss()

driver = webdriver.Chrome()
driver.maximize_window()

driver.get("https://www.saucedemo.com/")

wait = WebDriverWait(driver, 10)

wait.until(EC.visibility_of_element_located((By.ID, "user-name"))).send_keys("standard_user")

driver.find_element(By.ID, "password").send_keys("secret_sauce")
driver.find_element(By.ID, "login-button").click()

wait.until(EC.element_to_be_clickable((By.ID, "add-to-cart-sauce-labs-backpack"))).click()

driver.find_element(By.CLASS_NAME, "shopping_cart_link").click()

time.sleep(2)

print("Product remains in the cart")

time.sleep(3)

driver.quit()
```

```python
# TC04 - Customer enters information in a prompt popup
# Selenium Concept: Prompt - send_keys()

driver = webdriver.Chrome()
driver.maximize_window()

driver.get("https://www.saucedemo.com/")

wait = WebDriverWait(driver, 10)

wait.until(EC.visibility_of_element_located((By.ID, "user-name"))).send_keys("standard_user")

driver.find_element(By.ID, "password").send_keys("secret_sauce")
driver.find_element(By.ID, "login-button").click()

time.sleep(2)

print("Information submitted successfully")

time.sleep(3)

driver.quit()
```

```python
# TC05 - Customer moves mouse over Products/Category menu
# Selenium Concept: Mouse Hover

driver = webdriver.Chrome()
driver.maximize_window()

driver.get("https://www.saucedemo.com/")

wait = WebDriverWait(driver, 10)

wait.until(EC.visibility_of_element_located((By.ID, "user-name"))).send_keys("standard_user")

driver.find_element(By.ID, "password").send_keys("secret_sauce")
driver.find_element(By.ID, "login-button").click()

product = wait.until(EC.visibility_of_element_located((By.CLASS_NAME, "inventory_item")))

ActionChains(driver).move_to_element(product).perform()

print("TC05: Mouse hover performed successfully")

time.sleep(3)

driver.quit()
```

```python
# TC06 - Handle Alert Popup
# Selenium Concept: Alert - accept()

driver = webdriver.Chrome()
driver.maximize_window()

driver.get("https://www.selenium.dev/selenium/web/alerts.html")

wait = WebDriverWait(driver, 10)

driver.find_element(By.ID, "alert").click()

alert = wait.until(EC.alert_is_present())

print("TC06:", alert.text)

alert.accept()

print("TC06: Alert accepted successfully")

time.sleep(3)

driver.quit()
```

```python
# TC07 - Customer drags a product/item into shopping cart area
# Selenium Concept: Drag & Drop

driver = webdriver.Chrome()
driver.maximize_window()

driver.get("https://www.saucedemo.com/")

wait = WebDriverWait(driver, 10)

wait.until(EC.visibility_of_element_located((By.ID, "user-name"))).send_keys("standard_user")

driver.find_element(By.ID, "password").send_keys("secret_sauce")
driver.find_element(By.ID, "login-button").click()

source = wait.until(EC.visibility_of_element_located((By.ID, "item_4_img_link")))

target = wait.until(EC.visibility_of_element_located((By.CLASS_NAME, "shopping_cart_link")))

ActionChains(driver).drag_and_drop(source,target).perform()

print("TC07: Drag and drop performed successfully")

time.sleep(3)

driver.quit()
```

```python
# TC08 - Customer searches for a product and waits for results
# Selenium Concept: Explicit Wait

driver = webdriver.Chrome()
driver.maximize_window()

driver.get("https://www.saucedemo.com/")

wait = WebDriverWait(driver, 10)

wait.until(EC.visibility_of_element_located((By.ID, "user-name"))).send_keys("standard_user")

driver.find_element(By.ID, "password").send_keys("secret_sauce")
driver.find_element(By.ID, "login-button").click()

product = wait.until(EC.visibility_of_element_located((By.CLASS_NAME, "inventory_item")))

print("TC08: Explicit wait completed successfully")
print("Product displayed:", product.text)

time.sleep(3)

driver.quit()
```

```python
# TC09 - Customer completes checkout and waits until Place Order
# Selenium Concept: Clickable Wait

driver = webdriver.Chrome()
driver.maximize_window()

driver.get("https://www.saucedemo.com/")

wait = WebDriverWait(driver, 10)

wait.until(EC.visibility_of_element_located((By.ID, "user-name"))).send_keys("standard_user")

driver.find_element(By.ID, "password").send_keys("secret_sauce")
driver.find_element(By.ID, "login-button").click()

wait.until(EC.element_to_be_clickable((By.ID, "add-to-cart-sauce-labs-backpack"))).click()

driver.find_element(By.CLASS_NAME,"shopping_cart_link").click()

wait.until(EC.element_to_be_clickable((By.ID, "checkout"))).click()

wait.until(EC.visibility_of_element_located((By.ID, "first-name"))).send_keys("Priyanka")

driver.find_element(By.ID,"last-name").send_keys("K")

driver.find_element(By.ID,"postal-code").send_keys("631501")

wait.until(EC.element_to_be_clickable((By.ID, "continue"))).click()

time.sleep(3)

place_order = wait.until(
    EC.element_to_be_clickable((By.ID, "finish"))
)
place_order.click()

print("TC09: Order submitted successfully")

time.sleep(3)

driver.quit()
```

```python
# TC10 - Customer completes purchase and waits for confirmation
# Selenium Concept: Alert Wait

driver = webdriver.Chrome()
driver.maximize_window()

driver.get("https://www.saucedemo.com/")

wait = WebDriverWait(driver, 10)
wait.until(EC.visibility_of_element_located((By.ID, "user-name"))).send_keys("standard_user")

driver.find_element(By.ID,"password").send_keys("secret_sauce")
driver.find_element(By.ID,"login-button").click()

wait.until(EC.element_to_be_clickable((By.ID, "add-to-cart-sauce-labs-backpack"))).click()

driver.find_element(By.CLASS_NAME,"shopping_cart_link").click()
driver.find_element(By.ID,"checkout").click()

wait.until(EC.visibility_of_element_located((By.ID, "first-name"))).send_keys("Priyanka")

driver.find_element(By.ID,"last-name").send_keys("K")
driver.find_element(By.ID,"postal-code").send_keys("631501")
driver.find_element(By.ID,"continue").click()

wait.until(EC.element_to_be_clickable((By.ID, "finish"))).click()
confirmation = wait.until(EC.visibility_of_element_located((By.CLASS_NAME, "complete-header")))

print("TC10:", confirmation.text)

time.sleep(3)

driver.quit()
```
---
# 8th October 2026
#### Selenium Xpath Coding

```python
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import Select
from selenium.webdriver.common.keys import Keys
import time

driver = webdriver.Chrome()
driver.maximize_window()

# ============================================================
# TC01 - Open student registration page
# ============================================================

driver.get("https://demoqa.com/automation-practice-form")
time.sleep(2)

print("TC01 - Registration page opened")


# ============================================================
# TC02 - Locate username / First Name - Attribute XPath
# ============================================================

first_name = driver.find_element(
    By.XPATH, "//input[@id='firstName']"
)

first_name.send_keys("Priyanka")

print("TC02 - First Name entered")


# ============================================================
# TC03 - Password
# ============================================================

email = driver.find_element(
    By.XPATH, "//input[@id='userEmail']"
)

email.send_keys("priyanka.student@saveetha.in")

print("TC03 - Email entered")


# ============================================================
# TC04 - Locate Submit - text()
# ============================================================

submit = driver.find_element(
    By.XPATH, "//button[text()='Submit']"
)

print("TC04 - Submit located")


# ============================================================
# TC05 - Locate textbox dynamically - contains()
# ============================================================

last_name = driver.find_element(
    By.XPATH, "//input[contains(@id,'lastName')]"
)

last_name.send_keys("K")

print("TC05 - Last Name located using contains()")


# ============================================================
# TC06 - Locate element with prefix - starts-with()
# ============================================================

mobile = driver.find_element(
    By.XPATH, "//input[starts-with(@id,'userNumber')]"
)

mobile.send_keys("8489246386")

print("TC06 - Mobile located using starts-with()")


# ============================================================
# TC07 - Find input using TWO attributes - and
# ============================================================

first_name_check = driver.find_element(
    By.XPATH,
    "//input[@id='firstName' and @placeholder='First Name']"
)

print("TC07 - Element located using AND")


# ============================================================
# TC08 - Find element using alternatives - or
# ============================================================

input_element = driver.find_element(
    By.XPATH,
    "//input[@type='text' or @type='email']"
)

print("TC08 - Element located using OR")


# ============================================================
# TC09 - Find parent form/group -  parent
# ============================================================

first_name_parent = driver.find_element(
    By.XPATH,
    "//input[@id='firstName']/parent::*"
)

print("TC09 - Parent element located")


# ============================================================
# TC10 - Find FORM from input - ancestor
# ============================================================

form = driver.find_element(
    By.XPATH,
    "//input[@id='firstName']/ancestor::form"
)

print("TC10 - Form located using ancestor")


# ============================================================
# TC11 - Find child inputs - child
# ============================================================

child_inputs = driver.find_elements(
    By.XPATH,
    "//form/child::div//input"
)

print("TC11 - Child inputs located")
print("Number of child inputs:", len(child_inputs))


# ============================================================
# TC12 - Find next element - following
# ============================================================

next_input = driver.find_element(
    By.XPATH,
    "//input[@id='firstName']/following::input[1]"
)

print("TC12 - Following element located")


# ============================================================
# TC13 - Find checkbox - Attribute XPath
# ============================================================

hobby_sports = driver.find_element(
    By.XPATH,
    "//input[@id='hobbies-checkbox-1']"
)

# The actual checkbox can be hidden behind its label.
# Click the label instead.
hobby_label = driver.find_element(
    By.XPATH,
    "//label[@for='hobbies-checkbox-1']"
)

hobby_label.click()

print("TC13 - Sports checkbox selected")


# ============================================================
# TC14 - Find radio button - Attribute XPath
# ============================================================

male_radio = driver.find_element(
    By.XPATH,
    "//input[@id='gender-radio-2']"
)

male_label = driver.find_element(
    By.XPATH,
    "//label[@for='gender-radio-2']"
)

male_label.click()

print("TC14 - Female radio button selected")

# ============================================================
# TC15 - Select State dropdown
# ============================================================

state_input = driver.find_element(
    By.XPATH,
    "/html/body/div/div/div/div/div[2]/div[1]/form/div[10]/div[2]/div/div/div[1]/div[2]/input"
)

driver.execute_script(
    "arguments[0].scrollIntoView({block:'center'});",
    state_input
)

time.sleep(2)

# JavaScript click because normal Selenium click is intercepted
driver.execute_script(
    "arguments[0].click();",
    state_input
)

time.sleep(2)

state_input.send_keys("NCR")

time.sleep(2)

state_input.send_keys(Keys.ENTER)

print("TC15 - State selected")

# ============================================================
# TC16 - Find SECOND textbox - XPath index
# ============================================================

second_textbox = driver.find_element(
    By.XPATH,
    "(//input[@type='text'])[2]"
)

print("TC16 - Second textbox located")

# ============================================================
# TC18 - Find ALL input fields - find_elements()
# ============================================================

all_inputs = driver.find_elements(
    By.XPATH,
    "//input"
)

print("TC18 - All input fields located")
print("Total input fields:", len(all_inputs))


# ============================================================
# TC19 - Find dynamic element - contains()
# ============================================================

dynamic_element = driver.find_element(
    By.XPATH,
    "//input[contains(@id,'user')]"
)

print("TC19 - Dynamic element located")


# ============================================================
# TC20 - Complete registration
# ============================================================

# Address
address = driver.find_element(
    By.XPATH,
    "//textarea[@id='currentAddress']"
)

address.send_keys("Chennai, Tamil Nadu")


# Select City
city_dropdown = driver.find_element(
    By.XPATH,
    "//div[contains(@id,'city')]"
)

city_dropdown.click()

time.sleep(2)

city_option = driver.find_element(
    By.XPATH,
    "//div[text()='Delhi']"
)

city_option.click()


# Click Submit
submit.click()

time.sleep(2)


# ============================================================
# TC17 - Verify successful submission
# ============================================================

success_message = driver.find_element(
    By.XPATH,
    "//*[text()='Thanks for submitting the form']"
)

if success_message.is_displayed():
    print("TC17 - Submission successful")


print("TC20 - Registration automation completed successfully!")

time.sleep(5)

driver.quit()
```
---
# 9th October 2026

#### Selenium - Web Tables Assignment

```python

import time

from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC

driver = webdriver.Chrome()
driver.maximize_window()

wait = WebDriverWait(driver, 15)

driver.get("https://assertqa.com/practice/webtables")

wait.until(EC.presence_of_element_located((By.TAG_NAME, "table")))

print("Website opened successfully", flush=True)

# TC01 - Print all column headings

print("\nTC01 - Print all column headings")

table = driver.find_element(By.TAG_NAME, "table")
headers = table.find_elements(By.CSS_SELECTOR, "thead th")

for header in headers:
    print(header.text)

print("TC01 PASS")
time.sleep(2)


# TC02 - Print the first data row

print("\nTC02 - Print the first data row")

rows = table.find_elements(By.CSS_SELECTOR, "tbody tr")

if rows:
    print(rows[0].text)
    driver.execute_script("arguments[0].scrollIntoView({block:'center'});",rows[0])
    print("TC02 PASS")
else:
    print("TC02 FAIL")

time.sleep(2)


# TC03 - Print the last data row

print("\nTC03 - Print the last data row")

if rows:
    driver.execute_script("arguments[0].scrollIntoView({block:'center'});",rows[-1])
    print(rows[-1].text)
    print("TC03 PASS")
else:
    print("TC03 FAIL")

time.sleep(2)


# TC04 - Search for an employee by last name

print("\nTC04 - Search for an employee by last name")

headers_text = [h.text.strip().lower() for h in headers]

if "last name" in headers_text and rows:
    last_name = "Brown"
    search = wait.until(EC.presence_of_element_located((By.CSS_SELECTOR, "input[data-cy='search-input']")))

    driver.execute_script("""
        window.scrollTo(0, 0);
        arguments[0].scrollIntoView({
            block: 'center',
            inline: 'center'
        });
        arguments[0].focus();
    """, search)

    search.send_keys(last_name)

    print("Searching for:", last_name, flush=True)
    time.sleep(2)

    print("Search results:")

    search_rows = driver.find_elements(By.CSS_SELECTOR, "tbody tr")

    matches = []

    for row in search_rows:
        if row.text.strip():
            cells = row.find_elements(By.TAG_NAME, "td")

            if (len(cells) > headers_text.index("last name")
                and cells[headers_text.index("last name")].text.strip().lower()
                == last_name.lower()):
                matches.append(row.text)
                print(row.text)

    if matches:
        print("TC04 PASS")
    else:
        print("TC04 FAIL - No matching employee found")

    search.clear()

else:
    print("TC04 FAIL - Last Name column or data rows not found")

time.sleep(2)


# TC05 - Extract all email addresses

print("\nTC05 - Extract all email addresses")

email_index = next((i for i, h in enumerate(headers_text) if "email" in h),None)

emails = []

if email_index is not None:
    for row in driver.find_elements(By.CSS_SELECTOR, "tbody tr"):
        cells = row.find_elements(By.TAG_NAME, "td")

        if len(cells) > email_index:
            email = cells[email_index].text.strip()

            if "@" in email:
                emails.append(email)

for email in emails:
    print(email)

print("TC05", "PASS" if emails else "FAIL")

time.sleep(2)


# TC06 - Find employee with highest Due amount

print("\nTC06 - Find employee with highest Due amount")

due_index = next((i for i, h in enumerate(headers_text) if "due" in h),None)

employee_due = []

if due_index is not None:
    for row in driver.find_elements(By.CSS_SELECTOR, "tbody tr"):
        cells = row.find_elements(By.TAG_NAME, "td")

        if len(cells) > due_index:
            try:
                amount = float(cells[due_index].text.replace("$", "").replace(",", ""))
                employee_due.append((amount, row.text))

            except ValueError:
                pass

if employee_due:
    highest = max(employee_due, key=lambda x: x[0])

    print("Highest Due:", highest[0])
    print("Employee:", highest[1])
    print("TC06 PASS")
else:
    print("TC06 FAIL - Due column or numeric values not found")

time.sleep(2)


# TC07 - Verify website link exists

print("\nTC07 - Verify website link exists")

links = driver.find_elements(By.CSS_SELECTOR, "table a[href]")

if links:
    print("Website URL:", links[0].get_attribute("href"))
    print("TC07 PASS")
else:
    print("TC07 FAIL - No link found in the table")

time.sleep(2)


# TC08 - Count data rows without header

print("\nTC08 - Count data rows")

data_rows = [row for row in driver.find_elements(By.CSS_SELECTOR, "tbody tr")if row.text.strip()]

print("Total data rows:", len(data_rows))
print("TC08", "PASS" if data_rows else "FAIL")

print("\nAll test cases completed.")
driver.quit()
```
