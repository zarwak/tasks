# 1. Find the oldest of three ages
def find_oldest(age1, age2, age3):
    return max(age1, age2, age3)

# 2. Convert Celsius to Fahrenheit
def celsius_to_fahrenheit(celsius):
    return (celsius * 9/5) + 32

# 3. Swap two numbers
def swap_numbers(num1, num2):
    return num2, num1

# 4. Sum of three digits
def sum_of_three_digits(num):
    return sum(int(digit) for digit in str(num))

# 5. Reverse a four-digit number and check if reverse is true
def reverse_and_check(number):
    reverse_num = int(str(number)[::-1])
    return reverse_num, reverse_num == number

# 6. Check if a number is odd or even
def is_odd_or_even(number):
    return "Even" if number % 2 == 0 else "Odd"

# 7. Check if a year is a leap year
def is_leap_year(year):
    return year % 4 == 0 and (year % 100 != 0 or year % 400 == 0)

# 8. Find the Euclidean distance between two coordinates
import math
def euclidean_distance(x1, y1, x2, y2):
    return math.sqrt((x2 - x1)**2 + (y2 - y1)**2)

# 9. Check if three angles can form a triangle
def can_form_triangle(angle1, angle2, angle3):
    return angle1 + angle2 + angle3 == 180

# 10. Determine if there's a profit or loss
def profit_or_loss(cost_price, selling_price):
    if selling_price > cost_price:
        return "Profit"
    elif selling_price < cost_price:
        return "Loss"
    else:
        return "No profit, no loss"

# 11. Calculate simple interest
def simple_interest(principal, rate, time):
    return (principal * rate * time) / 100
# 11. Calculate simple interest
def simple_interest(principal, rate, time):
    return (principal * rate * time) / 100

# 12. Find the volume of a cylinder and calculate the cost for milk
def cylinder_volume_and_cost(radius, height, cost_per_litre=40):
    volume = math.pi * radius**2 * height  # Volume in cubic units
    volume_in_litres = volume / 1000  # Convert cubic centimeters to liters (assuming dimensions in cm)
    cost = volume_in_litres * cost_per_litre
    return volume, cost

# 13. Check if a number is divisible by 3 and 6
def divisible_by_3_and_6(number):
    return number % 3 == 0 and number % 6 == 0

# 14. Function for angle between hour and minute hand
def angle_between_hour_minute(hour, minute):
    if hour >= 12:
        hour -= 12
    hour_angle = (360 / 12) * (hour + minute / 60)
    minute_angle = (360 / 60) * minute
    angle = abs(hour_angle - minute_angle)
    return min(angle, 360 - angle)

# 15. Function to check overlapping rectangles
def overlapping_rectangles(l1, r1, l2, r2):
    if l1[0] >= r2[0] or l2[0] >= r1[0]:
        return False
    if r1[1] >= l2[1] or r2[1] >= l1[1]:
        return False
    return True

# 16. Determine weather based on temperature and humidity
def determine_weather(temperature, humidity):
    if temperature >= 30:
        if humidity >= 90:
            return "Hot and Humid"
        else:
            return "Hot"
    else:
        if humidity >= 90:
            return "Cool and Humid"
        else:
            return "Cool"

# 17. Add the square of three digits
def sum_of_squares_of_digits(digit1, digit2, digit3):
    return digit1**2 + digit2**2 + digit3**2

# 18. Check if a number is an Armstrong number
def is_armstrong_number(number):
    digits = [int(d) for d in str(number)]
    power = len(digits)
    return number == sum(d**power for d in digits)

# 19. Check if a 4-digit number is a narcissist number
def is_narcissist_number(number):
    if len(str(number)) != 4:
        return False
    return is_armstrong_number(number)

# 20. Calculate in-hand salary after deductions
def in_hand_salary(salary):
    hra = 0.1 * salary
    da = 0.05 * salary
    pf = 0.03 * salary
    taxable_income = salary - (hra + da + pf)

    if salary <= 100000:
        tax = 0
    elif salary <= 1000000:
        tax = 0.1 * (taxable_income - 500000)
    elif salary <= 2000000:
        tax = 0.2 * (taxable_income - 1000000)
    else:
        tax = 0.3 * (taxable_income - 2000000)

    in_hand = salary - (hra + da + pf + tax)
    return in_hand
