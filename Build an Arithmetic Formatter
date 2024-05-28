def arithmetic_arranger(problems, show_answers=False):
    if len(problems) > 5:
        return "Error: Too many problems."

    row_1 = ""
    row_2 = ""
    dashes = "" 
    answers = ""
    
    for problem in problems:
        parts = problem.split()
        #Categorizes user's input
        num_1 = parts[0]
        operator = parts[1]
        num_2 = parts[2]

        #Checks if user's inputs are valid 
        if not num_1.isdigit() or not num_2.isdigit():
            return "Error: Numbers must only contain digits."

        #Checks if user's operators are for addition and/or subtraction
        if operator not in ['+', '-']:
            return "Error: Operator must be '+' or '-'."
        
        #Checks if user's inputs numbers are correct length
        if len(num_1) > 4 or len(num_2) > 4:
            return "Error: Numbers cannot be more than four digits."

        #Performs this if input is valid
        width = max(len(num_1), len(num_2)) + 2
        row_1 += num_1.rjust(width) + "    "
        row_2 += operator + num_2.rjust(width - 1) + "    "
        dashes += '-' * width + "    "

        #Evaluates problems 
        if show_answers:
            if operator == '+':
                answer = str(int(num_1) + int(num_2))
            else:
                answer = str(int(num_1) - int(num_2))
            answers += answer.rjust(width) + "    "

    #Arranges problems according to requirements
    arranged_problems = row_1.rstrip() + '\n' + row_2.rstrip() + '\n' + dashes.rstrip()
    
    if show_answers:
        arranged_problems += '\n' + answers.rstrip()

    return arranged_problems

print(arithmetic_arranger(["32 + 698", "3801 - 2", "45 + 43", "123 + 49"], True))
