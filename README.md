# scrabble_game
#You have to enter word(s) and the sum of letter points in that word(s) gives you how many points you got , the project is very simple.


letters = ["A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z"]
points = [1, 3, 3, 2, 1, 4, 2, 4, 1, 8, 5, 1, 3, 4, 1, 3, 10, 1, 1, 1, 1, 4, 4, 8, 4, 10] 
print("Welcome to Scrabble!")
n = input("Write a word and start the game: ").upper()
letter_to_points = {key:value for key, value in zip(letters, points)}
letter_to_points[" "] = 0
print(letter_to_points)

def score_word(word):
  point_total = 0
  for letter in word:
    point_total += letter_to_points.get(letter, 0)
  return point_total
your_points = score_word(n)
print("You got:", your_points)