# 21. Menu-driven program for conversions
def conversion_menu():
    while True:
        print("1. cm to ft")
        print("2. km to miles")
        print("3. USD to INR")
        print("4. Exit")
        choice = int(input("Enter your choice: "))

        if choice == 1:
            cm = float(input("Enter cm: "))
            ft = cm / 30.48
            print(f"{cm} cm = {ft} ft")
        elif choice == 2:
            km = float(input("Enter km: "))
            miles = km * 0.621371
            print(f"{km} km = {miles} miles")
        elif choice == 3:
            usd = float(input("Enter USD: "))
            inr = usd * 82.50  # assuming exchange rate of 82.5 INR per USD
            print(f"{usd} USD = {inr} INR")
        elif choice == 4:
            break
        else:
            print("Invalid choice, please try again.")

# 22. Find the number of dogs and chickens given total heads and legs
def find_animals(heads, legs):
    for chickens in range(heads + 1):
        dogs = heads - chickens
        if chickens * 2 + dogs * 4 == legs:
            return chickens, dogs
    return "No solution"

# 23. Swap numbers
def swap_numbers(num1, num2):
    return num2, num1

# 24. Sum of first n natural numbers
def sum_of_n_numbers(n):
    return n * (n + 1) / 2

# 25. Multiply two numbers without using the * operator
def multiply_without_asterisk(num1, num2):
    result = 0
    for _ in range(abs(num2)):
        result += num1
    return result if num2 > 0 else -result

# 26. Find the factorial of a given number
def factorial(n):
    if n == 0 or n == 1:
        return 1
    return n * factorial(n - 1)

# 27. Print the first 25 odd numbers
def print_first_25_odd_numbers():
    odd_numbers = [i for i in range(1, 50, 2)]
    return odd_numbers

# 28. Check if a number is prime
def is_prime(number):
    if number <= 1:
        return False
    for i in range(2, int(math.sqrt(number)) + 1):
        if number % i == 0:
            return False
    return True

# 29. Print all Armstrong numbers in the range 100-1000
def print_armstrong_numbers():
    armstrong_numbers = []
    for num in range(100, 1000):
        if is_armstrong_number(num):
            armstrong_numbers.append(num)
    return armstrong_numbers

# 30. Calculate population for the last 10 years
def population_growth(initial_population, growth_rate=0.1, years=10):
    population = initial_population
    populations = []
    for year in range(1, years + 1):
        populations.append(f"{years - year + 1}th year - {int(population)}")
        population /= (1 + growth_rate)
    return populations

# 31. Print all unique combinations of 1, 2, 3, 4
def unique_combinations():
    from itertools import permutations
    combinations = list(permutations([1, 2, 3, 4]))
    return combinations

# 32. Find the HCF (GCD) of two numbers
def find_hcf(num1, num2):
    while num2:
        num1, num2 = num2, num1 % num2
    return num1

# 33. Find the LCM of two numbers
def find_lcm(num1, num2):
    hcf = find_hcf(num1, num2)
    return abs(num1 * num2) // hcf

# 34. Print first 25 prime numbers
def print_first_25_primes():
    primes = []
    num = 2
    while len(primes) < 25:
        if is_prime(num):
            primes.append(num)
        num += 1
    return primes

# 35. Print the first 20 numbers of a Fibonacci series
def fibonacci_series(n=20):
    fib_series = [0, 1]
    while len(fib_series) < n:
        fib_series.append(fib_series[-1] + fib_series[-2])
    return fib_series[:n]

# 36. Calculate compound interest
def compound_interest(principal, rate, time, n=1):
    amount = principal * (1 + rate/(100*n))**(n*time)
    return amount - principal

# 37. Compute the value of n + nn + nnn
def compute_n_nn_nnn(n):
    return n + int(f"{n}{n}") + int(f"{n}{n}{n}")

# 38. Find the number of digits in a number
def number_of_digits(num):
    return len(str(num))

# 39. Print all factors of a given number
def factors_of_number(num):
    return [i for i in range(1, num + 1) if num % i == 0]
# 40. Find the reverse of a number
def reverse_number(num):
    return int(str(num)[::-1])

# 41. Print the pattern:
# *
# **
# ***
# ****
# *****
def pattern_1(rows=5):
    for i in range(1, rows + 1):
        print("*" * i)

# 42. Print the pattern:
# *
# **
# ***
# **
# *
def pattern_2(rows=3):
    for i in range(1, rows + 1):
        print("*" * i)
    for i in range(rows - 1, 0, -1):
        print("*" * i)

# 43. Print the pyramid pattern:
#        *
#      * * *
#    * * * * *
#   * * * * * * *
# * * * * * * * * *
def pyramid_pattern(rows=5):
    for i in range(rows):
        print(" " * (rows - i - 1) + "* " * (2 * i + 1))

