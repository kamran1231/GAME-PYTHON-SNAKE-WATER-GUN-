# GAME-PYTHON-SNAKE-WATER-GUN-

import random

print('WELCOME TO MY SNAKE WATER GUN')
print('you have only 10 chances to this game')
print('Please input \n snake  \t or \t water \t or \t gun')

i = 0
user_point = 0
computer_point = 0
Tie = 0

chances = 10
for user in range(chances):
    list = ['snake','water','gun']
    choice = random.choice(list)

    while i < 10:
        i += 1
        user = input('enter your choice: ')
        if user == 'snake' and choice == 'water':
            print('Congrstulations you Won!')
            user_point += 1
            print('you have chaces left:',chances - i)

        elif user == 'snake' and choice == 'gun':
            print('you Loss!')
            computer_point += 1
            print('you have chaces left:',chances - i)

        elif user == 'snake' and choice == 'snake':
            print('Match Tie!')
            Tie += 1
            print('you have chaces left:',chances - i)

        elif user == 'gun' and choice == 'water':
            print('you Lost!')
            computer_point += 1
            print('you have chaces left:',chances - i)

        elif user == 'gun' and choice == 'snake':
            print('Congratulations You Won!')
            user_point += 1
            print('you have chaces left:', chances - i)

        elif user == 'gun' and choice == 'gun':
            print('Match tie!')
            Tie += 1
            print('you have chaces left:', chances - i)

        elif user == 'water' and choice == 'water':
            print('Match tie!')
            Tie += 1
            print('you have chaces left:', chances - i)

        elif user == 'water' and choice == 'gun':
            print('Congratulations You Won!')
            user_point += 1
            print('you have chaces left:', chances - i)

        elif user == 'water' and choice == 'snake':
            print('you Lost!')
            computer_point += 1
            print('you have chaces left:',chances - i)
            break

if chances == 10:
    print('GAME OVER')
    print('user point: ',user_point)
    print('computer point: ',computer_point)

    if user_point > computer_point:
        print('user won this battel:')
    elif user_point < computer_point:
        print('computer won this battel:')
    elif user_point == computer_point:
        print('Match Tied:')
print('Thankx for playing my GAME:')
