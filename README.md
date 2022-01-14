import random

top_of_range = input("Masukkan Angka: ")

if top_of_range.isdigit():
    top_of_range = int(top_of_range)

    if top_of_range <= 0:
        print('Masukkan Angka Lebih Dari 0.')
        quit()
else:
    print('Masukkan Angka Lagi.')
    quit()

random_number = random.randint(0, top_of_range)
guesses = 0

while True:
    guesses += 1
    user_guess = input("Tebaklah: ")
    if user_guess.isdigit():
        user_guess = int(user_guess)
    else:
        print('Masukkan Angka Lagi.')
        continue

    if user_guess == random_number:
        print("Bener Ya Gaes Ya")
        break
    elif user_guess > random_number:
        print("Terlalu Besar Angkanya, Kebawah dikit")
    else:
        print("Dikit Lagi Cuy")

print("Tebakan Benar Dalam", guesses, "Tebakan")
