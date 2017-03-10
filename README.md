# dayoftheyear
C++ program that transforms the month and day of the year to days in 365
Converts the month and day to the days of the year.

//************************************************************************//
// Subject: Assignment 6 - Day of the Year                                //
// Purpose: This program takes an input day and month of the year and     // 
//             translates it to the associated calendar day within 365.   //
// Author:  Nicole Anderson                                               //
// Date:    March 19, 2014                                                //
//************************************************************************//

#include <iostream>
#include <string>

using namespace std;

class dayOftheYear
{
public:
	void getMonth ();
	void getDay ();
	void getMonthName ();
	void printMonth ();
	void printDay ();
	void printMonthName ();

};
class numberOfDays: public dayOftheYear
{
public:
	int getDayCount ();
	void printDayCount ();
};

	string monthName;
	int month;
	int day;
	int daysInTheMonth;

	int numberOfDays::getDayCount ()
	{
		dayOftheYear::getMonth ();
		switch (month)
		{
		case 1:
			daysInTheMonth = 0 + day;
			break;
		case 2:
			daysInTheMonth = 31 + day;
			break;
		case 3:
			daysInTheMonth = 59 + day;
			break;
		case 4:
			daysInTheMonth = 90 + day;
			break;
		case 5:
			daysInTheMonth = 120 + day;
			break;
		case 6:
			daysInTheMonth = 151 + day;
			break;
		case 7:
			daysInTheMonth = 181 + day;
			break;
		case 8:
			daysInTheMonth = 212 + day;
			break;
		case 9:
			daysInTheMonth = 243 + day;
			break;
		case 10:
			daysInTheMonth = 273 + day;
			break;
		case 11:
			daysInTheMonth = 304 + day;
			break;
		case 12: 
			daysInTheMonth = 334 + day;
			break;
		default:
			cout << "Invalid entry!";
			break;
		}
		return daysInTheMonth;
	}
	void numberOfDays::printDayCount ()
	{
		switch (month)
		{
		case 1:
			daysInTheMonth = 0 + day;
			break;
		case 2:
			daysInTheMonth = 31 + day;
			break;
		case 3:
			daysInTheMonth = 59 + day;
			break;
		case 4:
			daysInTheMonth = 90 + day;
			break;
		case 5:
			daysInTheMonth = 120 + day;
			break;
		case 6:
			daysInTheMonth = 151 + day;
			break;
		case 7:
			daysInTheMonth = 181 + day;
			break;
		case 8:
			daysInTheMonth = 212 + day;
			break;
		case 9:
			daysInTheMonth = 243 + day;
			break;
		case 10:
			daysInTheMonth = 273 + day;
			break;
		case 11:
			daysInTheMonth = 304 + day;
			break;
		case 12: 
			daysInTheMonth = 334 + day;
			break;
		default:
			cout << "Invalid entry!";
			break;
		}
		cout << daysInTheMonth;
	
	}
	void dayOftheYear::getMonth ()
	{	
		cin >> month;
		cout << endl;
	}
	void dayOftheYear::getDay ()
	{
		cin >> day;
		cout << endl;
	}
	void dayOftheYear::getMonthName ()
	{
		switch (month)
		{
		case 1:
			monthName = "JAN";
			break;
		case 2:
			monthName = "FEB";
			break;
		case 3:
			monthName = "MAR";
			break;
		case 4:
			monthName = "Apr";
			break;
		case 5:
			monthName = "May";
			break;
		case 6:
			monthName = "Jun";
			break;
		case 7:
			monthName = "Jul";
			break;
		case 8:
			monthName = "AUG";
			break;
		case 9:
			monthName = "SEP";
			break;
		case 10:
			monthName = "OCT";
			break;
		case 11:
			monthName = "NOV";
			break;
		case 12: 
			monthName = "DEC";
			break;
		default:
			cout << "Invalid entry!";
			break;
		}
		cout << monthName;
	}
	void dayOftheYear::printMonth ()
	{
		cout << month;
	}
	void dayOftheYear::printDay ()
	{
		if (day <= 31)
		{
		cout << day << endl;
		}
	}
	void dayOftheYear::printMonthName ()
	{
		cout << monthName << endl;
	}

	int main ()
	{
		dayOftheYear monthAndDay;
		numberOfDays countingDays;
		cout << "Day Of The Month Translator" << endl;
		
		cout << "Input the month of the year in the format mm." << endl;
		monthAndDay.getMonth ();
		
		cout << "Input the day of the year in the format dd." << endl;
		monthAndDay.getDay ();
		

		cout << "The date you chose was: \n";
		
		monthAndDay.printMonth ();
		
		cout << " / ";
		
		monthAndDay.printDay ();
		
		cout << endl << endl;
		
		cout << "This converts to: \n";
		
		monthAndDay.getMonthName ();
		
		cout << " ";
		
		monthAndDay.printDay ();

		cout << endl;		

		cout << "The number of days is equivilent to: ";

		countingDays.printDayCount ();

		cout << endl;

	system ("pause");

	return 0;
	}
