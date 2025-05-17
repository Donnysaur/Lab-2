#include <iostream>
#include <cstdlib>
#include <iomanip>

using namespace std;

struct emp
{
	char name[50];
	char position[30];
	char department[30];
  int age;
	float salary;
};
void Accept();
void Output(emp *employee);

int main()
{
	Accept();
	system("pause");
}
void Accept()
{
	emp* employee{};
	employee - new emp();
	cout << "Employee Record..." << endl;
	cout << "Employee Name : ";
	cin.getline(employee->name, 49);
	cout << "Employee Position : ";
	cin.getline(employee->position, 29);
	cout << "Employee Department : ";
	cin.getline(employee->department, 29);
    cout << "Employee Age : ";
    cin.getline(employee->age);
	cout << "Employee Salary : ";
	cin >> employee->salary;
	Output(employee);

}
void Output(emp *employee)
{
	cout << fixed;
	cout << endl;
	cout << "Employee Record Encoded..." << endl;
	cout << employee->name << endl;
	cout << employee->position << endl;
	cout << employee->department << endl;
	cout << setprecision(2) << employee->salary << endl;
	cout << endl;
}
