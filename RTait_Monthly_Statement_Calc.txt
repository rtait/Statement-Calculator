//Roxanne Tait
//8 FEB 2012
//this program calculates monthly internet statements

#include <iostream>
#include <iomanip>
using namespace std;

int main ()

{

char choice; double hours; double charge;


//const for internet pakages
const double package_a = 9.95;
const double package_b = 14.95;
const double package_c = 19.95;



//const for menu options
const char a_option = 'a';
const char b_option = 'b';
const char c_option = 'c';



//menu
cout <<"\t\tInternet Bill Summary" << endl;
cout <<" PACKAGE a - $9.95 for 10 hours" << endl;
cout <<" PACKAGE b - $14.95 for 20 hours" << endl;
cout <<" PACKAGE c - $19.95 for Unlimited Hours" << endl;



//set to two decimals
cout << fixed << showpoint << setprecision(2);



//get data
cout <<"    Please select current plan (in lowercase letters): ";
cin >> choice;
cout << "    How many hours were used this month?";
cin >> hours;


//validate hours
while (choice > 'c' || choice < 'a')
{ 
	cout << " Please select a - c only." << endl;
	cout << "   Please select current plan (in lowercase letters):" << endl;
	cin >> choice;
}
	

while (hours > 744 || hours < 0)
{ 
	cout << "hours cannot exceed 744." << endl;
	cout << "    How many hours were used this month?" << endl;
	cin >> hours;
}

//choice a

      if    (choice == 'a')
      {
            if(hours <= 10)
            {
                  cout << "    monthly charge $ "<< package_a << endl;
            }

            else if(hours >= 11)
            {
                  charge = package_a + ((hours - 10) * 2.00);
                  cout << "   monthly charge $ " << charge << endl;
            }
      }



//choice b

     if    (choice == 'b')
      {
            if(hours <= 20)
            {
                  cout << "    monthly charge $ "<< package_b << endl;
            }

            else if(hours >= 21)
            {
                  charge = package_a + ((hours - 20) * 1.00);
                  cout << "   monthly charge $ " << charge << endl;
            }
      }


//choice c

  if    (choice == 'c')
      {
			cout << "    monthly charge $ "<< package_c << endl;
	  }



					 			 
return 0;
}