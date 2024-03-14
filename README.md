# Games
#Rock Paper Scissor
import random #we use import random here
# program for rock paper scissor
print('Winning rules of the game ROCK PAPER SCISSORS are :\n'
      + "Rock vs Paper -> Paper wins \n"
      + "Rock vs Scissors -> Rock wins \n"
      + "Paper vs Scissors -> Scissor wins \n")
while True:
    print('enter your choice:\n 1-rock \n 2-paper \n 3-scissor')
    choice = int(input("enter your choice : "))

    while choice > 3 or choice < 1:
        choice = int(input("Please enter correct choice \n"))

    if choice == 1:
        choice_name = 'Rock'
    elif choice == 2:
        choice_name = 'Paper'
    else :
        choice_name = 'scissor'

    print("Your choice is :  ", choice_name) #now computer's turn
    print("Now it's computer's turn")

    comp_choice = random.randint(1,3)
    while comp_choice == choice:
        comp_choice == random.randint(1,3)

    if comp_choice == 1:
        comp_choice_name = 'rocK'
    elif comp_choice == 2:
        comp_choice_name = 'papeR'
    else :
        comp_choice_name = 'scissoR'

    print("computer's choice is: ", comp_choice_name)
    print("choice_name vs comp_choice_name")

    if choice == comp_choice:
        print('Its a Draw',end="")
        result="DRAW"

    # condition for winning   
    #    
    if (choice==1 and comp_choice==2):
        print('paper wins =>',end="")
        result='papeR'

    elif (choice==2 and comp_choice==1):
        print('paper wins =>',end="")
        result='Paper'        
       
    if (choice==1 and comp_choice==3):
        print('Rock wins =>\n',end= "")
        result='Rock'

    elif (choice==3 and comp_choice==1):
        print('Rock wins =>\n',end= "")
        result='rocK'
         
    if (choice==2 and comp_choice==3):
        print('Scissors wins =>',end="")
        result='scissoR'

    elif (choice==3 and comp_choice==2):
        print('Scissors wins =>',end="")
        result='Rock'

     # Printing either user or computer wins or draw
    if result == 'DRAW':
        print("<== Its a tie ==>")

    if result == choice_name:
        print("<== User wins ==>")

    else:
        print("<== Computer wins ==>")

    print("Do you want to play again? (Y/N)")
    # if user input n or N then condition is True
    ans = input().lower()
    if ans =='n':
        break
# after coming out of the while loop
# we print thanks for playing
print("thanks for playing")

