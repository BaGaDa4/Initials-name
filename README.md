# Initials-name
#include <iostream>
#include <string>
#include<Windows.h>
using namespace std;
int main() {
	SetConsoleCP(1251);
	SetConsoleOutputCP(1251);
	cout << "Введите ФИО " << endl;
	string firstname, midname, lastname;
	cin >> firstname >> midname >> lastname;
	firstname[0] = toupper(firstname[0]);
	midname[0] = toupper(midname[0]);
	lastname[0] = toupper(lastname[0]);
	for (int i = 1; i < firstname.length(); i++) {
		firstname[i] = tolower(firstname[i]);
	}
	for (int i = 1; i < midname.length(); i++) {
		midname[i] = tolower(midname[i]);
	}
	for (int i = 1; i < lastname.length(); i++) {
		lastname[i] = tolower(lastname[i]);
	}
	string initials;
	initials += toupper(midname[0]);
	initials += '.';
	initials += toupper(lastname[0]);
	initials += '.';
	cout << firstname << " " << initials;
	return 0;
}
