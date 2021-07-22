import random

miles_traveled = 0
thirst = 0
camel_tiredness = 0
native_distance = -20
drinks_in_canteen = 3
done = False

print("Welcome to Camel!\nYou have stolen a camel to make your way across the great Mobi desert.\nThe natives want their camel back and are chasing you down!\nSurvive your desert trek and outrun the natives.")

while not(done):
    oasis = random.randrange(1,22)
    print("\nPick an option\nA. Drink from your canteen.\nB. Ahead moderate speed.\nC. Ahead full speed.\nD. Stop for the night\nE. Status check.\nQ. Quit")
    user_choice = input("Your choice? ")
    user_choice = user_choice.lower()

    if user_choice == "q":
        done = True

    elif user_choice == "e":
        print("Miles traveled:",miles_traveled, "\nDrinks in canteen:",drinks_in_canteen, "\nThe natives are", miles_traveled - native_distance, "miles behind you.")

    elif user_choice == "d":
        camel_tiredness = 0
        native_distance = native_distance + random.randrange(7,15)
        print("Your camel is well rested and happy!")

    elif user_choice == "c":
        current_miles = random.randrange(10,21)
        miles_traveled = miles_traveled + current_miles
        thirst = thirst + 1
        camel_tiredness = camel_tiredness + random.randrange(2,4)
        native_distance = native_distance + random.randrange(7,15)
        print("You traveled",current_miles,"miles!")

    elif user_choice == "b":
        current_miles = random.randrange(5,13)
        miles_traveled = miles_traveled + current_miles
        thirst = thirst + 1
        camel_tiredness = camel_tiredness + 1
        native_distance = native_distance + random.randrange(7,15)
        print("You traveled",current_miles,"miles!")

    elif user_choice == "a":
        print("You have quenched your thirst!")
        drinks_in_canteen = drinks_in_canteen - 1
        thirst = 0

    if drinks_in_canteen == 0:
            print("You have no more canteens!")

    if miles_traveled >= 100:
        print("You made it across the desert! You won!")
        done = True

    if native_distance >= miles_traveled and not done:
        print("The natives have caught up! Game over!")
        done = True

    if camel_tiredness > 8 and not done:
        print("Your camel is dead! Game over!")
        done = True
    elif 5 <= camel_tiredness <= 8 and not done:
        print("Your camel is getting tired")

    if thirst > 6 and not done:
        print("You died of thirst! Game over!")
        done = True
    elif 4 <= thirst <= 6 and not done:
        print("You are thirsty")

    if miles_traveled - native_distance < 15 and not done:
        print("The natives are getting close!")

    if oasis == 10 and not done:
        print("You found an oasis! Your thirst is quenched and canteens are filled!")
        thirst = 0
        drinks_in_canteens = 3
        camel_tiredness = 0

       
        
