# Exp-13 Function and Operator Overloading

## Aim:
To demonstrate the concepts of function overloading and operator overloading in C++.

## Software Used:
- Dev c++
  
## Theory:
Function Overloading: Function overloading allows the same function name to be used for different functions with different parameter lists. This helps in using the same function name for different types of operations.

Operator Overloading: Operator overloading allows us to define custom behaviors for C++ operators when applied to user-defined types such as classes. This enhances the functionality of operators for objects.

## Program 1: Function Overloading
<strong> Code: </strong>
<br>
```cpp
// Premish Ninawe
// 23070123092
// ENTC B1
#include <iostream>
using namespace std;

int add(int a, int b) {
    return a + b;
}

float add(float a, float b) {
    return a + b;
}

int add(int a, int b, int c) {
    return a + b + c;
}

int main() {
    cout << "Addition of 2 integers: " << add(3, 4) << endl;
    cout << "Addition of 2 floats: " << add(3.5f, 4.5f) << endl;
    cout << "Addition of 3 integers: " << add(1, 2, 3) << endl;
    return 0;
}
```
<strong> Output: </strong>
<br>
![image](https://github.com/user-attachments/assets/57827789-7824-4fb1-9e42-056b3b68e9bf)


## Program 2: Operation Overloading
<strong> Code: </strong>
<br>
```cpp
// Premish Ninawe
// 23070123092
// ENTC B1
#include <iostream>
using namespace std;

class Complex {
    private:
        float real;
        float imag;
    public:
        Complex(float r = 0, float i = 0) {
            real = r;
            imag = i;
        }
        
        Complex operator + (const Complex &obj) {
            Complex temp;
            temp.real = real + obj.real;
            temp.imag = imag + obj.imag;
            return temp;
        }
        
        void display() const {
            cout << real << " + " << imag << "i" << endl;
        }
};

int main() {
    Complex c1(3.5, 2.5);
    Complex c2(1.6, 3.7);
    Complex c3 = c1 + c2;
    
    cout << "First complex number: ";
    c1.display();
    cout << "Second complex number: ";
    c2.display();
    cout << "Sum of complex numbers: ";
    c3.display();
    return 0;
}
```
<strong> Output: </strong>
<br>
![image](https://github.com/user-attachments/assets/c986dbf2-81e0-4d1a-9020-a9f107c8af88)


## Conclusion:
We learned how to use operator overloading to add two complex numbers using the + operator in a user-defined way.
