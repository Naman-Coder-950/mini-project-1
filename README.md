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

# Initial sets
S1 = {10, 20, 30, 40, 50, 60}
S2 = {40, 50, 60, 70, 80, 90}

# (i) Add 55 and 66 to S1
S1.add(55)
S1.add(66)
print("After adding 55 and 66:", S1)

# (ii) Remove 10 and 30 from S1
S1.discard(10)  # discard() avoids KeyError if the element is not found
S1.discard(30)
print("After removing 10 and 30:", S1)

# (iii) Check if 40 is present in S1
if 40 in S1:
    print("40 is present in S1.")
else:
    print("40 is not present in S1.")

# (iv) Find the union of S1 and S2
union_set = S1.union(S2)
print("Union of S1 and S2:", union_set)

# (v) Find the intersection of S1 and S2
intersection_set = S1.intersection(S2)
print("Intersection of S1 and S2:", intersection_set)

# (vi) Find the difference S1 - S2
difference_set = S1.difference(S2)
print("Difference S1 - S2:", difference_set)

import random
import string

# Function to generate a random string of a given length
def generate_random_string(length):
    characters = string.ascii_letters + string.digits
    return ''.join(random.choices(characters, k=length))

# Generate and print 100 random strings with lengths between 6 and 8
for _ in range(100):
    length = random.randint(6, 8)
    print(generate_random_string(length))
    # Function to check if a number is prime
def is_prime(n):
    if n < 2:
        return False
    for i in range(2, int(n ** 0.5) + 1):
        if n % i == 0:
            return False
    return True

# Print all prime numbers between 600 and 800
for num in range(600, 801):
    if is_prime(num):
        print(num)

