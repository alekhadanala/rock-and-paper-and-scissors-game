# rock-and-paper-and-scissors-game
import random
userscore=0
computerscore=0
print("welcome to the game")

while True:
    print("\nchoose: rock, paper, scissors ")
    user=input("your choice:....").lower()
    if user not in ["rock","paper","scissors"]:
        print("invalid choice")
        continue
    computer=random.choice(["rock","paper","scissors"])
    print("computer choice:...",computer)

    if user==computer:
        print("it is tie")
    elif (user=="rock"and computer=="scissors")or(user=="paper" and computer=="rock")or(user=="scissors" and computer=="paper"):
        print("you won")
        userscore=userscore+1
    else:
        print("computer wons")
        computerscore=computerscore+1
        print("\n score:")
        print("you:",userscore)
        print("computer:..",computerscore)

        once_again=input(" play again?(yes /no)").lower()
        if once_again !="yes:":
            print("thanks")
            break
