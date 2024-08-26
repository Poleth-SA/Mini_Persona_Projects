#Calculator in Python

## Import Required Module
`code` ```python
import math

We import the math module to use mathematical functions like sqrt().

## Basic Arithmetic Functions

`code`def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y == 0:
        return "Error: Division by zero"
    return x / y

These functions perform basic arithmetic operations. The divide function includes a check for division by zero.

## Advanced Mathematical Functions

'code' def power(x, y):
    return x ** y

def square_root(x):
    if x < 0:
        return "Error: Cannot calculate square root of a negative number"
    return math.sqrt(x)
These functions handle more complex operations. The square root function checks for negative input.

## Main Calculator Function
'code' def calculator():
    while True:
        print("\nSelect operation:")
        print("1. Add")
        print("2. Subtract")
        print("3. Multiply")
        print("4. Divide")
        print("5. Power")
        print("6. Square Root")
        print("7. Exit")
        
        choice = input("Enter choice (1-7): ")
        
        if choice == '7':
            print("Exiting the calculator. Goodbye!")
            break
        
        if choice in ('1', '2', '3', '4', '5'):
            num1 = float(input("Enter first number: "))
            num2 = float(input("Enter second number: "))
            
            if choice == '1':
                print(f"{num1} + {num2} = {add(num1, num2)}")
            elif choice == '2':
                print(f"{num1} - {num2} = {subtract(num1, num2)}")
            elif choice == '3':
                print(f"{num1} * {num2} = {multiply(num1, num2)}")
            elif choice == '4':
                print(f"{num1} / {num2} = {divide(num1, num2)}")
            elif choice == '5':
                print(f"{num1} ^ {num2} = {power(num1, num2)}")
        
        elif choice == '6':
            num = float(input("Enter a number: "))
            print(f"Square root of {num} = {square_root(num)}")
        
        else:
            print("Invalid input. Please try again.")

This function creates a loop that continuously prompts the user for input until they choose to exit. It handles user input and calls the appropriate function based on the user's choice.

## Main Execution
'code' if __name__ == "__main__":
    calculator()
This ensures that the calculator() function is only run if the script is executed directly (not imported as a module).