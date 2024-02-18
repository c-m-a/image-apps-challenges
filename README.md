# Challenges

## Lambda Example

```python
fibonacci = lambda n: n if n <= 1 else fibonacci(n-1) + fibonacci(n-2)

# Example usage
for i in range(10):
    print(fibonacci(i), end=" ")
```

## Recursive function to calculate Fibonacci numbers

```python
def fibonacci(n):
    if n <= 1:
        return n
    else:
        return fibonacci(n-1) + fibonacci(n-2)

# Get user input for n
while True:
    try:
        n = int(input("Enter a non-negative integer (n): "))
        if n < 0:
            print("Please enter a non-negative integer.")
        else:
            break
    except ValueError:
        print("Invalid input. Please enter a valid integer.")

for i in range(n+1):
    print(f"Fibonacci({i}): {fibonacci(i)}")
```

## Lookup Table Example

```python
fruit_prices = {
    'apple': 1.0,
    'banana': 0.75,
    'orange': 1.25,
    'grape': 1.5,
    'kiwi': 2.0
}

# Function to get the price of a fruit from the lookup table
def get_fruit_price(fruit):
    return fruit_prices.get(fruit, "Not found")

# Example usage
fruit_to_lookup = 'banana'
price = get_fruit_price(fruit_to_lookup)

if price != "Not found":
    print(f"The price of {fruit_to_lookup} is ${price}")
else:
    print(f"{fruit_to_lookup} not found in the lookup table.")
```


## Q-Sort Example

```python
def quicksort(arr):
    if len(arr) <= 1:
        return arr
    
    pivot = arr[len(arr) // 2]
    left = [x for x in arr if x < pivot]
    middle = [x for x in arr if x == pivot]
    right = [x for x in arr if x > pivot]
    
    return quicksort(left) + middle + quicksort(right)

# Example usage
unsorted_array = [3, 6, 8, 10, 1, 2, 1]
sorted_array = quicksort(unsorted_array)

print("Unsorted array:", unsorted_array)
print("Sorted array:", sorted_array)
```