# 44. Print the pattern:
# 1
# 1 2 1
# 1 2 3 2 1
# 1 2 3 4 3 2 1
# 1 2 3 4 5 4 3 2 1
def number_pattern(rows=5):
    for i in range(1, rows + 1):
        for j in range(1, i + 1):
            print(j, end=" ")
        for j in range(i - 1, 0, -1):
            print(j, end=" ")
        print()
# 45. Print the pattern:
# 1
# 2 3
# 4 5 6
# 7 8 9 10
def number_pattern_2():
    num = 1
    for i in range(1, 5):
        for j in range(i):
            print(num, end=" ")
            num += 1
        print()

# 46. Calculate the sum of the series: 1/1! + 2/2! + ... + n/n!
import math
def sum_series_1(n):
    total = 0
    for i in range(1, n + 1):
        total += i / math.factorial(i)
    return total

# 47. Calculate the sum of the series: 1 + x^2/2 + x^3/3 + ... + x^n/n
def sum_series_2(x, n):
    total = 1
    for i in range(2, n + 1):
        total += (x ** i) / i
    return total

# 48. Calculate the natural logarithm series sum
def natural_log_series(x, terms=7):
    total = 0
    for i in range(1, terms + 1):
        term = ((x - 1) / x) ** i / i
        total += term
    return total

# 49. Accept numbers until the user enters Zero, then display the sum and average
def sum_and_average():
    total = 0
    count = 0
    while True:
        num = float(input("Enter a number (0 to stop): "))
        if num == 0:
            break
        total += num
        count += 1
    if count > 0:
        average = total / count
        return total, average
    return 0, 0

# 50. Simplify a fraction
def simplify_fraction(numerator, denominator):
    def gcd(a, b):
        while b:
            a, b = b, a % b
        return a

    common_divisor = gcd(numerator, denominator)
    return numerator // common_divisor, denominator // common_divisor

# 51. Find the length of a string without using len()
def string_length(s):
    length = 0
    for _ in s:
        length += 1
    return length

# 52. Extract username from an email
def extract_username(email):
    return email.split('@')[0]

# 53. Count the frequency of a particular character in a string
def char_frequency(s, char):
    frequency = 0
    for c in s:
        if c == char:
            frequency += 1
    return frequency
# 54. Find the index position of a particular character in another string.
def find_index(s, char):
    return s.find(char)

# 55. Count the number of vowels in a string provided by the user.
def count_vowels(s):
    vowels = 'aeiouAEIOU'
    return sum(1 for char in s if char in vowels)

# 56. Remove a particular character from a string.
def remove_char(s, char):
    return s.replace(char, '')

# 57. Check whether a given string is a palindrome.
def is_palindrome(s):
    return s == s[::-1]

# 58. Remove all the duplicates from a list.
def remove_duplicates(lst):
    return list(set(lst))

# 59. Convert a string to title case without using the title().
def to_title_case(s):
    return ' '.join(word.capitalize() for word in s.split())

# 60. Find the max item from a list without using the max function.
def find_max(lst):
    max_item = lst[0]
    for item in lst:
        if item > max_item:
            max_item = item
    return max_item

# 61. Reverse a list.
def reverse_list(lst):
    return lst[::-1]

# 62. Search a given number from a list.
def search_number(lst, num):
    return num in lst

# 63. Create a new list where each item is the square of the item of the old list.
def square_list(lst):
    return [x**2 for x in lst]

# 64. Reverse words of a given string.
def reverse_words(s):
    return ' '.join(s.split()[::-1])

# 65. Count the number of words in a given string.
def count_words(s):
    return len(s.split())

# 66. Check if a list is in ascending order or not.
def is_ascending(lst):
    return lst == sorted(lst)

# 67. Create two lists from a given list: one with odd numbers, the other with even numbers.
def split_odd_even(lst):
    odd = [x for x in lst if x % 2 != 0]
    even = [x for x in lst if x % 2 == 0]
    return odd, even

# 68. Merge two lists without using the + operator.
def merge_lists(lst1, lst2):
    for item in lst2:
        lst1.append(item)
    return lst1

# 69
def replace_item(lst, old_item, new_item):
    return [new_item if item == old_item else item for item in lst]

# 70
def flatten_2d_list(lst):
    return [item for sublist in lst for item in sublist]
