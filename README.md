#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main()
{
    int number, guess;
    int number_of_guesses = 0;

    // Initialize random number generator
    srand(time(NULL));

    // Generate a random number between 1 and 100
    number = rand() % 100 + 1;

    printf("====================================\n");
    printf("     WELCOME TO THE GUESSING GAME\n");
    printf("====================================\n");

    do
    {
        printf("\nPlease enter your guess between (1 to 100): ");
        scanf("%d", &guess);

        number_of_guesses++;

        if (guess < number)
        {
            printf("Guess a larger number.\n");
        }
        else if (guess > number)
        {
            printf("Guess a smaller number.\n");
        }
        else
        {
            printf("\nCongratulations! You guessed the correct number");
            printf(" in %d guesses.\n", number_of_guesses);
        }

    } while (guess != number);

    printf("\nThank you for playing the guessing game!\n");
    printf("Developed by: SAMAR PRATAP SINGH\n");

    return 0;
}
