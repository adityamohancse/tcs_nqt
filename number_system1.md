



---

# 1️⃣ Convert Binary to Decimal

### Input

```
bin(1011)
```

### Output

```
11
```

```python
s = input().strip()

b = int(s[4:-1])

decimal = 0
base = 1

while b > 0:
    last = b % 10
    decimal += last * base
    base *= 2
    b //= 10

print(decimal)
```

---

# 2️⃣ Convert Binary to Octal

### Input

```
binoct(101011)
```

### Output

```
53
```

```python
s = input().strip()

b = int(s[7:-1])

decimal = 0
base = 1

while b > 0:
    last = b % 10
    decimal += last * base
    base *= 2
    b //= 10

octal = ""

while decimal > 0:
    octal = str(decimal % 8) + octal
    decimal //= 8

print(octal)
```

---

# 3️⃣ Decimal to Binary

### Input

```
decbin(10)
```

### Output

```
1010
```

```python
s = input().strip()

n = int(s[7:-1])

binary = ""

while n > 0:
    binary = str(n % 2) + binary
    n //= 2

print(binary)
```

---

# 4️⃣ Decimal to Octal

### Input

```
decoct(25)
```

### Output

```
31
```

```python
s = input().strip()

n = int(s[7:-1])

octal = ""

while n > 0:
    octal = str(n % 8) + octal
    n //= 8

print(octal)
```

---

# 5️⃣ Octal to Binary

### Input

```
octbin(17)
```

### Output

```
1111
```

```python
s = input().strip()

o = int(s[7:-1])

decimal = 0
base = 1

while o > 0:
    last = o % 10
    decimal += last * base
    base *= 8
    o //= 10

binary = ""

while decimal > 0:
    binary = str(decimal % 2) + binary
    decimal //= 2

print(binary)
```

---

# 6️⃣ Octal to Decimal

### Input

```
octdec(17)
```

### Output

```
15
```

```python
s = input().strip()

o = int(s[7:-1])

decimal = 0
base = 1

while o > 0:
    last = o % 10
    decimal += last * base
    base *= 8
    o //= 10

print(decimal)
```

---

# 7️⃣ Convert Digits to Words

### Input

```
word(123)
```

### Output

```
One Two Three
```

```python
s = input().strip()

n = s[5:-1]

words = ["Zero","One","Two","Three","Four","Five","Six","Seven","Eight","Nine"]

for i in n:
    print(words[int(i)], end=" ")
```

---

✅ These follow the **same pattern you shared earlier**:

```
input()
slicing
string parsing
loop logic
print output
```

This is **exactly how TCS NQT coding questions usually appear**.

---



