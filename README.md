# COC-hangman-project

#  Hangman Game (C Language)

## About the Project
This is a simple **Hangman Game** written in C language.  
It’s a fun console-based word guessing game where the player tries to guess the secret word one letter at a time.  
The game ends when the player either guesses all the letters correctly or loses all lives.

This project was made as part of my **C programming learning journey** during the *Clash of Coders (CoC)* event.

---

##  Game Logic
1. The computer has a secret word — in this case, `"mentor"`.
2. The player guesses one letter at a time.
3. If the guessed letter is correct, it appears in the word.
4. If it’s wrong, one life is lost.
5. The player gets **6 lives** in total.
6. The game ends when:
   - The player guesses the full word ✅  
   - Or all 6 lives are used ❌

---

##  How It Works
- Uses **loops, conditionals, and strings** in C.
- The `display` array stores underscores `_` for hidden letters.
- Each correct guess replaces an underscore with the actual letter.
- The `strcmp()` function checks if the player has guessed the full word.

---

##  Code Snapshot
```c
char word[] = "mentor"; // Secret word
char display[10];        // To show guessed letters
int lives = 6;           // Number of chances


## sample run
Welcome to Hangman!
Guess the letters of the secret word.

Word: _ _ _ _ _ _
Enter a Letter: e
Good guess!

Word: _ e _ _ _ _
Enter a Letter: a
Wrong guess! Lives left: 5

Word: _ e _ _ _ _
Enter a Letter: n
Good guess!

Word: _ e n _ _ _
Enter a Letter: t
Good guess!

Word: _ e n t _ _
Enter a Letter: o
Good guess!

Word: _ e n t o _
Enter a Letter: r
Good guess!

Congratulations! You've guessed the word: mentor
