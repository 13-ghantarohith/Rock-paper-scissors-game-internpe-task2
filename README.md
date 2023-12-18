# Rock-paper-scissors-game-internpe-task2
#include <iostream>
#include <cstdlib>
#include <ctime>

using namespace std;

int main() {
   srand(static_cast<unsigned int>(time(0)));
    int computerChoice = rand() % 3;
    int userChoice;
    cout << "Enter your choice (0 for Rock, 1 for Paper, 2 for Scissors): ";
    cin >> userChoice;
    cout << "You chose: ";
    switch (userChoice) {
        case 0:
            cout << "Rock";
            break;
        case 1:
            cout << "Paper";
            break;
        case 2:
            cout << "Scissors";
            break;
        default:
            cout << "Invalid choice";
            return 1; 
    }

    cout << endl;
    cout << "Computer chose: ";
    switch (computerChoice) {
        case 0:
            cout << "Rock";
            break;
        case 1:
            cout << "Paper";
            break;
        case 2:
            cout << "Scissors";
            break;
    }

    cout << endl;
    if (userChoice == computerChoice) {
        cout << "It's a tie!" << endl;
    } else if ((userChoice == 0 && computerChoice == 2) ||
               (userChoice == 1 && computerChoice == 0) ||
               (userChoice == 2 && computerChoice == 1)) {
        cout << "You win!" << endl;
    } else {
        cout << "Computer wins!" << endl;
    }

    return 0;
}
