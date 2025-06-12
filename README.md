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
