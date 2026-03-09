### 1. Check if a Number is Palindrome

**Problem Statement**
You are given a number enclosed inside square brackets. Determine whether the number is a **palindrome**.

**Input Format**
A single line containing a number inside square brackets.

**Output Format**
Print `Palindrome` or `Not Palindrome`.

**Sample Input**

```
[1221]
```

**Sample Output**

```
Palindrome
```

**Explanation**
1221 reversed is still 1221.

**Solution**

```python
s = input().strip()
n = int(s.strip("[]"))
rev = int(str(n)[::-1])

if n == rev:
    print("Palindrome")
else:
    print("Not Palindrome")
```

---

# 2. Palindrome Numbers in Range

**Problem Statement**
Find all palindrome numbers in a given range written in bracket format.

**Input Format**
Single line:

```
[start,end]
```

**Output Format**
Print palindrome numbers separated by space.

**Sample Input**

```
[10,150]
```

**Sample Output**

```
11 22 33 44 55 66 77 88 99 101 111 121 131 141
```

**Explanation**
Numbers that read the same forward and backward are printed.

**Solution**

```python
s = input().strip()
a,b = map(int,s.strip("[]").split(","))

for i in range(a,b+1):
    if str(i)==str(i)[::-1]:
        print(i,end=" ")
```

---

# 3. Check Prime Number

**Problem Statement**
Check whether the given number is prime.

**Input Format**
Number inside parentheses.

```
(17)
```

**Output Format**
`Prime` or `Not Prime`

**Sample Input**

```
(17)
```

**Sample Output**

```
Prime
```

**Explanation**
17 has only two factors.

**Solution**

```python
s=input().strip()
n=int(s.strip("()"))

if n<=1:
    print("Not Prime")
else:
    for i in range(2,int(n**0.5)+1):
        if n%i==0:
            print("Not Prime")
            break
    else:
        print("Prime")
```

---

# 4. Prime Numbers in Range

**Problem Statement**
Print all prime numbers within the given range.

**Input Format**

```
10 50
```

**Output Format**
Prime numbers separated by space.

**Sample Input**

```
10 20
```

**Sample Output**

```
11 13 17 19
```

**Explanation**
These numbers have exactly two divisors.

**Solution**

```python
a,b=map(int,input().split())

for num in range(a,b+1):
    if num>1:
        for i in range(2,int(num**0.5)+1):
            if num%i==0:
                break
        else:
            print(num,end=" ")
```

---

# 5. Armstrong Number

**Problem Statement**
Check if a number is an Armstrong number.

**Input Format**
Digits written continuously.

Example

```
153
```

**Output Format**
`Armstrong` or `Not Armstrong`

**Sample Input**

```
153
```

**Sample Output**

```
Armstrong
```

**Explanation**
1³ + 5³ + 3³ = 153.

**Solution**

```python
n=int(input())
temp=n
digits=len(str(n))
sum=0

while n>0:
    d=n%10
    sum+=d**digits
    n//=10

if sum==temp:
    print("Armstrong")
else:
    print("Not Armstrong")
```

---

# 6. Perfect Number

**Problem Statement**
Check whether a number equals the sum of its factors excluding itself.

**Input Format**

```
{28}
```

**Output Format**
`Perfect Number` or `Not Perfect Number`

**Sample Input**

```
{28}
```

**Sample Output**

```
Perfect Number
```

**Explanation**
1+2+4+7+14 = 28.

**Solution**

```python
s=input()
n=int(s.strip("{}"))

sum=0
for i in range(1,n):
    if n%i==0:
        sum+=i

if sum==n:
    print("Perfect Number")
else:
    print("Not Perfect Number")
```

---

# 7. Even or Odd

**Problem Statement**
Determine whether the number is even or odd.

**Input Format**
Comma separated value.

```
24,
```

**Output Format**
`Even` or `Odd`

**Sample Input**

```
13,
```

**Sample Output**

```
Odd
```

**Solution**

```python
n=int(input().replace(",",""))

if n%2==0:
    print("Even")
else:
    print("Odd")
```

---

# 8. Positive or Negative

**Input Format**

```
#-15
```

**Output Format**
`Positive`, `Negative`, or `Zero`

**Sample Input**

```
#-15
```

**Sample Output**

```
Negative
```

**Solution**

```python
n=int(input().replace("#",""))

if n>0:
    print("Positive")
elif n<0:
    print("Negative")
else:
    print("Zero")
```

---

# 9. Sum of First N Natural Numbers

**Input Format**

```
N=10
```

**Output Format**
Sum

**Sample Input**

```
N=5
```

**Sample Output**

```
15
```

**Solution**

```python
s=input()
n=int(s.split("=")[1])

print(n*(n+1)//2)
```

