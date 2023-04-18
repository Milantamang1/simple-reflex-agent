# simple-reflex-agent
Artificial Intelligence(AI)

import random
import time
# Both room are empty initially
A = []
B = []


def clean_room():
    if len(A) != 0:
        print(f"Dirt on Room A = {A}")
        print("cleaning Room A")
        A.clear()
        print("Room A is cleaned")
        print("Moving to Room B\n")
    else:
        print("Room A is clean")
        print("Moving to Room B\n")

    time.sleep(5)

    if len(B) != 0:
        print(f"Dirt on Room B = {B}")
        print("cleaning Room B")
        B.clear()
        print("Room B is cleaned")
        print("Moving to Room A\n")
    else:
        print("Room B is clean")
        print("Moving to Room A\n")


while True:
    randRoom = random.randint(1, 2)
    randDirt = random.randint(1, 5)

    for i in range(randDirt):
        if randRoom == 1:
            A.append(i)
        else:
            B.append(i)

    print('\n')
    clean_room()
