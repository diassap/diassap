#include <iostream>
#include <string>
#include <cstdlib>
#include <ctime>

// Fungsi untuk menampilkan pesan cinta secara acak
void tampilkanPesanCinta() {
    std::string pesanCinta[] = {
        "Kamu adalah alasan aku tersenyum setiap hari.",
        "Setiap detik bersamamu adalah kenangan yang tak terlupakan.",
        "Aku sangat beruntung memilikimu dalam hidupku.",
        "Kamu adalah matahari yang mencerahkan hariku.",
        "Cinta kita lebih kuat dari apapun yang ada di dunia ini."
    };

    int jumlahPesan = sizeof(pesanCinta) / sizeof(pesanCinta[0]);
    int indexAcak = rand() % jumlahPesan;
    std::cout << pesanCinta[indexAcak] << std::endl;
}

int main() {
    srand(time(0)); // Inisialisasi generator angka acak
    std::string namaPacar;
    int pilihan;

    std::cout << "Hai cinta! Siapa namamu? ";
    std::getline(std::cin, namaPacar);

    std::cout << "Halo, " << namaPacar << "! Selamat datang di program cinta ini. ??" << std::endl;
    std::cout << "Apa yang ingin kamu lakukan hari ini?" << std::endl;
    std::cout << "1. Lihat pesan cinta\n2. Tutup program\n";
    
    std::cin >> pilihan;

    while (pilihan != 2) {
        if (pilihan == 1) {
            tampilkanPesanCinta();
        } else {
            std::cout << "Pilihan tidak valid. Silakan pilih lagi." << std::endl;
        }

        std::cout << "\nApa yang ingin kamu lakukan selanjutnya?" << std::endl;
        std::cout << "1. Lihat pesan cinta lagi\n2. Tutup program\n";
        std::cin >> pilihan;
    }

    std::cout << "Terima kasih telah menggunakan program cinta ini, " << namaPacar << "! Semoga harimu indah! ??" << std::endl;
    return 0;
}

<!---
diassap/diassap is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
