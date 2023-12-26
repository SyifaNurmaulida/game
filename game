## 1.1 Latar Belakang
Game ini dibuat untuk memenuhi salah satu tugas pada mata kuliah Praktikum Dasar Pemograman sebagai tugas Ulangan Tengah Semester (UTS) dan Ujian AKhir Semester (UAS).
## 1.2 Deksripsi dan alur cerita game
Game ini memperesentasikan tentang permainan petualangan roket luar angkasa.Dimana roket tersebut mulai naik ke atas melewati rintangan meteor yang berjatuhan. Permainan berlangsung hingga roket bisa atau berhasil menghindari 8 meteor yang jatuh sampai ke garis finish dan permainan pun selesai.
## 1.3 Branding game
- Nama Game = Rocket Game
- Tareget pengguna =
  - Game ini bisa dimainkan dari kalangan anak-anak sampai dewasa
- Genre: Adventure
## 1.4 User Story
Sebagai | Saya ingin bisa | Sehingga | Prioritas
---|---|---|---
Pengguna | Menggerakan roket | Roket bisa bergerak naik | ⭐⭐⭐⭐⭐
Pengguna | Menhingdari hambatan meteor| roket bisa menghindari meteor untuk bisa finish |  ⭐⭐⭐⭐⭐
Sistem | Membuat hambatan | Mempersulit roket supaya bisa menghindari 8 kali meteor yang jatuh| ⭐⭐⭐⭐⭐
## 1.5 Desain User Interface
![WhatsApp Image 2023-12-25 at 19 59 46_0076851a](https://github.com/SyifaNurmaulida/UTS-UAS-PDP/assets/145275738/710d6080-fbff-4a09-b6ab-b578a408e07b)
![WhatsApp Image 2023-12-25 at 19 59 46_ad7fa9e9](https://github.com/SyifaNurmaulida/UTS-UAS-PDP/assets/145275738/0027cd46-1b37-4d7a-b265-08be461e0c49)
![WhatsApp Image 2023-12-25 at 19 59 47_5bd0ac8d](https://github.com/SyifaNurmaulida/UTS-UAS-PDP/assets/145275738/6ef2cb7e-246a-49d5-879a-a371ceb3e379)
## 1.6 Flowchart
<img width="284" alt="Screenshot 2023-12-25 121035" src="https://github.com/SyifaNurmaulida/UTS-UAS-PDP/assets/145275738/faf4fe9e-385b-48e4-a01f-02433769fadb">

## 1.7 Link Demo game

## 1.8 Kode Pemograman Game
import java.util.Scanner;
// deklarasi penggunaan class scanner untuk mengambil input pengguna
public class gameroket {
// class utama
    static class Roket {
        private int posisi;
        //variabel posisi:menyimpan posisi roket
        public Roket() {
            this.posisi = 0;
        // inisialisasi posisi roket ke nilai awal(0)
        }   

        public void naik() { 
            //method,menaikkan posisi roket setiap dipanggil
            this.posisi++;
        }

        public int getPosisi() {
            return this.posisi;
            //method mengembalikan nilai posisi roket
        }
    }

    public static void main(String[] args) { //method utama yang dijalankan saat program dimulai
        int meteorDihindari = 0; //jumlah meteor yang berhasil dihindari
        int meteorDiperlukan = 8; //jumlah meteor yang harus dihindari untuk mencapai finish
        boolean gameOver = false; //status permainan (false selama game berlangsung,true saat game berakhir)

        System.out.println("Selamat datang di Game Roket Luar Angkasa!");
        System.out.println("Hindari meteor untuk mencapai finish.");
        // perintah menampilkan pesan dan perintah menghindari meteor
        Roket roket = new Roket();
        //objek roket yang digunakan dalam permainan
        Scanner scanner = new Scanner(System.in);

        while (!gameOver) { //loop utama yang berjalan selama gameover nya masih false
            displayGame(roket.getPosisi(), meteorDihindari);
            System.out.println("Pilih tindakan Anda:");
            System.out.println("1. Naik ke atas");
            System.out.println("2. Keluar");
            // pilihan untuk pemain memilih tindakan
            int pilihan = scanner.nextInt();
            // pilihan diinput dengan scanner
            switch (pilihan) { //switch untuk aksi pemain (pengondisian if/else)
                case 1:
                    if (Math.random() < 0.4) { //kemungkinan bertemu meteor 40%
                        System.out.println("Anda bertemu dengan meteor! Roket rusak!");
                        //perintah menampilkan pesan "jika bertemu meteor maka roket akan rusak"
                        meteorDihindari++; //jumlah meteor yang dihindari bertambah
                        System.out.println("Meteor yang dihindari: " + meteorDihindari);
                        //perintah menampilkan pesan
                        if (meteorDihindari >= meteorDiperlukan) { //pengondisian(if)jika mencapai jumlah meteor yang 
                                 diperlukan
                            System.out.println("Anda berhasil menghindari semua meteor! Selamat, Anda mencapai finish!");
                            gameOver = true;
                        } else {
                            System.out.println("Lanjutkan mencari jalan keluar.");
                        }
                    } else {
                        roket.naik();
                        System.out.println("Anda berhasil naik ke atas.");
                    }
                    break;
                    //pemain berhasil sampai finish
                case 2:
                    System.out.println("Anda keluar dari permainan.");
                    gameOver = true;
                    break;
                    //keluar dari permainan
                default:
                    System.out.println("Pilihan tidak valid. Silakan pilih kembali.");
                    break;
                    //jika pemain memilih pilihan lain,maka akan muncul pilihan tidak valid
            }
        }

        scanner.close(); //menutup objek scanner yang digunakan
    }

    private static void displayGame(int roketPosisi, int meteorsAvoided) {
        // Menampilkan roket dan meteor yang dihindari
        for (int i = 0; i < 10; i++) {
        //loop(for dari 0-9)
            if (i == roketPosisi) {
                System.out.print("R");
                //jika i=roketPosisi,makan akan muncul R=
            } else {
                System.out.print("-");
                //jika pengecualian diatas tidak jalan akan muncul simbol(-)
            }
        }
        System.out.println();

        // Menampilkan meteor yang dihindari
        System.out.print("Meteor dihindari: ");
        for (int i = 0; i < meteorsAvoided; i++) { //loop(for 0 hinnga meteorsAvoided -1)
            System.out.print("* ");// karakter representasi meteor (jumlah meteor)
        }
        System.out.println();
    }
}
  
## 2. konsep variable, data type dan operator pada bahasa pemrograman digunakan dalam pembuatan game ini
game ini memanfaatkan variabel-variabel seperti posisi,meteorDihindari, meteorDiperlukan dan gameOver digunakan untuk melacak informasi seperti roket, jumlah meteor, jumlah meteor yang diperlukan dan status game.
- Tipe data seperti int digunakan untuk menyimpan bilangan bulat, boolean untuk menyimpan nilai kebenaran (true/false), dan String untuk menyimpan teks. Contohnya adalah int meteorDihindari = 0;, yang mendeklarasikan variabel meteorDihindari dengan tipe data int.
- Operator: Operator digunakan untuk melakukan operasi pada variabel dan nilai. Dalam game ini, operator seperti ++ digunakan dalam method naik() untuk menaikkan nilai posisi roket. Operator logika seperti < (kurang dari) digunakan dalam kondisi if (Math.random() < 0.4) untuk menentukan kemungkinan bertemu meteor.
## 3. konsep boolean dan conditions pada bahasa pemrograman digunakan dalam pembuatan game ini
-Boolean: Dalam game di atas, variabel gameOver merupakan contoh tipe data boolean yang menunjukkan status permainan. Saat gameOver bernilai false, permainan berlanjut; saat bernilai true, permainan berakhir.
-Conditions :
- Dalam game ini, if (Math.random() < 0.4) adalah contoh dari pernyataan kondisional. Ini mengevaluasi apakah nilai acak yang dihasilkan kurang dari 0.4, dan jika benar, pemain bertemu dengan meteor, mengakibatkan roket rusak.
- Pernyataan if (meteorDihindari >= meteorDiperlukan) juga merupakan pernyataan kondisional. Jika jumlah meteor yang dihindari sudah mencapai atau melebihi jumlah yang diperlukan, permainan berakhir dengan pesan bahwa pemain berhasil mencapai finish.
- Pernyataan switch (pilihan) digunakan untuk menentukan aksi berdasarkan pilihan input pengguna. Misalnya, jika pemain memilih 1, maka kondisi case 1 akan dieksekusi, dan sebaliknya.
## 4. konsep looping dan array pada bahasa pemrograman digunakan dalam pembuatan game ini
- While loop digunakan untuk menjalankan blok pernyataan di dalamnya selama kondisi !gameOver masih bernilai true. Ini memastikan bahwa game berlanjut selama gameOver masih false.For loop digunakan untuk membuat iterasi dari 0 hingga 9 (dalam hal ini) dengan variabel kontrol i. Loop ini digunakan untuk menampilkan representasi roket pada layar, menunjukkan posisi roket.
- Meskipun bukan array, namun perulangan ini menampilkan karakter '*' sebanyak meteorsAvoided kali. yang akan menciptakan efek serupa dengan menampilkan sejumlah karakter yang mewakili meteor yang dihindari. Jadi,kita dapat membayangkan meteorsAvoided sebagai ukuran array yang menunjukkan jumlah meteor yang telah dihindari.
## 5. konsep method pada bahasa pemrograman digunakan dalam pembuatan game ini
- (public Roket(): digunakan untuk menginisialisasi objek roket yang dengan menetapkan nilai awal posisi roket yaitu 0 dan saat pertama kali dibuat.
- Void method
  (void naik(): digunakan untuk menaikkan posisi roket setiap kali dipanggil. method ini tidak bisa merubah nilai.tapi hanya bisa mengubah variabel posisi objek roket.
- Getter Method
  (GetPosisi(): digunakan untuk mengembalikan posisi roket yang bertipe data int karena nilai dari posisi roket berupa bilangan bulat.
- Main Method (public static void main(String[] args) { ... }):Method main merupakan titik awal eksekusi program.Menjalankan logika permainan dengan menggunakan objek Roket, input dari pengguna, pernyataan kondisional (if, else), dan perulangan (while).
- Display Method (private static void displayGame(int roketPosisi, int meteorsAvoided) { ... }):Method displayGame digunakan untuk menampilkan kondisi permainan seperti posisi roket dan meteor yang dihindari.Menggunakan dua parameter (roketPosisi dan meteorsAvoided) untuk menampilkan representasi grafis permainan.
## 6. konsep class pada bahasa pemrograman digunakan dalam pembuatan game ini 
Dalam game ini, terdapat kelas Roket yang mewakili objek roket.
- Atribut (private int posisi): Menyimpan informasi tentang posisi roket. Dideklarasikan sebagai variabel privat untuk kontrol akses.
- Constructor (public Roket()): Inisialisasi objek roket dengan menetapkan nilai awal posisi ke 0. Dipanggil saat objek roket pertama kali dibuat.
- Method (public void naik()): Menaikkan posisi roket setiap kali dipanggil. Memodelkan perilaku roket.Getter Method (public int getPosisi()): Mengembalikan nilai posisi roket. Memberikan akses baca ke nilai posisi.
## 7. algoritma
Dalam game Rocket Game ini  terdapat algoritma untuk mengatur jalannya permainan.
- While Loop (while (!gameOver) {...}): Mengatur loop utama permainan yang berjalan selama game belum berakhir. Setiap iterasi loop mewakili satu putaran permainan.
- Switch Statement (switch (pilihan) {...}): Menentukan aksi berdasarkan pilihan input pengguna. Dalam setiap kasus, terdapat logika untuk mengatasi kemungkinan bertemu meteor atau berhasil naik ke atas.
- Random Probability (if (Math.random() < 0.4) {...}): Menggunakan nilai acak untuk mensimulasikan kemungkinan bertemu meteor. Jika nilai acak kurang dari 0.4, pemain mengalami kerusakan roket.
- Display Method (private static void displayGame(int roketPosisi, int meteorsAvoided) {...}): Menampilkan kondisi permainan dengan representasi grafis roket dan meteor yang dihindari.
## 8. Jelaskan bagaimana game yang dibuat dapat didistribusikan dan digunakan oleh pengguna !
- Interaksi Pengguna:Program akan menampilkan pesan selamat datang dan petunjuk permainan.Pengguna dapat memilih tindakan dengan memasukkan nomor pilihan (1 untuk naik ke atas, 2 untuk keluar).
- Permainan:Roket akan ditampilkan pada layar, dan pengguna dapat memilih naik atau keluar.Ketika roket naik, ada kemungkinan bertemu meteor (40% kemungkinan).Jika bertemu meteor, roket rusak, dan jumlah meteor yang dihindari akan ditampilkan.Jika jumlah meteor yang dihindari mencapai target, permainan berakhir dengan pesan selamat.
- Keluar dari Permainan:Pengguna dapat keluar dari permainan dengan memilih opsi keluar.Program akan memberikan pesan dan berakhir.
