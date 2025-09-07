#include <iostream>
#include <signal.h>

//Разложить целое число на простые множители.
using namespace std;
int main() {
    int number;
    cin >> number;
    bool isFirst = true;
    for (int i = 2; i < number; i++) {
        if (i*i > number) {
            i=number;
        }
        while (number % i == 0) {
            if (isFirst) {
                cout << i;
                isFirst = false;
            }else {
                cout << "*"<<i;
            }
            number = number/i;
        }
    }
    return 0;
}
