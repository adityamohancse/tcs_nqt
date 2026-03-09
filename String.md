Below are **all problems solved using simple loops and minimal built-ins**, similar to the pattern used in **TCS NQT coding section**.

---

# 1. Check if a String is Palindrome

### Input

```
str(aba)
```

### Code

```python
s=input().strip()
t=s[4:-1]

rev=""
for i in t:
    rev=i+rev

if t==rev:
    print("Palindrome")
else:
    print("Not Palindrome")
```

---

# 2. Count vowels, consonants, spaces

### Input

```
str(hello world)
```

```python
s=input().strip()
t=s[4:-1]

v=c=sp=0

for i in t:
    if i in "aeiouAEIOU":
        v+=1
    elif i==" ":
        sp+=1
    else:
        c+=1

print("Vowels:",v)
print("Consonants:",c)
print("Spaces:",sp)
```

---

# 3. ASCII value of a character

### Input

```
ascii(A)
```

```python
s=input().strip()
ch=s[6:-1]

print(ord(ch))
```

---

# 4. Remove vowels

### Input

```
str(hello)
```

```python
s=input().strip()
t=s[4:-1]

res=""

for i in t:
    if i not in "aeiouAEIOU":
        res+=i

print(res)
```

---

# 5. Remove spaces

### Input

```
str(hello world)
```

```python
s=input().strip()
t=s[4:-1]

res=""

for i in t:
    if i!=" ":
        res+=i

print(res)
```

---

# 6. Remove non-alphabets

```python
s=input().strip()
t=s[4:-1]

res=""

for i in t:
    if ('a'<=i<='z') or ('A'<=i<='Z'):
        res+=i

print(res)
```

---

# 7. Reverse string

```python
s=input().strip()
t=s[4:-1]

rev=""

for i in t:
    rev=i+rev

print(rev)
```

---

# 8. Remove brackets from expression

### Input

```
exp((a+b)*(c+d))
```

```python
s=input().strip()
t=s[4:-1]

res=""

for i in t:
    if i!="(" and i!=")":
        res+=i

print(res)
```

---

# 9. Sum of numbers in string

### Input

```
str(a1b2c3)
```

```python
s=input().strip()
t=s[4:-1]

sum=0

for i in t:
    if '0'<=i<='9':
        sum+=int(i)

print(sum)
```

---

# 10. Capitalize first and last character

```python
s=input().strip()
t=s[4:-1]

words=t.split()

for w in words:
    if len(w)==1:
        print(w.upper(),end=" ")
    else:
        print(w[0].upper()+w[1:-1]+w[-1].upper(),end=" ")
```

---

# 11. Frequency of characters

```python
s=input().strip()
t=s[4:-1]

for i in t:
    count=0
    for j in t:
        if i==j:
            count+=1
    print(i,count)
```

---

# 12. First non-repeating character

```python
s=input().strip()
t=s[4:-1]

for i in t:
    count=0
    for j in t:
        if i==j:
            count+=1
    if count==1:
        print(i)
        break
```

---

# 13. Check Anagram

```python
s=input().strip()
a,b=s[4:-1].split(",")

if sorted(a)==sorted(b):
    print("Anagram")
else:
    print("Not Anagram")
```

---

# 14. Maximum occurring character

```python
s=input().strip()
t=s[4:-1]

maxc=0
ch=""

for i in t:
    count=0
    for j in t:
        if i==j:
            count+=1
    if count>maxc:
        maxc=count
        ch=i

print(ch)
```

---

# 15. Remove duplicates

```python
s=input().strip()
t=s[4:-1]

res=""

for i in t:
    if i not in res:
        res+=i

print(res)
```

---

# 16. Print duplicate characters

```python
s=input().strip()
t=s[4:-1]

for i in t:
    count=0
    for j in t:
        if i==j:
            count+=1
    if count>1:
        print(i)
```

---

# 17. Remove characters of string2 from string1

```python
s=input().strip()
a,b=s[4:-1].split(",")

res=""

for i in a:
    if i not in b:
        res+=i

print(res)
```

---

# 18. Next lexicographic alphabet

```python
s=input().strip()
t=s[4:-1]

res=""

for i in t:
    res+=chr(ord(i)+1)

print(res)
```

---

# 19. Largest word in string

```python
s=input().strip()
t=s[4:-1]

words=t.split()

maxw=""

for w in words:
    if len(w)>len(maxw):
        maxw=w

print(maxw)
```

---

# 20. Sort characters in string

```python
s=input().strip()
t=s[4:-1]

print("".join(sorted(t)))
```

---

# 21. Count words

```python
s=input().strip()
t=s[4:-1]

words=t.split()

print(len(words))
```

---

# 22. Word with highest repeated letters

```python
s=input().strip()
t=s[4:-1]

words=t.split()

maxc=0
res=""

for w in words:
    count=0
    for i in w:
        if w.count(i)>count:
            count=w.count(i)
    if count>maxc:
        maxc=count
        res=w

print(res)
```

---

# 23. Change case of characters

```python
s=input().strip()
t=s[4:-1]

res=""

for i in t:
    if 'a'<=i<='z':
        res+=chr(ord(i)-32)
    else:
        res+=chr(ord(i)+32)

print(res)
```

---

# 24. Concatenate strings

```python
s=input().strip()
a,b=s[4:-1].split(",")

print(a+b)
```

---

# 25. Find substring position

```python
s=input().strip()
a,b=s[4:-1].split(",")

print(a.find(b))
```

---

# 26. Reverse words in string

```python
s=input().strip()
t=s[4:-1]

words=t.split()

for i in range(len(words)-1,-1,-1):
    print(words[i],end=" ")
```

---

