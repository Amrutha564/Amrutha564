import random 
import time
player = input('Player Name: ')

print(f"Hey {player}! Let's play ROCK PAPER SCISSORS")

wins = 0
losses = 0
ties = 0
while True:
    print(f'{wins} Wins, {losses} Losses, {ties} Ties')
    time.sleep(1)
    user_choice = input('Enter your move: \n\tROCK: r\n\tPAPER: p\n\tSCISSORS: s\n\tQUIT: q\n')

    if user_choice == 'r':
        print('ROCK versus ', end='')
    elif user_choice == 'p':
        print('PAPER versus ', end='')
    elif user_choice == 's':
        print('SCISSORS versus ', end='')
    elif user_choice == 'q':
        exit()
    else:
           print('Enter valid input! Try again.') 
            time.sleep(3)
        
    if user_choice == 'r' or  user_choice == 'p' or user_choice == 's' :
        n = random.randint(1,3)

        if n == 1:
            comp_choice = 'r'
        elif n == 2:
            comp_choice = 'p'
        else:
            comp_choice = 's'

        if comp_choice == 'r':
            print('ROCK')
            time.sleep(1)
        elif comp_choice == 'p':
            print('PAPER')
            time.sleep(1)
        else:
            print('SCISSORS')
            time.sleep(1)
  
        if user_choice==comp_choice:
            print('Its a tie!')
            ties += 1
            time.sleep(1)
        elif  user_choice=='r' and comp_choice=='s':    
            print('You win!')
            wins += 1
            time.sleep(1)

        elif user_choice=='s'  and comp_choice=='p':
            print('You win!')
            wins += 1
            time.sleep(1)
        elif user_choice=='p'  and comp_choice=='r': 
            print('You win!')
            wins += 1
            time.sleep(1)
        else:
            print('Computer win!') 
            losses += 1      
            time.sleep(1)
