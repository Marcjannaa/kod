#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;

int main() {
    int liczba;
    int liczba_pobrana = -1;
    int licznik = 0;
    srand(time(NULL));
    liczba = rand() % 100;

    while (liczba != liczba_pobrana)
    {
        cin >> liczba_pobrana;
        if (liczba_pobrana == liczba)
        {
            cout << "zgadleś\n";
        }
        else
        {
            cout << "nie zgadleś";
            if (liczba_pobrana > liczba)
                cout << "za wysoko\n";
            else
                cout << "za malo\n";
        }
        licznik++;
    }
    cout << "ilosc prob: " << licznik;
}
