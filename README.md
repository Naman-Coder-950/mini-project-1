# mini-project-1
PYTHON ASSIGNMENT
# Initial list
L = [11, 12, 13, 14]

# (i) Add 50 and 60 to L
L.append(50)
L.append(60)
print("After adding 50 and 60:", L)

# (ii) Remove 11 and 13 from L
L.remove(11)
L.remove(13)
print("After removing 11 and 13:", L)

# (iii) Sort L in ascending order
L.sort()
print("Sorted in ascending order:", L)

# (iv) Sort L in descending order
L.sort(reverse=True)
print("Sorted in descending order:", L)

# (v) Search for 13 in L
search_value = 13
if search_value in L:
    print(f"{search_value} found at index {L.index(search_value)}")
else:
    print(f"{search_value} not found in the list")

# (vi) Count the number of elements in L
print("Number of elements in L:", len(L))

# (vii) Sum all elements in L
print("Sum of all elements in L:", sum(L))

# (viii) Sum all odd numbers in L
odd_sum = sum(x for x in L if x % 2 != 0)
print("Sum of all odd numbers in L:", odd_sum)

# (ix) Sum all even numbers in L
even_sum = sum(x for x in L if x % 2 == 0)
print("Sum of all even numbers in L:", even_sum)

# (x) Sum all prime numbers in L
def is_prime(n):
    if n < 2:
        return False
    for i in range(2, int(n ** 0.5) + 1):
        if n % i == 0:
            return False
    return True

prime_sum = sum(x for x in L if is_prime(x))
print("Sum of all prime numbers in L:", prime_sum)

# (xi) Clear all elements in L
L.clear()
print("After clearing all elements:", L)

# (xii) Delete L
del L
print("L has been deleted.")

# Initial dictionary
D = {1: 5.6, 2: 7.8, 3: 6.6, 4: 8.7, 5: 7.7}

# (i) Add new entry with key=8 and value=8.8
D[8] = 8.8
print("After adding key=8 and value=8.8:", D)

# (ii) Remove key=2
if 2 in D:
    del D[2]
    print("After removing key=2:", D)
else:
    print("Key 2 not found in D.")

# (iii) Check if key=6 is present in D
if 6 in D:
    print("Key 6 is present in D.")
else:
    print("Key 6 is not present in D.")

# (iv) Count the number of elements in D
print("Number of elements in D:", len(D))

# (v) Add all the values in D
total_sum = sum(D.values())
print("Sum of all values in D:", total_sum)

# (vi) Update the value of key=3 to 7.1
if 3 in D:
    D[3] = 7.1
    print("After updating key=3 to value=7.1:", D)
else:
    print("Key 3 not found in D.")

# (vii) Clear all elements in D
D.clear()
print("After clearing all elements in D:", D)
