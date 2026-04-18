# coba-coba
website ini adalah sarana untuk coba-coba penuagasan matkul "Algoritma Pemrograman" ala anak kuliahan
 SELAMAT MENCOBA!
 #include <iostream>
#include <cstdlib>
#include <ctime>

using namespace std;

int main() {
    srand(time(0));
    
    int angkaTarget = rand() % 100 + 1;
    int tebakan;
    int nyawa = 7; // Batas nyawa
    int skor = 0;
    bool menang = false;

    cout << "======================================" << endl;
    cout << "    GAME TEBAK ANGKA: EDISI LIMIT" << endl;
    cout << "======================================" << endl;
    cout << "Saya sudah memilih angka 1-100." << endl;
    cout << "Kamu punya " << nyawa << " nyawa untuk menebak." << endl;
    cout << "--------------------------------------" << endl;

    while (nyawa > 0) {
        cout << "\nNyawa tersisa: " << nyawa << endl;
        cout << "Masukkan tebakanmu: ";
        cin >> tebakan;

        if (tebakan == angkaTarget) {
            menang = true;
            skor = nyawa * 100; // Skor dihitung dari sisa nyawa
            break;
        } else if (tebakan > angkaTarget) {
            cout << "Terlalu BESAR!" << endl;
        } else {
            cout << "Terlalu KECIL!" << endl;
        }

        nyawa--;
    }

    cout << "\n--------------------------------------" << endl;
    if (menang) {
        cout << "SELAMAT! Kamu menang!" << endl;
        cout << "Angka rahasianya adalah: " << angkaTarget << endl;
        cout << "SKOR KAMU: " << skor << endl;
    } else {
        cout << "GAME OVER! Nyawa kamu habis." << endl;
        cout << "Angka yang benar adalah: " << angkaTarget << endl;
    }
    cout << "======================================" << endl;

    return 0;
}
