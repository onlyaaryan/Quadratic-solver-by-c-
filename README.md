//Quadratic-solver-by-c++
// This is code for Matha lover in this With the help of the Cpp code
// We can solve Quadratic Equations 

#include<stdio.h>
#include<iostream>
#include<iomanip>
#include<cmath>
using namespace std;
int main(void)
{
    int a , b , c ;
    float D , x1 , x2 ;
    cout<<"Quadratic Equation Solver" << endl;
    cout << "The equation is of the form ax^2 + bx + c = 0" << endl;

    cout<<"\n\n";


    cout << "Enter coefficients a :  ";
    cin >> a ;
    cout << "Enter coefficients b :  ";
    cin >> b ;
    cout << "Enter coefficients c :  ";
    cin >> c ;

    cout<<"\n\n";

    D = b * b - 4 * a * c ;
    if (D < 0)
    {
        cout<<"The roots Are Imaginary"<<endl;
        int i = sqrt(-D);
        cout<<"\n";
        cout << "x1 = " << setw(2) << -b / (2 * a) << " + " << i / (2 * a) << "i" << endl;
        cout << "x2 = " << setw(2) << -b   / (2 * a) << " - " << i / (2 * a) << "i" << endl;
        return 0;
    }
    else if (D == 0)
    {
        x1 = -b / (2 * a);
        cout << "The roots are real and equal" << endl;
        cout << "x1 = x2 = " <<setw(2) << x1 << endl;
    }
    else
    {
        x1 = (-b + sqrt(D)) / (2 * a);
        x2 = (-b - sqrt(D)) / (2 * a);
        cout << "The roots are real and different" << endl;
        cout << "x1 = " << setw(2) << x1 << endl;
        cout << "x2 = " << setw(2) << x2 << endl;
    }
}
