# survey_5questions_scored
#This a customer service survey. Python
# This program is a customer satisfaction survey with 5 questions
# Each five answere customer enters is stored in a list called selections
# The function "checkanswers" determines if the customer has made a valid entry
# The program displays an error message and quits i invalid entry is made


# Deine the function called checkanswers

def checkanswers(answer) :
    try :
        answer = int(answer)
        if answer >= 1 and answer <= 5 :
            print('thank you for your answer!')
        elif answer < 1 or answer > 5 :
            print('Invalid entry')
            quit()
    except :
        print('Try again. Please enter a 1, 2 ,3, 4, or 5 Numerical values only ')
        quit()


## Code begins here

selections = list()

# Question 1
print('how would rate our SERVICE on a scale of 1 to 5? 5 being the highest.')
answer_1 = input('1\n2\n3\n4\n5\n: ')
print('You chose ', answer_1)

#call the function "checkanswers" to ensure valid user entry
#make sure or Q1 user entered numerical 1,2,3,4 or 5 otherwise quit

checkanswers(answer_1)

selections.append(answer_1)

# *********Question 2**************
print('how would rate our STAFF on a scale of 1 to 5? 5 being the highest.')
answer_2 = input('1\n2\n3\n4\n5\n: ')
print('You chose ', answer_2)


#call the function "checkanswers" to ensure valid user entry
#make sure or Q2 user entered numerical 1,2,3,4 or 5 otherwise quit
checkanswers(answer_2)

selections.append(answer_2)

# **********Question 3************
print('how would rate our FACIITIES on a scale of 1 to 5? 5 being the highest.')
answer_3 = input('1\n2\n3\n4\n5\n: ')
print('You chose ', answer_3)

#call the function "checkanswers" to ensure valid user entry
#make sure or Q3 user entered numerical 1,2,3,4 or 5 otherwise quit
checkanswers(answer_3)

selections.append(answer_3)



# **********Question 4***********
print('how would rate our HELP LINE on a scale of 1 to 5? 5 being the highest.')
answer_4 = input('1\n2\n3\n4\n5\n: ')
print('You chose ', answer_4)

#call the function "checkanswers" to ensure valid user entry
#make sure or Q4 user entered numerical 1,2,3,4 or 5 otherwise quit
checkanswers(answer_4)

selections.append(answer_4)

# **********Question5**********
print('how would rate our PAYMENT SYSTEM on a scale of 1 to 5. 5 being the highest.')
answer_5 = input('1\n2\n3\n4\n5\n')
print('You chose ', answer_5)

#call the function "checkanswers" to ensure valid user entry
#make sure or Q5 user entered numerical 1,2,3,4 or 5 otherwise quit
checkanswers(answer_5)

selections.append(answer_5)


## convert list values in selections to int from str
## int selection
##print(selections)
selections = [int(i) for i in selections]
print('Please review your answers: ', selections)
print("Number of survey questions you answered = ", (len(selections)))

# total the user selections
score = sum(selections)
# print(score)

# print message to user based on score

if score >= 22 :
    print('We will continually strive to meet your expectations!')
elif score < 22 and score >= 19 :
    print('Thank you for your input!')
elif score < 18 and score >= 16 :
    print('We are working to improve our service')
else :
    print('a customer service rep will contact you soon to discuss how we can improve ousr service')

print('Thank you for completing the survey!')
average = score / len(selections)
float(average)
print('Average rating = ', average)
