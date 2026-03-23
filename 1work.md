<img width="773" height="272" alt="image" src="https://github.com/user-attachments/assets/ce52e6f7-9b93-4755-ae30-266dc1e2af7b" />

# 2-1
n = int(input())
print(n % 2)

# 2-2
F = float(input())
C = (F - 32) * 5 / 9
print(C)

# 2-3
twd = float(input())
usd = twd / 32
print(usd)

# 2-4
sec = int(input())
h = sec // 3600
m = (sec % 3600) // 60
s = sec % 60
print(h, ":", m, ":", s)

# 2-5
price = float(input())
discount = price * 0.8
print(discount)

# 2-6
b = float(input())
h = float(input())
area = (b * h) / 2
print(area)

# 2-7
age = int(input())
code = input()
print(age >= 18 and code == "PASS")

# 2-8
is_weekend = input()
is_holiday = input()
print(is_weekend == "True" or is_holiday == "True")

# 2-9
x = int(input())
y = int(input())
print(y != 0 and x / y > 1)

# 2-10
money = float(input())
price = float(input())
print(money >= price)

# 3-1
year = int(input())
if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):
    print("Leap Year")
else:
    print("Not Leap Year")
    
# 3-2
a = int(input())
b = int(input())
c = int(input())
max_num = a
if b > max_num:
    max_num = b
if c > max_num:
    max_num = c
print(max_num)

# 3-3
a = float(input())
op = input()
b = float(input())
if op == "+":
    print(a + b)
elif op == "-":
    print(a - b)
elif op == "*":
    print(a * b)
elif op == "/":
    print(a / b)
else:
    print("error")
    
# 3-4
money = int(input())
if money >= 120:
    print(True)
else:
    print(False)

    
# 3-5 to 3-10
weight = float(input())
height = float(input())
bmi = weight / (height ** 2)
if bmi < 18.5:
    print("Underweight")
elif bmi < 24:
    print("Normal")
elif bmi < 27:
    print("Overweight")
else:
    print("Obese")

# 4-1
answer = 50
guess = int(input())
while guess != answer:
    if guess > answer:
        print("Too big")
    else:
        print("Too small")
    guess = int(input())
print("Correct")

# 4-2
for i in range(1, 10):
    for j in range(1, 10):
        print(i, "*", j, "=", i*j)
        
# 4-3
n = int(input())
is_prime = True
for i in range(2, n):
    if n % i == 0:
        is_prime = False
if is_prime and n > 1:
    print("Prime")
else:
    print("Not Prime")
    
# 4-4
n = int(input())
for i in range(1, n+1):
    for j in range(n-i):
        print(" ", end="")
    for k in range(2*i-1):
        print("*", end="")
    print()
    
# 5-1
scores = []

for i in range(5):
    score = int(input(f"請輸入第{i+1}個成績: "))
    scores.append(score)
average = sum(scores) / len(scores)
highest = max(scores)
lowest = min(scores)
print("平均:", average)
print("最高:", highest)
print("最低:", lowest)

# 5-2
scores = [75, 40, 90, 55, 80]
passed = []
for s in scores:
    if s >= 60:
        passed.append(s)
print("及格成績:", passed)

# 5-3
a = [1, 2, 3]
b = [4, 5, 6]
result = []
for i in range(len(a)):
    result.append(a[i] + b[i])
print(result)

# 5-4
nums = [1, 2, 3, 2, 4, 1, 5]
duplicates = []
for n in nums:
    if nums.count(n) > 1 and n not in duplicates:
        duplicates.append(n)
print("重複元素:", duplicates)

# 5-5
text = input("輸入文字: ")
shift = int(input("位移: "))
result = ""
for char in text:
    if char.isalpha():
        base = ord('A') if char.isupper() else ord('a')
        result += chr((ord(char) - base + shift) % 26 + base)
    else:
        result += char
print("加密後:", result)
