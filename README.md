#include <iostream>
using namespace std;
int main() {
/*
    cout << "Hello, World!" << endl;
    double sayi1;
    double sayi2;
    int islem;
    int islem0;
    int islem1;
    int islem2;

    cout << "Lutfen 1. Sayi Giriniz: ";
    cin >> sayi1;
    cout << endl;
    cout << "Lutfen 2. Sayi Giriniz: ";
    cin >> sayi2;
    cout << endl;
    cout << "Basit islem yapmak istemiyorsaniz 0 giriniz: ";
    cin >> islem0;
    if(islem0 == 0){
        cout << "Diger islemeler; 5)ort alma: 6)karelerin toplami 7)Toplamlarin karesi 8)Daha farkli islem: ";
        cin >> islem1;
        cout << endl;
        if(islem1 == 5){
            cout << "Girilen Sayilarin Ortalamasi: " << (sayi1 + sayi2)/ 2;
        }
        else if(islem1 == 6){
            cout << "Girilen Sayilerin Kareleri Toplami: " << (sayi1*sayi1) + (sayi2*sayi2);
        }
        else if(islem1 == 7){
            cout << "Toplamalarin Karesi: " << (sayi1+sayi2)*(sayi1+sayi2);
        }
        else if(islem1 ==8 ){
            cout << "Daha farkli islemler; 9)ortlamalari ile karelerinin toplami ile bolumu: ";
            cin >> islem2;
            if(islem2 == 9){
                cout << "Girilen Sayilerin Ortlamalari ile karelerinin toplami ile bolumu: " << ((sayi1+sayi2)/2)/((sayi1*sayi1) + (sayi2*sayi2));
            }
        }
    }
    else if(islem0 != 0){
        cout << "Girilen Sayilarin hangi islem yapmak istersiniz ; 1)+ 2)- 3)/ 4)* : ";
        cin >> islem;
        cout << endl;


        if(islem == 1){
            cout << "Sayilarin Toplami: " << sayi1 + sayi2;
        }
        else if(islem == 2){
            cout << "Sayilarin Farki: " << sayi1 - sayi2;
        }
        else if(islem == 3){
            cout << "Sayilarin Bolumu: " << sayi1 / sayi2;
        }
        else if(islem == 4){
            cout << "Sayilarin Carpimi: " << sayi1 * sayi2;
        }
    }
 //ÜÇGEN İSİMLENDİRME PROGRAMI

    double kenar1;
    double kenar2;
    double kenar3;

    cout << "Lutfen Cesidini Ogrenmek Istediginiz Ucgenin Kenarlani Giriniz: "<< endl;
    cout << "1.Kenar Uzunlugunu giriniz: ";
    cin >> kenar1;
    cout << endl;
    cout << "2.Kenar Uzunlugunu giriniz: ";
    cin >> kenar2;
    cout << endl;
    cout << "3.Kenar Uzunlugunu giriniz: ";
    cin >> kenar3;
    cout << endl;

    if(kenar1 == kenar2 && kenar2 == kenar3 && kenar1 == kenar3){
        cout << "Bu Ucgen Eskenar Ucgendir.";
    }
    if(kenar1 < kenar2 && kenar2 < kenar3){
        if((kenar1 * kenar1)+(kenar2*kenar2) == kenar3*kenar3){
            cout << "Bu Ucgen Dik Ucgendir.";
        }
        else if(kenar1 < kenar3 && kenar3 < kenar2){
            if((kenar1 * kenar1)+(kenar3*kenar3) == kenar2*kenar2){
                cout << "Bu Ucgen Dik Ucgendir.";
            }
        }
        else if(kenar2 < kenar3 && kenar3 < kenar1){
            if((kenar2 * kenar2)+(kenar3*kenar3) == kenar1*kenar1){
                cout << "Bu Ucgen Dik Ucgendir.";
            }
        }
        else if(kenar1 != kenar2 && kenar1 !=kenar3 && kenar2 != kenar3){
            cout << "Bu Ucgen Cesitkenar Ucgendir.";
        }
    }
    else if(kenar1 == kenar2 || kenar2 == kenar3 || kenar1 == kenar3){
        cout << "Bu Ucgen Ikizkenar Ucgendir.";
    }
     // BANKA PROGRAMI
    double bakiye;
    int islem;
    double miktar;

    // Kullanıcıdan mevcut bakiyeyi ve yapmak istediği işlemi alalım
    cout << "Mevcut bakiyenizi girin: ";
    cin >> bakiye;

    cout << "Yapmak istediginiz islemi secin:" << endl;
    cout << "1. Para Yatirma" << endl;
    cout << "2. Para Cekme" << endl;
    cout << "3. Bakiye Sorgulama" << endl;
    cin >> islem;

    // İşlemi gerçekleştirelim
    if (islem == 1) {
        cout << "Yatirmak istediginiz miktari girin: ";
        cin >> miktar;
        bakiye += miktar;
        cout << "Yeni bakiyeniz: " << bakiye << endl;
    } else if (islem == 2) {
        cout << "Cekmek istediginiz miktari girin: ";
        cin >> miktar;
        if (miktar > bakiye) {
            cout << "Hesabinizda yeterli bakiye yok!" << endl;
        } else {
            bakiye -= miktar;
            cout << "Yeni bakiyeniz: " << bakiye << endl;
        }
    } else if (islem == 3) {
        cout << "Mevcut bakiyeniz: " << bakiye << endl;
    } else {
        cout << "Gecersiz islem!" << endl;
    }
      //SAVAŞ OYUNU
    // Karakter ve düşmanın özellikleri
    int karakterSaldiriGucu = 50;
    int karakterSavunmaGucu = 30;
    int karakterCanPuani = 100;

    int dusmanSaldiriGucu = 40;
    int dusmanSavunmaGucu = 20;
    int dusmanCanPuani = 80;

    // Savaş başlangıcı
    while (karakterCanPuani > 0 && dusmanCanPuani > 0) {
        // Karakterin saldırısı
        int karakterHasar = karakterSaldiriGucu - dusmanSavunmaGucu;
        if (karakterHasar < 0) {
            karakterHasar = 0;
        }
        dusmanCanPuani -= karakterHasar;
        if (dusmanCanPuani <= 0) {
            cout << "Dusmani yendiniz!" << endl;
            break;
        }

        // Düşmanın saldırısı
        int dusmanHasar = dusmanSaldiriGucu - karakterSavunmaGucu;
        if (dusmanHasar < 0) {
            dusmanHasar = 0;
        }
        karakterCanPuani -= dusmanHasar;
        if (karakterCanPuani <= 0) {
            cout << "Karakter oldu!" << endl;
            break;
        }
    }
*/
    return 0;
}