# 71. Perform union and intersection on 2 given lists.
def union_and_intersection(lst1, lst2):
    union = list(set(lst1) | set(lst2))
    intersection = list(set(lst1) & set(lst2))
    return union, intersection

# 72. Find the max item of each row of a matrix.
def max_of_each_row(matrix):
    return [max(row) for row in matrix]

# 73. Convert an integer to a string.
def int_to_string(n):
    return str(n)

# 74. Print the shape of a matrix.
def matrix_shape(matrix):
    rows = len(matrix)
    cols = len(matrix[0]) if rows > 0 else 0
    return rows, cols

# 75. Check if you can perform matrix multiplication on 2 matrices.
def can_multiply_matrices(matrix1, matrix2):
    return len(matrix1[0]) == len(matrix2)

# 76. Perform matrix multiplication on 2 matrices.
def multiply_matrices(matrix1, matrix2):
    if not can_multiply_matrices(matrix1, matrix2):
        return "Matrices cannot be multiplied."
    result = [[sum(a*b for a, b in zip(row, col)) for col in zip(*matrix2)] for row in matrix1]
    return result

# 77. Sort a given unsorted list without using any built-in function.
def bubble_sort(lst):
    n = len(lst)
    for i in range(n):
        for j in range(0, n-i-1):
            if lst[j] > lst[j+1]:
                lst[j], lst[j+1] = lst[j+1], lst[j]
    return lst

# 78. Find the most used word in a Bollywood song (assuming song is provided as a string).
def most_used_word(song):
    words = song.split()
    word_count = {}
    for word in words:
        word_count[word] = word_count.get(word, 0) + 1
    return max(word_count, key=word_count.get)

# 79. Convert a list of numbers from 1 to 10 into a dictionary where keys are the numbers and values are their squares.
def list_to_dict(lst):
    return {x: x**2 for x in lst}

# 80. Merge two given dictionaries.
def merge_dictionaries(dict1, dict2):
    merged = dict1.copy()
    merged.update(dict2)
    return merged

# 81. Swap the key-value pair for max and min values in a dictionary.
def swap_min_max(dictionary):
    min_key = min(dictionary, key=dictionary.get)
    max_key = max(dictionary, key=dictionary.get)
    dictionary[min_key], dictionary[max_key] = dictionary[max_key], dictionary[min_key]
    return dictionary

# 82. Find histogram of a given set of numbers with user-defined bin size.
def histogram(numbers, bin_size):
    hist = {}
    for number in numbers:
        bin_key = (number // bin_size) * bin_size
        hist[bin_key] = hist.get(bin_key, 0) + 1
    return hist

# 83. Count the number of upper case and lower case characters in a string.
def count_case(s):
    case_count = {'upper': 0, 'lower': 0}
    for char in s:
        if char.isupper():
            case_count['upper'] += 1
        elif char.islower():
            case_count['lower'] += 1
    return case_count

# 84. Convert a list of strings to numerical vectors using the Bag of Words model.
def bag_of_words(strings):
    words = set()
    for string in strings:
        words.update(string.split())
    words = sorted(words)

    vectors = []
    for string in strings:
        vector = [0] * len(words)
        for word in string.split():
            if word in words:
                vector[words.index(word)] += 1
        vectors.append(vector)

    return vectors

# 85. Perform login and registration using a menu driven program.
def login_registration():
    users = {}

    def register():
        username = input("Enter a new username: ")
        if username in users:
            print("Username already exists.")
        else:
            password = input("Enter a new password: ")
            users[username] = password
            print("Registration successful.")

    def login():
        username = input("Enter your username: ")
        if username in users:
            password = input("Enter your password: ")
            if users[username] == password:
                print("Login successful.")
            else:
                print("Incorrect password.")
        else:
            print("Username not found.")

    while True:
        choice = input("Choose an option: 1. Register 2. Login 3. Exit: ")
        if choice == '1':
            register()
        elif choice == '2':
            login()
        elif choice == '3':
            break
        else:
            print("Invalid option. Please try again.")
import math

def nearest_neighbor(neighbors, point):
    def euclidean_distance(p1, p2):
        return math.sqrt((p1[0] - p2[0])**2 + (p1[1] - p2[1])**2)

    nearest = None
    min_distance = float('inf')

    for neighbor in neighbors:
        distance = euclidean_distance(neighbor, point)
        if distance < min_distance:
            min_distance = distance
            nearest = neighbor

    return nearest

def factorial(n):
    # Base case: factorial of 0 or 1 is 1
    if n <= 1:
        return 1
    # Recursive case
    return n * factorial(n - 1)


