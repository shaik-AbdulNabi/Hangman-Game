import random

def choose_word():
    words = ['python', 'hangman', 'program', 'computer', 'science', 'engineering', 'keyboard', 'monitor']
    return random.choice(words)

def display_word(word, guessed_letters):
    displayed_word = ''
    for letter in word:
        if letter in guessed_letters:
            displayed_word += letter + ' '
        else:
            displayed_word += '_ '
    return displayed_word.strip()

def hangman():
    print("Welcome to Hangman!")
    word = choose_word()
    guessed_letters = []
    incorrect_guesses = 0
    max_incorrect_guesses = 6
    
    while incorrect_guesses < max_incorrect_guesses:
        print("\nWord to guess:", display_word(word, guessed_letters))
        guess = input("Guess a letter: ").lower()
        
        if len(guess) != 1 or not guess.isalpha():
            print("Please enter a single letter.")
            continue
        
        if guess in guessed_letters:
            print("You already guessed that letter!")
            continue
        
        guessed_letters.append(guess)
        
        if guess in word:
            print("Good guess!")
        else:
            print("Wrong guess!")
            incorrect_guesses += 1
        
        if all(letter in guessed_letters for letter in word):
            print("\nCongratulations! You guessed the word:", word)
            break
    
    if incorrect_guesses >= max_incorrect_guesses:
        print("\nSorry, you ran out of guesses. The word was:", word)

hangman()
