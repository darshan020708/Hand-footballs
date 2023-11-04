# Hand-footballs#include <stdio.h>

int main() {
    int player1_score = 0;
    int player2_score = 0;
    int turn = 1;

    while (player1_score < 5 && player2_score < 5) {
        printf("Player 1 score: %d | Player 2 score: %d\n", player1_score, player2_score);
        printf("Player %d, choose (1 for goal, 2 for pass): ", turn);

        int choice;
        scanf("%d", &choice);

        if (choice == 1) {
            if (turn == 1) {
                printf("Player 1 scored!\n");
                player1_score++;
            } else {
                printf("Player 2 scored!\n");
                player2_score++;
            }
        } else if (choice == 2) {
            printf("Pass successful!\n");
        } else {
            printf("Invalid choice. Try again.\n");
            continue;
        }

        if (turn == 1) {
            turn = 2;
        } else {
            turn = 1;
        }
    }

    printf("Final score - Player 1: %d | Player 2: %d\n", player1_score, player2_score);
    if (player1_score > player2_score) {
        printf("Player 1 wins!\n");
    } else {
        printf("Player 2 wins!\n");
    }

    return 0;
}
