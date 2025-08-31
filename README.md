# yyu-cikmissorular1.sinif2.donem
çıkmış soruların sadece çözümü yani cevapları var
#include <iostream>
#include <vector>
#include<ctime>
#include <fstream>
#include <algorithm>
#include <set>
#include <fstream>
#include<cstdlib>
#include <map>
#include <queue>

using namespace std;
////Rastgele bir sayı al ve ortalamasını bul
//int main()
//{
//    vector<int> ortalama;
//    srand(time(0));
//    int toplam =0;
//    cout << "sayi girin";
//    for (int i = 0; i < 10; i++) {
//        int sayi = rand() % 100 + 1;
//        
//        ortalama.push_back(sayi);
//        toplam += sayi;
//    }
//    double ortalamaal = static_cast<double>(toplam) / ortalama.size();
//    cout << "Ortalamasi: " << ortalamaal << endl;
//
//	return 0;
//}
// Linear search ile aranan sayıyı bulma
//int linearSearch(int d[], int size, int x) {
//    for (int i = 0; i < size; i++) {
//        if (d[i] == x) return i;
//    }
//    return -1;
//}
//
//int main() {
//    int d[] = { 2,6,10,13,17,22,38,44 };
//    int size = sizeof(d) / sizeof(d[0]);
//    int idx = linearSearch(d, size, 22);
//    cout << idx << endl;
//}
// 
// Rasgele sayı üret sırla ve eski haline çevir
//int main() {
//    vector<int> v, yedek;
//    srand(time(0));
//    while (v.size() < 10) {
//        int r = rand() % 100 + 1;
//        if (find(v.begin(), v.end(), r) == v.end()) v.push_back(r);
//    }
//    yedek = v;
//    sort(v.begin(), v.end());
//    for (int x : v) cout << x << " "; cout << endl;
//    v = yedek;
//    for (int x : v) cout << x << " ";
//    return 0;
//}
// Aşağıda verilen kod aslında yine aşağıda verdiğim sayılarla oluşturulmuş koddur istediğin sayıyı verince oluşturulan kare ben 5 verdim
// 0 0 0 0 0
// 0 1 1 1 0
// 0 1 2 1 0
// 0 1 1 1 0   
// 0 0 0 0 0 
//
//int main() {
//    int n; cin >> n;
//   for (int i = 0; i < n; i++) {
//       for (int j = 0; j < n; j++)
//           cout << min(min(i, j), min(n - 1 - i, n - 1 - j)) << " ";
//       cout << endl;
//   }
//  return 0;
//}
// 
// Template kullanarak küçükten büyüğe sıralama yapma
//template<typename T>
//void bubbleSort(T d[], int n) {
//    for (int i = 0; i < n - 1; i++)
//        for (int j = 0; j < n - 1 - i; j++)
//            if (d[j] > d[j + 1]) swap(d[j], d[j + 1]);
//}
//int main() {
//    int d[] = { 3,5,7,6,4,8,1 };
//    int n = 7;
//    bubbleSort(d, n);
//    for (int i = 0; i < n; i++) cout << d[i] << " ";
//}
// 
// İlçeler verilmiş ve bu ilçeleri harf sırasına göre sıralama yapma 
//int main() {
//    set<string> s = { "ERCİŞ","MURADİYE","TUŞBA","ÖZALP","BAŞKALE","TUŞBA","GEVAŞ","ERCİŞ","EDREMİT" };
//    for (auto x : s) cout << x << " ";
//    return 0;
//}
// 
// 
// 
//int main() {
//    vector<int> v(10);
//    srand(time(0));
//    for (int& x : v) x = rand() % 100 + 1;
//    sort(v.begin(), v.end());
//    for (int x : v) cout << x << " "; cout << endl;
//    int ara; cin >> ara;
//    int l = 0, r = 9, b = -1;
//    while (l <= r) {
//        int m = (l + r) / 2;
//        if (v[m] == ara) { b = m; break; }
//        if (v[m] < ara) l = m + 1; else r = m - 1;
//    }
//    if (b != -1) cout << "Bulundu: " << b << endl;
//    else cout << "Yok\n";
//    return 0;
//}
// buble sort
//int main() {
//    vector<int> v = { 5,3,8,1,6 };
//    for (int i = 0; i < v.size() - 1; i++)
//        for (int j = 0; j < v.size() - 1 - i; j++)
//            if (v[j] > v[j + 1]) swap(v[j], v[j + 1]);
//    for (int x : v) cout << x << " ";
//    return 0;
//}
// insertion sort
// int main() {
//vector<int> v = { 5, 3, 8, 1, 6 };
//for (int i = 1; i < v.size(); i++) {
//    int key = v[i];
//    int j = i - 1;
//    while (j >= 0 && v[j] > key) {
//        v[j + 1] = v[j];
//        j--;
//    }
//    v[j + 1] = key;
//}
//for (int x : v) cout << x << " ";
//return 0;
//}
// selection sort
// int main() {
//vector<int> v = { 5, 3, 8, 1, 6 };
//for (int i = 0; i < v.size() - 1; i++) {
//    int minIdx = i;
//    for (int j = i + 1; j < v.size(); j++) {
//        if (v[j] < v[minIdx])
//            minIdx = j;
//    }
//    if (minIdx != i)
//        swap(v[i], v[minIdx]);
//}
//for (int x : v) cout << x << " ";
//return 0;
//}
// 
//int main() {
//    vector<string> ad; vector<double> fiyat; vector<int> stok;
//    int n; cin >> n;
//    for (int i = 0; i < n; i++) {
//        string s; double f; int t;
//        cin >> s >> f >> t;
//        ad.push_back(s); fiyat.push_back(f); stok.push_back(t);
//    }
//    for (int i = 0; i < n; i++) cout << ad[i] << " " << fiyat[i] << " " << stok[i] << endl;
//    return 0;
//}
//int main() {
//    vector<string> ad; vector<double> fiyat; vector<int> stok;
//    int n; cin >> n;
//    for (int i = 0; i < n; i++) {
//        string s; double f; int t;
//        cin >> s >> f >> t;
//        ad.push_back(s); fiyat.push_back(f); stok.push_back(t);
//    }
//    ofstream dosya("urunler.txt");
//    for (int i = 0; i < n; i++) dosya << ad[i] << "," << fiyat[i] << "," << stok[i] << endl;
//    dosya.close();
//    return 0;
//}
//
//int main() {
//   map<char, double(*)(double, double)> op;
//   op['+'] = [](double a, double b) {return a + b; };
//    op['-'] = [](double a, double b) {return a - b; };
//    op['*'] = [](double a, double b) {return a * b; };
//    op['/'] = [](double a, double b) {return a / b; };
//    double x, y; char ch;
//    cin >> x >> ch >> y;
//    if (op.count(ch)) cout << op[ch](x, y) << endl;
//    else cout << "Hatali islem\n";
//    return 0;
//}
//int main() {
//    queue<int> musteriKuyrugu;
//    int musteriSayisi, numara;
//
//    cout << "Kac musteri gelecek? ";
//    cin >> musteriSayisi;
//
//    // Müşteri numaralarını sırayla kuyruğa ekle
//    for (int i = 0; i < musteriSayisi; i++) {
//        cout << i + 1 << ". musterinin numarasini girin: ";
//        cin >> numara;
//        musteriKuyrugu.push(numara);
//    }
//
//    cout << "\nIslem basliyor...\n";
//
//    // Kuyruktan sırayla işlem yap
//    while (!musteriKuyrugu.empty()) {
//        int mevcutMusteri = musteriKuyrugu.front(); // sıradaki müşteri
//        cout << "Musteri #" << mevcutMusteri << " islemi yapiliyor...\n";
//        musteriKuyrugu.pop(); // işlem bitince kuyruktan çıkar
//    }
//
//    cout << "\nTum musterilerin islemleri tamamlandi.\n";
//
//    return 0;
//}
//polindrom
//int main() {
//    string s;
//    cout << "Kelime: "; cin >> s;
//    int pal = 1;
//    for (int i = 0; i < s.length() / 2; i++) {
//        if (s[i] != s[s.length() - 1 - i]) {
//            pal = 0;
//            break;
//        }
//    }
//    if (pal)
//        cout << "Palindrom" << endl;
//    else
//        cout << "Palindrom degil" << endl;
//    return 0;
//}
// try caste ile negatif pozitif kontrolü
//int main() {
//   int x;
//    cout << "Pozitif bir sayi giriniz: ";
//    try {
//        cin >> x;
//        if (x < 0)
//            throw "Negatif sayi girdiniz!";
//        cout << "Sayiniz: " << x << endl;
//
//    }
//   catch (...) {
//        cout << "Hata: " << endl;
//    }
//    return 0;
//}
//
//int main() {
//    vector<int> sayilar;
//    srand(time(0));
//    for (int i = 0; i < 10; i++)
//        sayilar.push_back(rand() % 100 + 1);
//
//    sort(sayilar.begin(), sayilar.end());
//    for (int x : sayilar) cout << x << " "; cout << endl;
//
//    int ara;
//    cout << "Aranacak sayi: ";
//    cin >> ara;
//
//    if (binary_search(sayilar.begin(), sayilar.end(), ara))
//        cout << "Bulundu!" << endl;
//    else
//        cout << "Yok." << endl;
//}
//int main() {
//    vector<int> sayilar;
//    srand(time(0));
//
//    for (int i = 0; i < 10; i++)
//        sayilar.push_back(rand() % 100 + 1);
//
//    for (int x : sayilar)
//        cout << x << " ";
//    cout << endl;
//
//    int ara;
//    cout << "Aranacak sayi: ";
//    cin >> ara;
//
//    bool bulundu = false;
//    for (int x : sayilar) {
//        if (x == ara) {
//            bulundu = true;
//            break;
//        }
//    }
//
//    if (bulundu)
//        cout << "Bulundu!" << endl;
//    else
//        cout << "Yok." << endl;
//
//    return 0;
//}
//int main()
//{
//	string kelime;
//	char ilk_karakter, son_karakter;
//	cout << "Lutfen Buyuk Harflerden Olusan Bir Kelime Girin: ";
//	cin >> kelime;
//	ilk_karakter = kelime[0];
//	son_karakter = kelime[kelime.size() - 1];
//	for (int i = 1; i < kelime.size(); i++)
//	{
//		if (kelime[i] < ilk_karakter)
//		{
//			ilk_karakter = kelime[i];
//		}
//		if (kelime[i] > son_karakter)
//		{
//			son_karakter = kelime[i];
//		}
//	}
//	cout << "Alfabetik Siraya Gore Kelimenin En Onde Bulunan Karakteri: " <<
//		ilk_karakter << endl;
//	cout << "Alfabetik Siraya Gore Kelimenin En Sonda bulunan Karakteri: " <<
//		son_karakter << endl;
//	return 0;
//}
//
//
//int main() {
//    string kelime;
//    cout << "Lutfen Buyuk Harflerden Olusan Bir Kelime Girin: ";
//    cin >> kelime;
//
//    char ilk_karakter = *min_element(kelime.begin(), kelime.end());
//    char son_karakter = *max_element(kelime.begin(), kelime.end());
//
//    cout << "Alfabetik Siraya Gore Kelimenin En Onde Bulunan Karakteri: "
//        << ilk_karakter << endl;
//    cout << "Alfabetik Siraya Gore Kelimenin En Sonda Bulunan Karakteri: "
//        << son_karakter << endl;
//
//    return 0;
//}
//int main() {
//    string a, b;
//    cout << "1. string: "; cin >> a;
//    cout << "2. string: "; cin >> b;
//    if (a.length() > b.length())
//        cout << "Daha uzun: " << a << endl;
//    else if (b.length() > a.length())
//        cout << "Daha uzun: " << b << endl;
//    else
//        cout << "Uzunluklar esit." << endl;
//    return 0;
//}
//int main() {
//    int d[4];
//
//    cout << "4 adet sayi giriniz:\n";
//    for (int i = 0; i < 4; i++)
//        cin >> d[i];
//
//    sort(d, d + 4);  // Küçükten büyüğe sıralanır
//
//    cout << "En buyuk ikinci: " << d[2] << endl;  // Sıralı dizide sondan bir önceki eleman
//    return 0;
//}
//int main() {
//    map<string, int> notlar;
//
//    for (int i = 0; i < 3; i++) {
//        string isim;
//        int notu;
//        cout << "Öğrenci adı: ";
//        cin >> isim;
//        cout << "Notu: ";
//        cin >> notu;
//        notlar[isim] = notu;
//    }
//
//    string enYuksekOgrenci;
//    int enYuksekNot = -1;
//
//    for (auto& p : notlar) {
//        if (p.second > enYuksekNot) {
//            enYuksekNot = p.second;
//            enYuksekOgrenci = p.first;
//        }
//    }
//
//    cout << "En yüksek not: " << enYuksekOgrenci << " - " << enYuksekNot << endl;
//    return 0;
//}