---

# 10. Greatest of Two Numbers

**Input Format**

```
[10 45]
```

**Output Format**
Greatest number.

**Sample Input**

```
[12 5]
```

**Sample Output**

```
12
```

**Solution**

```python
s=input()
a,b=map(int,s.strip("[]").split())

print(max(a,b))
```

---

# 11. Leap Year

**Input Format**

```
Year:2024
```

**Output Format**
`Leap Year` or `Not Leap Year`

**Sample Input**

```
Year:2024
```

**Sample Output**

```
Leap Year
```

**Solution**

```python
s=input()
year=int(s.split(":")[1])

if (year%4==0 and year%100!=0) or year%400==0:
    print("Leap Year")
else:
    print("Not Leap Year")
```

---

# 12. Reverse Digits

**Input Format**

```
<12345>
```

**Output Format**
Reversed number.

**Sample Input**

```
<1234>
```

**Sample Output**

```
4321
```

**Solution**

```python
s=input()
n=int(s.strip("<>"))

print(int(str(n)[::-1]))
```

---

# 13. Fibonacci upto N Terms

**Input Format**

```
fib(7)
```

**Output Format**
Fibonacci sequence.

**Sample Input**

```
fib(5)
```

**Sample Output**

```
0 1 1 2 3
```

**Solution**

```python
s=input()
n=int(s[4:-1])

a,b=0,1

for i in range(n):
    print(a,end=" ")
    a,b=b,a+b
```

---

# 14. Factorial

**Input Format**

```
fact:5
```

**Output Format**
Factorial value.

**Sample Input**

```
fact:5
```

**Sample Output**

```
120
```

**Solution**

```python
s=input()
n=int(s.split(":")[1])

fact=1
for i in range(1,n+1):
    fact*=i

print(fact)
```

---

# 15. GCD of Two Numbers

**Input Format**

```
(48,18)
```

**Output Format**
GCD

**Sample Input**

```
(48,18)
```

**Sample Output**

```
6
```

**Solution**

```python
import math

s=input()
a,b=map(int,s.strip("()").split(","))

print(math.gcd(a,b))
```

---

# 16. LCM of Two Numbers

**Input Format**

```
LCM 12 15
```

**Output Format**
LCM

**Sample Input**

```
LCM 12 15
```

**Sample Output**

```
60
```

**Solution**

```python
import math

_,a,b=input().split()
a=int(a)
b=int(b)

print(abs(a*b)//math.gcd(a,b))
```

---

# 17. Area of Circle

**Input Format**

```
radius=7
```

**Output Format**
Area

**Sample Input**

```
radius=7
```

**Sample Output**

```
153.86
```

**Solution**

```python
s=input()
r=float(s.split("=")[1])

print(round(3.14*r*r,2))
```

---

# 18. Sum of Digits

**Input Format**

```
digits:12345
```

**Output Format**
Sum of digits.

**Sample Input**

```
digits:123
```

**Sample Output**

```
6
```

**Solution**

```python
s=input()
n=s.split(":")[1]

print(sum(map(int,n)))
```
Below are the **remaining problems with tricky input formats and Python solutions** (same exam style).

---

# 19. Power of a Number

**Problem Statement**
Find the power of a number.

**Input Format**

```
pow(2,5)
```

**Output Format**
Result of power.

**Sample Input**

```
pow(2,5)
```

**Sample Output**

```
32
```

**Solution**

```python
s=input().strip()
a,b=s[4:-1].split(",")
a=int(a)
b=int(b)

print(a**b)
```

---

# 20. Factors of a Number

**Input Format**

```
num:12
```

**Output Format**
All factors separated by space.

**Sample Input**

```
num:12
```

**Sample Output**

```
1 2 3 4 6 12
```

**Solution**

```python
s=input()
n=int(s.split(":")[1])

for i in range(1,n+1):
    if n%i==0:
        print(i,end=" ")
```

---

# 21. Prime Factors of Number

**Input Format**

```
pf[84]
```

**Output Format**
Prime factors separated by space.

**Sample Input**

```
pf[84]
```

**Sample Output**

```
2 2 3 7
```

**Solution**

```python
s=input()
n=int(s[3:-1])

i=2
while i<=n:
    if n%i==0:
        print(i,end=" ")
        n//=i
    else:
        i+=1
```

---

# 22. Strong Number

**Input Format**

```
strong=145
```

**Output Format**
`Strong Number` or `Not Strong Number`

**Sample Input**

```
strong=145
```

**Sample Output**

```
Strong Number
```

**Solution**

```python
import math

s=input()
n=int(s.split("=")[1])

temp=n
sum=0

while n>0:
    d=n%10
    sum+=math.factorial(d)
    n//=10

if sum==temp:
    print("Strong Number")
else:
    print("Not Strong Number")
```

