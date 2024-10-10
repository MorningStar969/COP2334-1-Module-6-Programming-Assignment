# COP2334-1-Module-6-Programming-Assignment
This is a GitHub repository for the Programming Assignment from Module 6.

// This program is used to caculate the average number of days a company's employees are absent.

// Including the iostream library
#include <iostream>
using namespace std;

// Function prototypes
int numEmployees();
int daysMissed(int);
double averageDaysMissed(int, int);
int main() {

  // Declaring variables
  int employees = numEmployees();
  int totalDaysMissed = daysMissed(employees);
  double average = averageDaysMissed(employees, totalDaysMissed);
  cout << "The average number of days missed per employee is " << average << endl;
}

// Function to get the number of employees
int numEmployees() {
  int employees;
  cout << "Enter the number of employees in the company: ";
  cin >> employees;
  while(employees < 1);
  return employees;
}

// Function to get the number of days missed by each employee
int daysMissed(int employees) {
  int total = 0;
  for(int i = 1; i <= employees; i++) {
    int days;
    cout << "Enter the number of days employee " << i << " missed: ";
    cin >> days;
    while(days < 0);
    total += days;
  }
  return total;
}
// Function to calculate the average number of days missed
double averageDaysMissed(int employees, int total) {
  return (double)total / employees;
}
