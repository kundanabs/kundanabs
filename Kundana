#include <iostream>
using namespace std;
class Arithmetic {
public:
 int add(int a, int b) {
 return a + b;
 }
int subtract(int a, int b) {
return a - b;
}
};
class Multiplication {
public:
int multiply(int a, int b) {
 return a * b;
 }
};
class Division {
public:
 float divide(float a, float b) {
 return a / b;
 }};
class Calculator : public Arithmetic, public Multiplication, public Division {
public:
 void performOperations(int a, int b) {
 cout << "Addition: " << add(a, b) << endl;
 cout << "Subtraction: " << subtract(a, b) << endl;
 cout << "Multiplication: " << multiply(a, b) << endl;
 cout << "Division: " << divide(a, b) << endl;
 }
};
int main() {
 int num1, num2;
 cout << "Enter two numbers: ";
 cin >> num1 >> num2;
 Calculator calculator;
 calculator.performOperations(num1, num2);
 return 0;
}




#include <iostream>

using namespace std;

class Base {

protected:

int alpha;

public:

Base(int a) {

alpha = a;

cout << "Base class constructor called" << endl;

}

};

class Derived : public Base {

protected:

int beta;

int gamma;

public:

Derived(int a, int b, int c) {

beta = b;

gamma = c;

cout << "Derived class constructor called" << endl;

}

void displayValues() {

cout << "Alpha: " << alpha << endl;

cout << "Beta: " << beta << endl;

cout << "Gamma: " << gamma << endl;

}
};

int main() {

Derived obj(1, 2, 3);

obj.displayValues();

return 0;

}




#include <iostream>
#include <fstream>
using namespace std;
int main() {
ofstream outfile("example.txt");
if (outfile) {
cout << "File created successfully!" << std::endl;
outfile << "Hello, world!";
outfile.close();
ifstream infile("example.txt");
string line;
if (infile) {
cout << "File opened successfully!" << endl;
while (getline(infile, line)) {
cout << line << endl;
}
infile.close();
} else {
cout << "Error opening file!" << std::endl;
} } else {
cout << "Error creating file!" << std::endl;
} return 0; }




#include <iostream>
#include <fstream>
#include <ctime>
using namespace std;
void writeTimeToFile(const string& fileName) {
ofstream file(fileName, ios::binary);
if (file.is_open()) {
time_t currentTime = time(nullptr);
file.write((char*)&currentTime, sizeof(time_t));
file.close();
cout << "Time has been written to the file." << endl;
} else {
cout << "Failed to open the file for writing." << endl;
} }
void readTimeFromFile(const string& fileName) {
ifstream file(fileName, ios::binary);
if (file.is_open()) {
time_t storedTime;
file.read((char*)&storedTime, sizeof(time_t));
if (file) {
string timeString = ctime(&storedTime);
cout << "Time read from the file: " << timeString << endl;
} else {
cout << "Failed to read the time from the file." << endl;
}
file.close();
} else {
cout << "Failed to open the file for reading." << endl;
}
}
int main() {
string fileName = "time.bin";
writeTimeToFile(fileName);
readTimeFromFile(fileName);
return 0;
}




#include <iostream>
using namespace std;
double divide(int numerator, int denominator) {
if (denominator == 0) {
throw "Division by zero error";
}
return numerator / denominator;
}
int main() {
int numerator, denominator;
cout << "Enter numerator: ";
cin >> numerator;
cout << "Enter denominator: ";
cin >> denominator;
try {
double result = divide(numerator, denominator);
cout << "Result of division: " << result << endl;
} catch (const char* errorMessage) {
cerr << "Error:" << errorMessage << endl;
}
return 0;
}




#include <iostream>
#include <stdexcept>
using namespace std;
int main() {
 try {
 int arr[5] = {1, 2, 3, 4, 5};
 int index = 10; // Out-of-bounds index
 if (index >= 0 && index < 5) {
 cout << "Value at index " << index << ": " << arr[index] << endl;
 } else {
 throw out_of_range("Index is out of bounds!");
 }
 } catch (const out_of_range& e) {
 cout << "Exception caught: " << e.what() << endl;
 }
 return 0;
}
