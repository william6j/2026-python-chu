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

# 6-1
text = input("輸入一句話: ")
words = text.split()
count = {}
for w in words:
    if w in count:
        count[w] += 1
    else:
        count[w] = 1
print(count)

# 6-2
text = input("輸入文章: ")
count = {}
for ch in text:
    if ch in count:
        count[ch] += 1
    else:
        count[ch] = 1
print(count)

# 6-3
morse_dict = {
    'A': '.-', 'B': '-...', 'C': '-.-.',
    'D': '-..', 'E': '.', 'F': '..-.',
    'G': '--.', 'H': '....'
}
text = input("輸入英文: ").upper()
result = []
for ch in text:
    if ch in morse_dict:
        result.append(morse_dict[ch])
    else:
        result.append('?')
print(" ".join(result))

# 6-4
import random
nums = set()
while len(nums) < 6:
    nums.add(random.randint(1, 49))
print("你的號碼:", nums)
# 6-5
cart = {
    "apple": 30,
    "banana": 20,
    "milk": 50
}
total = 0
for price in cart.values():
    total += price
print("總金額:", total)

# 7-1
def universal_calculator(a, b, operation='add', history=None):
    if history is None:
        history = []    
    if operation == 'add':
        result = a + b
    elif operation == 'sub':
        result = a - b
    else:
        result = "Unsupported Operation" 
    history.append(result)
    return result, history

# 7-2
import math
def is_prime(n):
    if n <= 1:
        return False
    if n == 2:
        return True
    if n % 2 == 0:
        return False
    for i in range(3, int(math.sqrt(n)) + 1, 2):
        if n % i == 0:
            return False
    return True

# 7-3
def c_to_f(celsius):
    return (celsius * 9/5) + 32
def f_to_c(fahrenheit):
    return (fahrenheit - 32) * 5/9
if __name__ == "__main__":
    test_c = 100
    print(f"{test_c}°C 等於 {c_to_f(test_c)}°F")


# 8-1
students = []
def add_score(name, score):
    students.append({"name": name, "score": score})
def show_summary():
    if not students: return
    avg = sum(s['score'] for s in students) / len(students)
    fail_list = [s['name'] for s in students if s['score'] < 60]
    print(f"平均分數: {avg:.2f}")
    print(f"不及格名單: {', '.join(fail_list) if fail_list else '無'}")

# 8-2
state = "森林入口"
while True:
    print(f"\n你現在在：{state}")
    action = input("你要去哪裡？(左/右/離開): ")
    if action == "離開":
        print("遊戲結束"); break
    elif state == "森林入口":
        state = "神祕洞窟" if action == "左" else "平靜湖畔"
    else:
        print("走到底了，回頭吧！")
        state = "森林入口"
# 8-3
def check_password(pwd):
    has_upper = any(c.isupper() for c in pwd)
    has_lower = any(c.islower() for c in pwd)
    has_digit = any(c.isdigit() for c in pwd)
    length_ok = len(pwd) >= 8
    score = sum([has_upper, has_lower, has_digit, length_ok])
    levels = {4: "強", 3: "中", 2: "弱", 1: "極弱", 0: "極弱"}
    return levels[score]
print(f"強度：{check_password('Python123')}")

# 8-4
low, high = 1, 100
print("請在心中想一個 1-100 的數字...")

while low <= high:
    mid = (low + high) // 2
    ans = input(f"電腦猜 {mid}，請問是 太大(L)、太小(S)、還是正確(C)？ ").upper()
    if ans == 'C':
        print("AI 勝利！"); break
    elif ans == 'L':
        high = mid - 1
    elif ans == 'S':
        low = mid + 1
        
# 8-5
low, high = 1, 100
print("請在心中想一個 1-100 的數字...")

while low <= high:
    mid = (low + high) // 2
    ans = input(f"電腦猜 {mid}，請問是 太大(L)、太小(S)、還是正確(C)？ ").upper()
    if ans == 'C':
        print("AI 勝利！"); break
    elif ans == 'L':
        high = mid - 1
    elif ans == 'S':
        low = mid + 1
