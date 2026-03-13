#include <iostream>
#include <string>

using namespace std;

int main() {
    const int numQuestions = 5;
    string questions[numQuestions] = {
        "1. What is the capital of France?\n(a) Paris\n(b) London\n(c) Rome\n(d) Madrid",
        "2. Which language is used for system programming?\n(a) Python\n(b) C++\n(c) HTML\n(d) JavaScript",
        "3. Who wrote 'Romeo and Juliet'?\n(a) Charles Dickens\n(b) William Shakespeare\n(c) J.K. Rowling\n(d) Mark Twain",
        "4. What is 9 + 10?\n(a) 19\n(b) 20\n(c) 21\n(d) 18",
        "5. Which planet is known as the Red Planet?\n(a) Earth\n(b) Mars\n(c) Venus\n(d) Jupiter"
    };
    
    char answers[numQuestions] = {'a', 'b', 'b', 'a', 'b'};
    char userAnswer;
    int score = 0;

    cout << "Welcome to the Quiz Game!\nAnswer the following questions:\n\n";

    for (int i = 0; i < numQuestions; i++) {
        cout << questions[i] << "\nYour answer: ";
        cin >> userAnswer;

        if (tolower(userAnswer) == answers[i]) {
            cout << "Correct!\n\n";
            score++;
        } else {
            cout << "Wrong! The correct answer is: " << answers[i] << "\n\n";
        }
    }

    cout << "Quiz Over! Your final score is " << score << " out of " << numQuestions << ".\n";

    return 0;
}
