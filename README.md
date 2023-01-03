# Calculator-app-Python


The user will choose between the 4 math operations (Add, Subtract, Multiply and Divide)

The application will ask for 2 numbers

Display the result

The application will ask again if the user wants to try again

Use the appropriate Exception (ex: Invalid input such as text and zero division)

----------------------------------------------------------------------------------------------

def calculator():

    operations = ["+", "-", "*", "/"]


    while True:
    
        Menu()
        
        Selection = input("Your choice: ")


        if Selection not in operations:
        
            print("Invalid Input!")
            
        else:
        
            try:
            
                firstNumber = float(input("first number: "))
                
                secondNumber = float(input("Second number: "))
                
                result = 0
                

                if Selection == "+":
                
                    result = firstNumber + secondNumber
                    
                    print("Answer: ", result)
                    
                elif Selection == "-":
                
                    result = firstNumber - secondNumber
                    
                    print("Answer: ", result)
                    
                elif Selection == "*":
                
                    result = firstNumber * secondNumber
                    
                    print("Answer: ", result)
                    
                elif Selection == "/":
                
                    if secondNumber == 0:
                    
                        print("Error! Cannot divide by zero")
                        
                    else:
                    
                        result = firstNumber / secondNumber
                        
                        print("Answer: ", result)
                        
            except:
            
                print("Invalid Input! Only numbers are allowed.")
                
        user = input("\nDo you want to try again? (y/n) ")
        
        if user == "n":
        
            print("\nProgram End ")
            
            break


def Menu():

    print()
    
    print("========= Menu ==========")
    
    print('Type "+" Addition       |')
    
    print('Type "-" Subtraction    |')
    
    print('Type "*" Multiplication |')
    
    print('Type "/" Division       |')
    
    print("=========================")
    
    print()


if __name__ == "__main__":

    calculator()
