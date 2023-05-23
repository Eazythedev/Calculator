#include <iostream>
#include <cmath>
#include <limits>
using namespace std;

int main()
{
    double num1, num2;
    char operation;
    
    cout << "This is Dat Calculator" << endl;
    
    while (true)
    {
        cout << "Enter the first number: ";
        if (!(cin >> num1))
        {
            cout << "That ain't a valid input. Please enter a valid number." << endl;
            cin.clear();
            cin.ignore(numeric_limits<streamsize>::max(), '\n');
            continue;
        }
        
        cout << "Enter the operation (+, -, *, /, %): ";
        cin >> operation;
        
        if (operation == '+' || operation == '-' || operation == '*' || operation == '/')
        {
            cout << "Enter the second number: ";
            if (!(cin >> num2))
            {
                cout << "That ain't a valid input. Please enter a valid number." << endl;
                cin.clear();
                cin.ignore(numeric_limits<streamsize>::max(), '\n');
                continue;
            }
        }
        
        switch (operation)
        {
            case '+':
                cout << num1 << " + " << num2 << " = " << num1 + num2 << endl;
                break;
            case '-':
                cout << num1 << " - " << num2 << " = " << num1 - num2 << endl;
                break;
            case '*':
                cout << num1 << " * " << num2 << " = " << num1 * num2 << endl;
                break;
            case '/':
                if (num2 != 0)
                    cout << num1 << " / " << num2 << " = " << num1 / num2 << endl;
                else
                    cout << "Error: Division by zero is not allowed." << endl;
                break;
            case '%':
                if (fmod(num1, 1) == 0 && fmod(num2, 1) == 0)
                    cout << static_cast<int>(num1) << " % " << static_cast<int>(num2) << " = " << static_cast<int>(num1) % static_cast<int>(num2) << endl;
                else
                    cout << "Error: Modulus operation requires integer operands." << endl;
                break;
            default:
                cout << "Invalid operation. Please enter a valid operation." << endl;
        }
        
        cout << "Do you want to perform another calculation? (y/n): ";
        char choice;
        cin >> choice;
        
        if (choice != 'y' && choice != 'Y')
            break;
    }
    
    cout << "Ok, peace!" << endl;
    return 0;
}
