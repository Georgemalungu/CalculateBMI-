#include <iostream>
using namespace std;

// Function to calculate BMI
double calculateBMI(double weight, double height) {
    return weight / (height * height);
}

// Function to display BMI category
void displayBMICategory(double bmi) {
    if (bmi < 20) {
        cout << "Lower than normal weight";
    } else if (bmi >= 20 && bmi <= 25) {
        cout << "Normal Weight";
    } else if (bmi > 25 && bmi <= 30) {
        cout << "Overweight";
    } else if (bmi > 30 && bmi <= 40) {
        cout << "Obese";
    } else {
        cout << "Extreme obese";
    }
}

int main() {
    // Variable declarations
    double height, weight, bmi;

    // Input section
   cout << "Enter the height in meters: ";
    cin >> height;
    cout << "Enter the weight in kilograms: ";
    cin >> weight;

    // Calculate BMI
   bmi = calculateBMI(weight, height);

    // Display BMI and category
  cout << "Your BMI is: " << bmi << endl;
    displayBMICategory(bmi);

  return 0;
}
