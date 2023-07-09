# TextbasedAdventureGame.
import time

def print_delay(text, delay=1):
    print(text)
    time.sleep(delay)

def intro():
    print_delay("You find yourself standing in a dark forest.")
    print_delay("In front of you, there are two paths. One leads to a mysterious cave and the other leads to a hidden beach.")
    print_delay("Which path will you choose? (1) Cave or (2) Beach")

def cave():
    print_delay("You cautiously enter the cave.")
    print_delay("It is very dark and you can barely see anything.")
    print_delay("You hear a faint growl and realize there's a bear sleeping in the cave!")
    print_delay("What would you do? (1) Try to sneak past the bear or (2) Retreat quietly?")

    choice = input("Enter your choice (1 or 2): ")
    if choice == '1':
        print_delay("You try to sneak past the bear...")
        print_delay("But it wakes up and attacks you! Game over.", 2)
    elif choice == '2':
        print_delay("You retreat quietly and leave the cave.")
        print_delay("You return to the forest.")
        play_game()
    else:
        print_delay("Invalid input. Please enter a valid choice.", 1)
        cave()

def beach():
    print_delay("You arrive at the hidden beach.")
    print_delay("The beach is deserted, and the waves crash gently on the shore.")
    print_delay("You notice a shiny object glimmering in the sand.")
    print_delay("As you approach, you realize it's a treasure chest!")
    print_delay("You can (1) try to open it or (2) ignore it and keep exploring the beach.")

    choice = input("Enter your choice (1 or 2): ")
    if choice == '1':
        print_delay("You try to open the treasure chest...")
        print_delay("Congratulations! You found the hidden treasure. You win!", 2)
    elif choice == '2':
        print_delay("You decide to ignore the treasure chest.")
        print_delay("You continue exploring the beach.")
        play_game()
    else:
        print_delay("Invalid input. Please enter a valid choice.", 1)
        beach()

def play_game():
    intro()

    choice = input("Enter your choice (1 or 2): ")
    if choice == '1':
        cave()
    elif choice == '2':
        beach()
    else:
        print_delay("Invalid input. Please enter a valid choice.", 1)
        play_game()

play_game()
