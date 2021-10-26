# Lecture-9-Excercises-While-and-Do-While

9 time's table reverse : 

    //#include<iostream>
    //using namespace std;
    //
    //int main()
    //{
    //	int num = 108;
    //
    //	while (num != 0){
    //		if ((num % 9) == 0) {
    //			cout << num << endl;
    //
    //		}
    //		num--;
    //	}
    //}
    
Pointless Box : 



Input Improvements : 




Brute force 1 and 2 : 
( Miss for this excercise I got help from reinald, but only during the task brute force 2, the brute force 1 was done by me. for these two excerices I have complide into 1 task ask brute force 2 was a continuation. ) 

    #include <iostream>
    #include<string>
    using namespace std;

    int main()
    {
        string passcode = "246";
        string userInput;
        int attempts = 4;

        cout << "Enter the passcode to the safe:" << endl;
        cin >> userInput;

        if (userInput == passcode) {
            cout << "You have entered the correct passcode, beep..boop..beep..." << endl;
        }
        else {
            while (userInput != passcode) {

                cin.clear();
                cin.ignore(10000, '\n');

                cout << "This is the inccorect passcode, please try again:" << endl;
                cin >> userInput;

                if (userInput == passcode) {
                    cout << "You have entered the correct passcode, beep..boop..beep..." << endl;
                    break;
                }

                attempts--;

                if (attempts == 0) {
                    cout << "This is the incorrect passcode, please try again:" << endl;
                    break;
                }
                cout << "You have " << attempts << "left " << endl;
            }
        }
    }
    
    
