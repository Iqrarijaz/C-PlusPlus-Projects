#include<iostream>
#include<stdio.h>
#include<conio.h>
#include<stdlib.h>
#include<fstream>
using namespace std;
int main(){
	ifstream file1;
	ofstream file2;
	char ch;
	char sfile[10], tfile[10];
	cout << "\nEnter the source filename: ";
	cin >> sfile;
	cout << "\nEnter the target filename: ";
	cin >> tfile;

	file2.open(sfile);
	file2 << "hello world";
	file2.close();

	file1.open(sfile);
	file2.open(tfile);

	while (file1.get(ch)) {
		cout << ch;
		if (ch == ' ') {
			continue;
		}
		file2 << ch;
	}
	file1.close();
	file2.close();
	return 0;
}
