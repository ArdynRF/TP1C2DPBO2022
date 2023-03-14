# TP1C2DPBO2022
### Saya Ardyn Rezky Fahreza NIM 2103551 mengerjakan Tugas Praktikum 1 dalam mata kuliah Desain dan Pemrograman Berorientasi Objek untuk keberkahanNya maka saya tidak melakukan kecurangan seperti yang telah dispesifikasikan. Aamiin.

## Desain Program
Program didesain menjadi 9 class:
* **Human**
* **Mahasiswa**
* **Dosen**
* **Asisten Dosen**
* **Organisasi**
* **Proker**
* **Laptop**
* **Buku**
* **Spidol**

Pada class `Human` terdapat tiga atribut:
* **nama**               -> merupakan nama human, tipe data `string`
* **usia**               -> merupakan Usia human, bertipe data `int`
* **jenis_kelamin**      -> merupakan jenis kelamin human, bertipe data `string`\
class ini memiliki 3 method:
* **makan()**            -> method untuk aktifitas makan human
* **minum()**            -> method untuk aktifitas minum human
* **tidur()**            -> method untuk aktifitas tidur human

Kemudian pada class `Mahasiswa` merupakan pewarisan dari class `Human`, karena Mahasiswa dan human merupakan objek yang sama
pada class `Mahasiswa` memiliki tiga atribut:
* **NIM**                  -> merupakan NIM mahasiswa, tipe data `string`
* **fakultas**             -> merupakan fakultas mahasiswa, tipe data `string`
* **prodi**                -> merupakan prodi mahasiswa, tipe data `string`
class ini memiliki 1 method:
* **buat_proker()**          -> ketika nilai organisasi != null maka method ini dapat dilakukan

Lalu pada class `Dosen`, merupakan pewarisan dari class `Human`
pada class 'Mahasiswa' terdapat tiga atribut:
* **NIP**               -> merupakan NIP dosen, tipe data `string`
* **fakultas**          -> merupakan fakultas dosen, tipe data `string`
* **prodi**             -> merupakan program studi dosen, tipe data `string`
* **matkul**            -> merupakan mata kuliah dosen, tipe data `string`
class ini memiliki 1 method:
* **memberi_nilai()**       -> ketika nilai approve dari asisten dosen sudah True maka dosen dapat memberikan nilai kepada mahasiswa.

Lalu pada class `AsistenDosen`, merupakan pewarisan dari class `Mahasiswa`
pada class 'AsistenDosen' terdapat dua atribut:
* **matkul**          -> merupakan mata kuliah asisten dosen, tipe data `string`
* **approve**         -> merupakan persetujuan asisten dosen terhadap nilai, tipe data `boolean`
class ini memiliki 1 method:
* **IsApprove()**       -> method untuk menyetujui nilai dari dosen dengan mengubah approve menjadi True

Class `Organisasi`, merupakan kelas yang bukan pewarisan dari kelas manapun.
pada class 'Organisasi' terdapat dua atribut:
* **nama_organisasi**       -> merupakan nama organisasi, tipe data `string`
* **lingkungan**            -> merupakan lingkungan organisasi, tipe data `string`
class ini memiliki 2 method:
* **lakukan_evaluasi()**    -> method untuk melakukan evaluasi terhadap seluruh proker yang ada
* **menyelesaikan_proker()** -> method untuk menyelesaikan proker dengan mengganti status proker menjadi True

lalu 3 kelas lainnya yakni class `Spidol`, `Buku`, dan `Laptop`
ketiga kelas ini memiliki 2 atribut yang hampir sama yakni:
* **id**                -> id untuk barang-barang tersebut
* **merek/judul**       -> merek/judul barang-barang tersebut.

### Hubungan Inheritance
Didalam kode ini hubungan inheritance hanya dimiliki class `Human` dan anak-anaknya, yakni:

Class `Human` merupakan parent dari class `Dosen` dan `Mahasiswa`.
Lalu class `Mahasiswa` memiliki subclass yakni `AsistenDosen`, class ini merupakan subclass dari class `Mahasiswa` dikarenakan asisten dosen merupakan mahasiswa yang mengajar membantu dosen.

### Hubungan Composite
1. Pertama hubungan composite mahasiswa dengan class barang barang untuk belajar seperti class `buku` dan `laptop`, mahasiswa dapat memiliki lebiih dari satu barang tersebut maka class `Mahasiswa` memiliki array of object dari kelas tersebut.
2. Kedua hubungan composite class `Mahasiswa` dengan `Organisasi` hubungan mereka yakni Mahasiswa has a Organisasi.
3. hubungan class `Organisasi` dengan `Proker` di dalam organisasi terdapat banyak proker maka dari class organisasi memiliki array of object dari class proker.
4. hubungan class `Dosen` dengan class barang barang untuk mengajar seperti class `Spidol` dan `Laptop`, dosen dapat memiliki lebih dari satu barang tersebut maka class dosen memilki array of object dari kelas tersebut.
5. Terakhir hubungan class `Dosen` dengan `AsistenDosen` sebenarnya dosen dapat memiliki lebih dari 1 asisten namun disini saya membuat design dosen hanya memiliki satu asisten.

##Alur Program
Inputan untuk program ini dibuat dengan HardCode dan sudah memiliki tampilan.
syarat-syarat seperti evaluasi tidak dapat dilakukan ketika proker sudah selesai dan dosen tidak dapat memberi nilai tanpa persetujuan dari asisten dosen terdapat dalam kode ini.
