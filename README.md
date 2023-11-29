# Task-1-codsoft-calculator
import math
print("*** SIMPLE CALCULATOR USING PYTHON ***")

# Defining required functions
def add(a, b):
    return a + b

def subtract(a, b):
    return a - b

def multiply(a, b):
    return a * b

def divide(a, b):
    if b != 0:
        return a / b
    else:
        return "Cannot be divided by zero"

while True:
    while True:

        # to get user input

        n1 = float(input("\nEnter the first number of your choice: "))
        n2 = float(input("Enter the second number of your choice: "))

        print("\n Select an operation you want to perform on calculator :")
        print("1) Addition")
        print("2) Subtraction")
        print("3) Multiplication")
        print("4) Division")

        choice = input("Enter your choice out of following (1/2/3/4): ")

        # To perform the calculation based on the user's choice
        if choice == '1':
            result = add(n1, n2)
        elif choice == '2':
            result = subtract(n1, n2)
        elif choice == '3':
            result = multiply(n1, n2)
        elif choice == '4':
            result = divide(n1, n2)
        else:
            result = "Sorry, you have chosen an 'Invalid Input'"

        # To display the result

        print(f"\n The result is: {result}")

        usr_input = input("Would you like to continue ? (Y/N) ").upper()

        if usr_input != 'Y':
            print("Thank You for using the calculator.")
            break
        else:
            print("Continuing the process, Restarting from beginning...\n")
            continue

    print("Exiting the program.")
    break
