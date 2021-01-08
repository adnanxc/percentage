# percentage
Write a C++ code with a function that takes two positive numbers and calculate what percentage the smaller number is of the larger number. Print the calculated value from the main function. 


#include <iostream>
using namespace std;

float perc (float x , float y){
    float p = (y/x)*100.0;
    return p;
}

int main(){

    float x , y , temp;
    cout << "Enter the first positive number: ";
    cin >> x;
    cout << "Enter the second positive number: ";
    cin >> y;

    if(x<y){
        temp = x;
        x = y;
        y = temp;
    }

    cout << y << " is " << perc(x , y) << "% of " << x;

    return 0;
}

