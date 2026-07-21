# Week1_Budget_Tracker_hollymiller

monthly_income = float(input("Enter your monthly income: "))

expenses = []
for i in range(1, 4):
    while True:
        try:
            expense = float(input(f"Enter expense {i}: "))
            expenses.append(expense)
            break
        except ValueError:
            print("Invalid input. Please enter a number for the expense.")

total_expenses = sum(expenses)
remaining_budget = monthly_income - total_expenses

print(f"\nRemaining budget: ${remaining_budget:.2f}")

if remaining_budget < 0:
    print(f"Warning: You are over budget by ${abs(remaining_budget):.2f}!")