---

# 23. Automorphic Number

**Input Format**

```
auto(25)
```

**Output Format**
`Automorphic` or `Not Automorphic`

**Sample Input**

```
auto(25)
```

**Sample Output**

```
Automorphic
```

**Solution**

```python
s=input()
n=int(s[5:-1])

sq=n*n

if str(sq).endswith(str(n)):
    print("Automorphic")
else:
    print("Not Automorphic")
```

---

# 24. Harshad Number

**Input Format**

```
harshad=18
```

**Output Format**
`Harshad Number` or `Not Harshad Number`

**Sample Input**

```
harshad=18
```

**Sample Output**

```
Harshad Number
```

**Solution**

```python
s=input()
n=int(s.split("=")[1])

sum=0
temp=n

while temp>0:
    sum+=temp%10
    temp//=10

if n%sum==0:
    print("Harshad Number")
else:
    print("Not Harshad Number")
```

---

# 25. Abundant Number

**Input Format**

```
abundant{12}
```

**Output Format**
`Abundant` or `Not Abundant`

**Sample Input**

```
abundant{12}
```

**Sample Output**

```
Abundant
```

**Solution**

```python
s=input()
n=int(s[9:-1])

sum=0

for i in range(1,n):
    if n%i==0:
        sum+=i

if sum>n:
    print("Abundant")
else:
    print("Not Abundant")
```

---

# 26. Maximum and Minimum Digit

**Input Format**

```
digits[59431]
```

**Output Format**
`Max Min`

**Sample Input**

```
digits[59431]
```

**Sample Output**

```
9 1
```

**Solution**

```python
s=input()
n=s[7:-1]

digits=list(map(int,n))

print(max(digits),min(digits))
```

---

# 27. Sum of Numbers in Range

**Input Format**

```
range(5,10)
```

**Output Format**
Sum

**Sample Input**

```
range(5,10)
```

**Sample Output**

```
45
```

**Solution**

```python
s=input()
a,b=map(int,s[6:-1].split(","))

print(sum(range(a,b+1)))
```

---

# 28. Permutations nPr

**Input Format**

```
perm(5,2)
```

**Output Format**
Value of permutation.

**Sample Input**

```
perm(5,2)
```

**Sample Output**

```
20
```

**Solution**

```python
import math

s=input()
n,r=map(int,s[5:-1].split(","))

print(math.factorial(n)//math.factorial(n-r))
```

---

# 29. Add Two Fractions

**Input Format**

```
1/2 + 3/4
```

**Output Format**
Result fraction.

**Sample Input**

```
1/2 + 3/4
```

**Sample Output**

```
10/8
```

**Solution**

```python
s=input()

a,b=s.split("+")
n1,d1=map(int,a.strip().split("/"))
n2,d2=map(int,b.strip().split("/"))

num=n1*d2+n2*d1
den=d1*d2

print(f"{num}/{den}")
```

---

# 30. Replace 0 with 1

**Input Format**

```
num=102030
```

**Output Format**
Number after replacement.

**Sample Input**

```
num=102030
```

**Sample Output**

```
112131
```

**Solution**

```python
s=input()
n=s.split("=")[1]

print(n.replace("0","1"))
```

---

# 31. Sum of Two Prime Numbers

**Input Format**

```
sumprime(34)
```

**Output Format**
`Yes` or `No`

**Sample Input**

```
sumprime(34)
```

**Sample Output**

```
Yes
```

**Solution**

```python
s=input()
n=int(s[9:-1])

def prime(x):
    if x<2:
        return False
    for i in range(2,int(x**0.5)+1):
        if x%i==0:
            return False
    return True

for i in range(2,n):
    if prime(i) and prime(n-i):
        print("Yes")
        break
else:
    print("No")
```

---

# 32. Quadratic Equation Roots

**Input Format**

```
quad(1,5,6)
```

**Output Format**
Roots.

**Sample Input**

```
quad(1,5,6)
```

**Sample Output**

```
-2.0 -3.0
```

**Solution**

```python
import math

s=input()
a,b,c=map(int,s[5:-1].split(","))

d=b*b-4*a*c

r1=(-b+math.sqrt(d))/(2*a)
r2=(-b-math.sqrt(d))/(2*a)

print(r1,r2)
```

---

✅ Now you have **ALL number-based coding problems with tricky inputs and working solutions**, useful for preparation of the **TCS National Qualifier Test coding round.

---

If you want, I can also give **25 MOST REPEATED TCS NQT coding questions (arrays + strings + numbers)** that appear **almost every year**.
Those will help you **crack the exam faster.** 🚀
