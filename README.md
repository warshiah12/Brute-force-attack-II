# Brute-force-attack-II
[ using while-loop and break statement ] 
#include<iostream>
using namespace std;
int main()
{                                                      
	int attempts=5;            /*declaring variable and initialising value to it*/
	string passcode = "246";
	string number;
	while (attempts > 0)//using while loop
	{
		cout << "Enter the passcode:" << endl;
		cin >> number;
		if (number == passcode) {  //using if else to check if number is equal to passcode or not

			cout << "Permission granted! You can enter the safe. " << endl;
			break;
		}
		else {
			attempts = attempts - 1;  //using decreement operator
		}
		cout << attempts << " chances left. " << endl;   //this statement will tell the user about the remaining attempts left
	}
	if (attempts == 0)   //if there are no more chances left then the following statement will be executed
	{
		cout << "You have incorrectly entered the password 5 times. You cannot enter the safe! " << endl;
	}
	cin.get();
	return 0;
}
