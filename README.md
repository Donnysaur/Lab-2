#include <iostream>
#include <iomanip>
using namespace std;

struct emp {
    char name[50];
    char position[30];
    char department[30];
    int age;
    float salary;
};

void Accept(emp employees[], int count);
void Output(emp employees[], int count);

int main() {
    const int numEmployees = 3;
    emp employees[numEmployees];

    Accept(employees, numEmployees);
    Output(employees, numEmployees);

    system("pause");
    return 0;
}

void Accept(emp employees[], int count) {
    cin.ignore(); // to clear input buffer
    for (int i = 0; i < count; ++i) {
        cout << "\nEmployee Record " << i + 1 << "..." << endl;
        cout << "Employee Name: ";
        cin.getline(employees[i].name, 50);

        cout << "Employee Position: ";
        cin.getline(employees[i].position, 30);

        cout << "Employee Department: ";
        cin.getline(employees[i].department, 30);

        cout << "Employee Age: ";
        cin >> employees[i].age;
        cin.ignore(); // clear buffer for next getline

        cout << "Employee Salary: ";
        cin >> employees[i].salary;
        cin.ignore(); // clear buffer again
    }
}

void Output(emp employees[], int count) {
    cout << fixed << setprecision(2);
    cout << "\nEmployee Records Encoded..." << endl;
    for (int i = 0; i < count; ++i) {
        cout << "\nEmployee " << i + 1 << ":\n";
        cout << "Name: " << employees[i].name << endl;
        cout << "Position: " << employees[i].position << endl;
        cout << "Department: " << employees[i].department << endl;
        cout << "Age: " << employees[i].age << endl;
        cout << "Salary: $" << employees[i].salary << endl;
    }
}
