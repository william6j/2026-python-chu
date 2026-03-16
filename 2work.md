#2-1
n = int(input())
print(n % 2)

#2-2
F = float(input())
C = (F - 32) * 5 / 9
print(C)

#2-3
twd = float(input())
usd = twd / 32
print(usd)

#2-4
sec = int(input())
h = sec // 3600
m = (sec % 3600) // 60
s = sec % 60
print(h, ":", m, ":", s)

#2-5
price = float(input())
discount = price * 0.8
print(discount)

#2-6
b = float(input())
h = float(input())
area = (b * h) / 2
print(area)

#2-7
age = int(input())
code = input()
print(age >= 18 and code == "PASS")

#2-8
is_weekend = input()
is_holiday = input()
print(is_weekend == "True" or is_holiday == "True")

#2-9
x = int(input())
y = int(input())
print(y != 0 and x / y > 1)

#2-10
money = float(input())
price = float(input())
print(money >= price)
