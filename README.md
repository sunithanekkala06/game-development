# game-development
word path game
import random

word_list = ["apple", "evergreen", "near","restaurant","task"]

def word_chain():
    word = random.choice(word_list)
    print(f"Starting word: {word}")
    
    while True:
        last_letter = word[-1]
        print(f"\nLast letter: {last_letter}")
      
        matching_words = [w for w in word_list if w.startswith(last_letter) and w != word]
        
        if matching_words:
            word = random.choice(matching_words)
            print(f"Next word: {word}")
        else:
            print(f"No words found starting with {last_letter}. Game over!")
            break

word_chain()


