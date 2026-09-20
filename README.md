# calculator.py
op = input("Choose operation (+, -, *, /): ")

n = int(input("How many numbers? "))

nums = []

for i in range(n):

    nums.append(float(input(f"Enter number {i+1}: ")))
    
result = nums[0]
for num in nums[1:]:
    if op == '+':
        result += num

    elif op == '-':
        result -= num
        
    elif op == '*':
        result *= num
        
    elif op == '/':
        if num == 0:
            print("Error! Division by zero.")
            break
        result /= num
        
    else:
        print("Invalid operation")
        break

print("Result:", result)
