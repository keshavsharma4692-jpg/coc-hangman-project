#include <stdio.h>
#include <string.h>

int main() {
    char word[] = "mentor"; // Secret word to guess
    char guess;
    char display[10];  // To display guessed letters and underscores
    int i, lives = 6; // Number of allowed wrong guesses
    int correct = 0;


    // Initialize display with underscores
    for (i = 0; i < strlen(word); i++) {
        display[i] = '_';
    }
    display[i] = '\0';

    printf("Welcome to Hangman!\n");
    printf("Guess the letters of the secret word.\n");

    while (lives > 0)  {
        int found = 0;
        printf("\nWord: ");
        for (i = 0; i < strlen(word); i++) {
            printf("%c ", display[i]);
        }
        printf("\nEnter a Letter: ");
        scanf(" %c", &guess);

        // Check if the guessed letter is in the word

        for (i = 0; i < strlen(word); i++) {
            if (word[i] == guess && display[i] == '_') {
                display[i] = guess;
                correct++;
                found = 1;
            }
        }
        if (!found) {
            lives--;
            printf("Wrong guess! Lives left: %d\n", lives);
        } else {
            printf("Good guess!\n");
        }
        // Check if the word is fully guessed
        if (strcmp(word, display) == 0) {
            printf("\nCongratulations! You've guessed the word: %s\n", word);
            break;
        }
    }

    if (lives == 0) {
        printf("\nGame Over! The correct word was: %s\n", word);
    }

    return 0;

}
