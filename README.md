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

import random

# Generate two lists of 10 random numbers between 10 and 30
list1 = [random.randint(10, 30) for _ in range(10)]
list2 = [random.randint(10, 30) for _ in range(10)]

# (i) Common numbers in both lists
common_numbers = list(set(list1) & set(list2))

# (ii) Unique numbers in both lists
unique_numbers = list(set(list1) ^ set(list2))

# (iii) Minimum in both lists
min_list1 = min(list1)
min_list2 = min(list2)

# (iv) Maximum in both lists
max_list1 = max(list1)
max_list2 = max(list2)

# (v) Sum of both lists
sum_list1 = sum(list1)
sum_list2 = sum(list2)

# Display results
print("List 1:", list1)
print("List 2:", list2)
print("\n(i) Common numbers:", common_numbers)
print("\n(ii) Unique numbers:", unique_numbers)
print("\n(iii) Minimum in List 1:", min_list1)
print("    Minimum in List 2:", min_list2)
print("\n(iv) Maximum in List 1:", max_list1)
print("    Maximum in List 2:", max_list2)
print("\n(v) Sum of List 1:", sum_list1)
print("    Sum of List 2:", sum_list2)

import random

# Generate a list of 100 random numbers between 100 and 900
numbers = [random.randint(100, 900) for _ in range(100)]

# (i) Count and print all odd numbers
odd_numbers = [num for num in numbers if num % 2 != 0]
print(f"Odd numbers ({len(odd_numbers)}): {odd_numbers}")

# (ii) Count and print all even numbers
even_numbers = [num for num in numbers if num % 2 == 0]
print(f"Even numbers ({len(even_numbers)}): {even_numbers}")

# (iii) Count and print all prime numbers
def is_prime(n):
    if n < 2:
        return False
    for i in range(2, int(n ** 0.5) + 1):
        if n % i == 0:
            return False
    return True

prime_numbers = [num for num in numbers if is_prime(num)]
print(f"Prime numbers ({len(prime_numbers)}): {prime_numbers}")

# Define the dictionary
D = {1: "One", 2: "Two", 3: "Three", 4: "Four", 5: "Five"}

# Open the file in write mode
with open("output.txt", "w") as file:
    # Iterate through the dictionary and write each key-value pair to the file
    for key, value in D.items():
        file.write(f"{key}, {value}\n")

print("Dictionary has been written to 'output.txt'")

# Define the list
L = ["One", "Two", "Three", "Four", "Five"]

# Open the file in write mode
with open("output.txt", "w") as file:
    # Iterate through the list and write each element and its length to the file
    for item in L:
        file.write(f"{item}, {len(item)}\n")

print("List elements and their lengths have been written to 'output.txt'")

import random
import string

# Function to generate a random string of a given length
def generate_random_string(length):
    characters = string.ascii_letters + string.digits + string.punctuation
    return ''.join(random.choices(characters, k=length))

# Open the file in write mode
with open("random_strings.txt", "w") as file:
    # Generate and write 100 random strings to the file
    for _ in range(100):
        length = random.randint(10, 15)  # Random length between 10 and 15
        random_string = generate_random_string(length)
        file.write(random_string + "\n")

print("100 random strings have been written to 'random_strings.txt'")

