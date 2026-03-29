## Laporan Praktikum SISOP 

Nama : Atik Putri Matulina 

NRP : 5027251128

Kelas : Sistem Operasi A 

## SOAL_1 
diminta untuk menghitung totala penumpang, jumlah gerbong, umur tertua, rata rata usia penumpang, dan menghitung jumlah penumpang yang ada di business class
a : total penumpang yang berada di dalam kereta.

b : Jumlah gerbong penumpang.

c : umur tertua dari penumpang kereta KANJ.

d : rata rata usia penumpang kereta KANJ.

e : menghitung jumlah penumpang yang ada di business class.




awk -f KANJ.sh passenger.csv a ##untuk menghitung total penumpang kereta 

awk -f KANJ.sh passenger.csv b ##unutk menghitung jumlah gerbong  

awk -f KANJ.sh passenger.csv c ##untuk mendapatkan usia tertua penumpang yang ada di kereta 

awk -f KANJ.sh passenger.csv d ##untuk mendapatkan usia rata rata dari penumpang kereta 

awk -f KANJ.sh passenger.csv e ##untuk menghitung jumlah penumpang business class 

awk -f KANJ.sh passenger.csv f atau huruf lain selain a - e maka akan mengeluarkan output "Soal tidak dikenali. Gunakan a, b, c, d, atau e."



BEGIN {
    opsi = ARGV[2]

    if (opsi != "a" && opsi != "b" && opsi != "c" && opsi != "d" && opsi != "e") {
        print "Soal tidak dikenali. Gunakan a, b, c, d, atau e."
        print "Contoh penggunaan: awk -f file.sh data.csv a"
        exit 1
    }
}

opsi = ARGV[2] = program akan membaca argumen yang user pakai, misalnya f, lalu dicek satu persatu apakah f sama dengan "a"? tidak. Sama dengan "b"? tidak. Sama dengan "c"? tidak. Sama dengan "d"? tidak. Sama dengan "e"? tidak.
karena semua kondisi != terpenuhi, masuk ke dalam if dan langsung print pesan error lalu program berhenti.
