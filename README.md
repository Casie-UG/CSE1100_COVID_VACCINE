# CSE1100_COVID_VACCINE
#Program intro-cassie

intro = 'WELCOME TO COV-AL! \nThis program is a data collection and analysis model.\nIt collects patient demographics and medical history, then suggests a suitable vaccine based on the info you enter. \nPlease enter data as truthfully and as accurately as possible for best results.'
intro = intro.center(300)
print (intro,'\n\n')

dose = input ('Lets get started.\nIs this your FIRST or SECOND dose of the vaccine?\n')
dose = dose.casefold() #makes it so that the input will not be case sensitive

first_txt = ['first','1st'] #creates a list of text that will be taken as valid if user choses "first" 
second_txt = ['second','2nd'] #creates a list of text that will be taken as valid if user chooses "second"

if any(x in dose for x in first_txt): 
   print ('You have selected that this is your First dose\n') 
   L_name = input ('Please enter your LAST name\n')
   F_name = input ('Please enter your FIRST name\n')
   P_address = input ('Please enter your current address\n') 
elif any(x in dose for x in second_txt):
   print ('You have selected that this is your SECOND dose')
else: print ('Invalid input, please try again') 
