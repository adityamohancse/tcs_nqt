Below are **complete TCS NQT-style solutions for each array problem**.
I kept the **coding style simple (loops + basic Python)** because this is the pattern generally used in the **TCS NQT coding section**.

Each problem includes:

* **Problem**
* **Example Input/Output**
* **Python Code**

---

# 1. Find the Smallest Number in an Array

### Example

Input

```
5
4 2 7 1 9
```

Output

```
1
```

### Code

```python
n = int(input("Enter size: "))
arr = list(map(int,input("Enter elements: ").split()))

smallest = arr[0]

for i in range(1,n):
    if arr[i] < smallest:
        smallest = arr[i]

print("Smallest element:",smallest)
```

---

# 2. Find the Largest Number in an Array

### Code

```python
n = int(input())
arr = list(map(int,input().split()))

largest = arr[0]

for i in range(1,n):
    if arr[i] > largest:
        largest = arr[i]

print("Largest element:",largest)
```

---

# 3. Second Smallest and Second Largest Element

### Code

```python
n = int(input())
arr = list(map(int,input().split()))

arr = list(set(arr))
arr.sort()

print("Second Smallest:",arr[1])
print("Second Largest:",arr[-2])
```

---

# 4. Reverse a Given Array

### Code

```python
n = int(input())
arr = list(map(int,input().split()))

print("Reversed array:")

for i in range(n-1,-1,-1):
    print(arr[i],end=" ")
```

---

# 5. Count Frequency of Each Element

### Code

```python
n = int(input())
arr = list(map(int,input().split()))

freq = {}

for num in arr:
    if num in freq:
        freq[num] += 1
    else:
        freq[num] = 1

for key,value in freq.items():
    print(key,"appears",value,"times")
```

---

# 6. Rearrange Array in Increasing-Decreasing Order

### Code

```python
n = int(input())
arr = list(map(int,input().split()))

arr.sort()

print("Rearranged array:")

for i in range(0,n//2):
    print(arr[i],end=" ")

for i in range(n-1,n//2-1,-1):
    print(arr[i],end=" ")
```

---

# 7. Calculate Sum of Elements

### Code

```python
n = int(input())
arr = list(map(int,input().split()))

total = 0

for i in arr:
    total += i

print("Sum:",total)
```

---

# 8. Rotate Array by K Elements

### Code

```python
n = int(input())
arr = list(map(int,input().split()))
k = int(input("Enter K: "))

k = k % n

rotated = arr[k:] + arr[:k]

print("Rotated array:",*rotated)
```

---

# 9. Average of All Elements

### Code

```python
n = int(input())
arr = list(map(int,input().split()))

total = 0

for num in arr:
    total += num

avg = total/n

print("Average:",avg)
```

---

# 10. Find Median of Array

### Code

```python
n = int(input())
arr = list(map(int,input().split()))

arr.sort()

if n%2==1:
    median = arr[n//2]
else:
    median = (arr[n//2] + arr[n//2-1]) / 2

print("Median:",median)
```

---

# 11. Remove Duplicates from Sorted Array

### Code

```python
n = int(input())
arr = list(map(int,input().split()))

result = [arr[0]]

for i in range(1,n):
    if arr[i] != arr[i-1]:
        result.append(arr[i])

print("Array after removing duplicates:",*result)
```

---

# 12. Remove Duplicates from Unsorted Array

### Code

```python
n = int(input())
arr = list(map(int,input().split()))

unique = list(set(arr))

print("Array without duplicates:",*unique)
```

---

# 13. Adding Element in Array

### Code

```python
arr = list(map(int,input().split()))

element = int(input("Enter element to add: "))

arr.append(element)

print("Updated array:",*arr)
```

---

# 14. Find All Repeating Elements

### Code

```python
n = int(input())
arr = list(map(int,input().split()))

freq = {}

for num in arr:
    freq[num] = freq.get(num,0)+1

print("Repeating elements:")

for key,value in freq.items():
    if value>1:
        print(key,end=" ")
```

---

# 15. Find Non-Repeating Elements

### Code

```python
n = int(input())
arr = list(map(int,input().split()))

freq = {}

for num in arr:
    freq[num] = freq.get(num,0)+1

print("Non repeating elements:")

for key,value in freq.items():
    if value==1:
        print(key,end=" ")
```

---

# 16. Find Symmetric Pairs

### Code

```python
pairs = [(1,2),(3,4),(2,1),(5,6)]

s = set()

print("Symmetric pairs:")

for a,b in pairs:
    if (b,a) in s:
        print((b,a),(a,b))
    else:
        s.add((a,b))
```

---

# 17. Maximum Product Subarray

### Code

```python
n = int(input())
arr = list(map(int,input().split()))

max_prod = arr[0]
min_prod = arr[0]
result = arr[0]

for i in range(1,n):

    if arr[i] < 0:
        max_prod,min_prod = min_prod,max_prod

    max_prod = max(arr[i],max_prod*arr[i])
    min_prod = min(arr[i],min_prod*arr[i])

    result = max(result,max_prod)

print("Maximum product:",result)
```

---

# 18. Replace Each Element by its Rank

### Code

```python
n = int(input())
arr = list(map(int,input().split()))

sorted_arr = sorted(arr)

rank = {}
r = 1

for num in sorted_arr:
    if num not in rank:
        rank[num] = r
        r += 1

print("Ranks:")

for num in arr:
    print(rank[num],end=" ")
```

---

# 19. Sort Elements by Frequency

### Code

```python
n = int(input())
arr = list(map(int,input().split()))

freq = {}

for num in arr:
    freq[num] = freq.get(num,0)+1

arr.sort(key=lambda x:(-freq[x],x))

print("Sorted by frequency:",*arr)
```

---

# 20. Left Rotation of Array

### Code

```python
n = int(input())
arr = list(map(int,input().split()))
k = int(input())

k = k % n

arr = arr[k:] + arr[:k]

print("Left rotated array:",*arr)
```

---

# 21. Right Rotation of Array

### Code

```python
n = int(input())
arr = list(map(int,input().split()))
k = int(input())

k = k % n

arr = arr[-k:] + arr[:-k]

print("Right rotated array:",*arr)
```

---

# 22. Equilibrium Index

### Code

```python
n = int(input())
arr = list(map(int,input().split()))

total = sum(arr)
left_sum = 0

for i in range(n):

    total -= arr[i]

    if left_sum == total:
        print("Equilibrium index:",i)
        break

    left_sum += arr[i]
```

---

# 23. Search an Element in Array

### Code

```python
n = int(input())
arr = list(map(int,input().split()))

key = int(input("Enter element to search: "))

for i in range(n):

    if arr[i] == key:
        print("Element found at index",i)
        break

else:
    print("Element not found")
```

---

# 24. Check if Array is Subset of Another Array

### Code

```python
arr1 = list(map(int,input("Enter array1: ").split()))
arr2 = list(map(int,input("Enter array2: ").split()))

if set(arr2).issubset(set(arr1)):
    print("Array2 is subset of Array1")
else:
    print("Array2 is not subset of Array1")
```

---


---

If you want, I can also give you the **Top 50 TCS NQT coding problems with the exact exam pattern** (very useful for your preparation since you're preparing for **TCS NQT**).
