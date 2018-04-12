import random

def main():
    #declare variables
    counter = 0
    studentName = "NO NAME"
    averageRight = 0.0
    right = 0.0
    number1 = 0
    number2 = 0
    answer = 0.0


    studentName = getName()

    while counter <10:
        number1, number2 = getNumbers()
        #getanswer
        answer = getAnswer(number1, number2, answer)
    
        #checkAnswer
        right = checkAnswer(number1, number2, answer, right)
        counter = counter + 1
    #function getAverage
    #print information

def getName():
    studentName = input("Enter Student Name ")
    return studentName

def getNumbers():
    number1 = random.randint(1, 500)
    number2 = random.randint(1, 500)
    return number1, number2

def getAnswer(number1, number2, answer):
    print("what is the answer to the following equation")
    print(number1)
    print("+")
    print(number2)
    answer = int(input("what is the sum? "))
    return number1, number2, answer

def checkAnswer(number1, number2, answer, right):
    if answer == number1 + number2:
        print("right")
    else:
        print("wrong")
    return number1, number2, answer, right

main()
