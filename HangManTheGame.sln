#include <iostream>
#include <string>
#include <vector>
using namespase std;

void hangmanGame() {
    std::string word = "programming"; 
    std::string guessedWord(word.length(), '_');
    std::vector<char> guessedLetters; 
    int attempts = 7; 

    std::cout << "Welcome to the game 'Висилиця'!\n";
    std::cout << "You've got" << attempts << "to try to guess the word.\n";

    while (attempts > 0 && guessedWord != word) {
        cout << "Word: " << guessedWord << '\n';
        cout << "Guess the letter: ";
        char guess;
        cin >> guess;

        if (std::find(guessedLetters.begin(), guessedLetters.end(), guess) != guessedLetters.end()) {
            cout << "You have already tried this letter. Try another one.\n";
            continue;
        }

        guessedLetters.push_back(guess);
        bool found = false;

        for (size_t i = 0; i < word.length(); ++i) {
            if (word[i] == guess) {
                guessedWord[i] = guess;
                found = true;
            }
        }

        if (found) {
            std::cout << "Correctly!\n";
        } else {
            --attempts;
            cout << "Wrong! You've got left " << attempts << " спроб.\n";
        }
    }

    if (guessedWord == word) {
        cout << "Welcome! You guessed the word: " << word << '\n';
    } else {
        cout << "Unfortunately, you lost. The word was: " << word << '\n';
    }
}

int main() {
    hangmanGame();
    return 0;
}
