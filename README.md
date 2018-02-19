# Rock-Paper-Scissors
My code for a rock paper scissors game in C++

#include <iostream>
#include <string>
#include <stdlib.h>
#include <time.h>
#include <ctime>

using namespace std;

int main()
{
    string response1;
    string again;
    cout << "Would you like to play rock, paper, scissors? (yes or no?) ";
    cin >> response1;

     if(response1 == "No" || response1 == "no")
        cout << "Fine fuck you I don't want to play with you anyway!" << endl;

    if(response1 == "Yes" || response1 == "yes")
    {
        do
        {
            const string computer_choices[] = {"rock", "paper", "scissors"};
            string random_choice = computer_choices[rand()%3];
            srand( time(NULL) );
            string your_choice;
            cout << "Great! What is your weapon? ";
            cin >> your_choice;
            if(your_choice == "rock" && random_choice == "scissors")
            {
                cout << "Computer chose " << random_choice << endl;
                cout << "So you win! " << endl;
                cout << endl;
            }
            else if(your_choice == "scissors" && random_choice == "paper" )
            {
                cout << "Computer chose " << random_choice << endl;
                cout << "So you win! " << endl;
                cout << endl;
            }
            else if( your_choice == "paper" && random_choice == "rock" )
            {
                cout << "Computer chose " << random_choice << endl;
                cout << "So you win! " << endl;
                cout << endl;
            }
            else if(your_choice == random_choice)
            {
                cout << "Computer chose: " << random_choice << endl << "you chose: " << your_choice << endl;
                cout << "Dam you tied with a computer Fam!" << endl;
                cout << endl;
            }
            else
            {
                cout << "You chose: " << your_choice << endl <<
                "computer chose: " << random_choice <<
                " so you lose!" << endl;
                cout << endl;
            }

            cout << "Would you like to try again? (yes or no) ";
            cin >> again;
            if(again == "No" || again == "no")
                cout << "Alright fuck you then" << endl;
        } while(again != "no");
    }

    return 0;
}
