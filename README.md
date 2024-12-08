# modul praktikum 8
# OOP

Nama : ghefira azka fardani 

Kelas : TI.24.A5

NIM : 312410521

## praktikum 8

### - flowchart
![foto]()
### - code program

#### 1. Konstruktor ```__init__```
```phython
def __init__(self):
    self.mahasiswa = []
```
* Konstruktor ini dijalankan saat sebuah objek ```DaftarNilaiMahasiswa``` dibuat.
  
* ```self.mahasiswa = []``` berarti Anda membuat sebuah list kosong untuk menyimpan data mahasiswa nantinya.

#### 2. Metode ```tambah```
```phython
def tambah(self, nama, nilai):
    """Menambah data mahasiswa baru."""
    self.mahasiswa.append({'nama': nama, 'nilai': nilai})
    print(f"Data mahasiswa {nama} berhasil ditambahkan.")
```
* Metode ini digunakan untuk menambahkan data mahasiswa baru ke dalam daftar.
  
* Data mahasiswa disimpan dalam bentuk dictionary, di mana ```'nama'``` dan ```'nilai'``` adalah kunci yang berisi nilai yang diberikan saat pemanggilan metode.
  
* Data mahasiswa yang ditambahkan akan muncul dengan pesan: ```"Data mahasiswa {nama} berhasil ditambahkan"```.

#### 3. Metode ```tampilkan```
```phython
def tampilkan(self):
    """Menampilkan semua data mahasiswa."""
    if not self.mahasiswa:
        print("Tidak ada data mahasiswa.")
        return
    print("Daftar Nilai Mahasiswa:")
    for index, mhs in enumerate(self.mahasiswa, start=1):
        print(f"{index}. Nama: {mhs['nama']}, Nilai: {mhs['nilai']}")
```
* Metode ini digunakan untuk menampilkan semua data mahasiswa yang sudah ada.
  
* Jika daftar mahasiswa kosong, program akan menampilkan pesan ```"Tidak ada data mahasiswa"```.
  
* Jika ada data, setiap data mahasiswa ditampilkan menggunakan ```enumerate```, yang memberikan indeks untuk setiap mahasiswa, dimulai dari 1, lalu mencetak nama dan nilai mereka.

#### 4. Metode ```hapus```
```phython
def hapus(self, nama):
    """Menghapus data mahasiswa berdasarkan nama."""
    for mhs in self.mahasiswa:
        if mhs['nama'] == nama:
            self.mahasiswa.remove(mhs)
            print(f"Data mahasiswa {nama} berhasil dihapus.")
            return
    print(f"Data mahasiswa dengan nama {nama} tidak ditemukan.")
```
* Metode ini digunakan untuk menghapus data mahasiswa berdasarkan nama.

* Program akan mencari mahasiswa dengan nama yang diberikan. Jika ditemukan, mahasiswa tersebut akan dihapus dari daftar, dan pesan ```"Data mahasiswa {nama} berhasil dihapus"```. akan ditampilkan.

* Jika nama tidak ditemukan, maka akan muncul pesan ```"Data mahasiswa dengan nama {nama} tidak ditemukan"```.

#### 5. Metode ```ubah```
```phython
def ubah(self, nama, nilai_baru):
    """Mengubah data mahasiswa berdasarkan nama."""
    for mhs in self.mahasiswa:
        if mhs['nama'] == nama:
            mhs['nilai'] = nilai_baru
            print(f"Data mahasiswa {nama} berhasil diubah menjadi nilai {nilai_baru}.")
            return
    print(f"Data mahasiswa dengan nama {nama} tidak ditemukan.")
```
* Metode ini digunakan untuk mengubah nilai mahasiswa berdasarkan nama.

* Jika nama mahasiswa ditemukan dalam daftar, nilai mahasiswa tersebut akan diubah menjadi ```nilai_baru```, dan pesan perubahan akan ditampilkan.

* Jika nama mahasiswa tidak ditemukan, maka akan muncul pesan ```"Data mahasiswa dengan nama {nama} tidak ditemukan"```.

#### contoh penggunaan 
```phython
daftar_nilai = DaftarNilaiMahasiswa()
daftar_nilai.tambah("fabio", 10)
daftar_nilai.tambah("ghefira", 90)
daftar_nilai.tampilkan()
daftar_nilai.ubah("fabio", 20)
daftar_nilai.tampilkan()
daftar_nilai.hapus("ghefira")
daftar_nilai.tampilkan()
```
*Pertama, objek ```daftar_nilai``` dibuat dengan memanggil konstruktor ```DaftarNilaiMahasiswa()```.

* Kemudian, data mahasiswa ditambahkan menggunakan metode ```tambah```. ```fabio``` dengan nilai 10 dan ghefira dengan nilai 90 ditambahkan.

* Metode ```tampilkan()``` dipanggil untuk menampilkan daftar mahasiswa yang ada:

```phython
1. Nama: fabio, Nilai: 10
2. Nama: ghefira, Nilai: 90
```
* Kemudian, nilai mahasiswa ```fabio``` diubah menjadi 20 menggunakan metode ```ubah()```.

* Setelah perubahan, metode ```tampilkan()``` dipanggil lagi untuk menunjukkan perubahan nilai:

```phython
1. Nama: fabio, Nilai: 20
2. Nama: ghefira, Nilai: 90
```
* Terakhir, data mahasiswa ```ghefira``` dihapus menggunakan metode ```hapus()```, dan daftar mahasiswa ditampilkan lagi, yang menunjukkan bahwa hanya ```fabio``` yang tersisa:
```phython
1. Nama: fabio, Nilai: 20
```

#### - hasil
![foto](https://github.com/azkaa-pixel/pratikum-8/blob/77a74133fed49c6f8642180229ddabc506feb1af/hasil%208.jpeg)

