# Project5
#Simple rock paper scissors number game in python
# Label program
# author:Bhagyashree
# Location:Pune
# Date:18/11/2020
#Simple rock paper scissors number game in python
#completed sucessfully


import random

#rock=r paper=p scissors=s
def gameWin(comp,you):
    if comp==you:
        return None
    elif comp=='r':
        if you=='p':
            return False
        elif you=='s':
            return True

    elif comp=='p':
        if you=='s':
            return False
        elif you=='r':
            return True

    elif comp=='s':
        if you=='r':
            return False
        elif you=='p':
            return True
print("comp turn:rock(r),paper(p) or scissors(s)?")
randNo=random.randint(1,3)
if randNo==1:
    comp='r'
elif randNo==2:
    comp='p'
elif randNo==3:
    comp='s'
you=input("your turn:rock(r),paper(p)or scissors(s)?")
a=gameWin(comp,you)
print(f"computer choose {comp}")
print(f"you choose {you}")
if a==None:
    print("the game is a tie!")
elif a:
    print("you win!")
else:
    print("you lose!")

'''#OUTPUT:
comp turn:rock(r),paper(p) or scissors(s)?
your turn:rock(r),paper(p)or scissors(s)?r
computer choose p
you choose r
you win!'''
