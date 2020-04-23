def guess_game():
    try:
        import random
        secret_number = random.randint(1, 10)
        guess_count = 0
        guess_limit = 3
        while guess_count < guess_limit:
            guess = int(input('\n'"I'm guessing a number in my head, lets see if you can guess it:"))
            guess_count += 1
            if guess == secret_number:
                print("you won! :)")
                break
        else:
            print('\n'"You lost! :(")

    except ValueError:
        print('\n''Please enter a number')


def play_again2():
    play_again = str(input('Do you wanna play again?:'))
    if play_again.lower() == 'yes':
        guess_game()
    elif play_again.lower() == 'no':
        print('\n'"Thanks for playing")
    else:
        print('\n'"please enter either yes or no")
        play_again2()


guess_game()
play_again2()


