## NAMA  : ADINDA AULIA NABILA PUTRI

## NIM   : 312410309

## KELAS : TI.24.A.4 




# TUGAS PRAKTIKUM 

  ![Screenshot (91)](https://github.com/user-attachments/assets/05e1be8a-3bfe-4a74-b8f8-2f8b6befd7f9)


![code 3](https://github.com/user-attachments/assets/d805f1a9-6f34-4d89-bd0e-414bcdc219ff)




# Lab-8.py

```PYTHON
class Mahasiswa:
    def __init__(self, nama, nilai):
        self.nama = nama
        self.nilai = nilai

class DaftarNilaiMahasiswa:
    def __init__(self):
        self.daftar_nilai = {}

    def tambah(self, nama, nilai):
        """Menambahkan data mahasiswa"""
        self.daftar_nilai[nama] = Mahasiswa(nama, nilai)
        print(f"Data {nama} berhasil ditambahkan.")

    def tampilkan(self):
        """Menampilkan data mahasiswa"""
        print("Daftar Nilai Mahasiswa:")
        for mahasiswa in self.daftar_nilai.values():
            print(f"Nama: {mahasiswa.nama}, Nilai: {mahasiswa.nilai}")

    def hapus(self, nama):
        """Menghapus data mahasiswa berdasarkan nama"""
        if nama in self.daftar_nilai:
            del self.daftar_nilai[nama]
            print(f"Data {nama} berhasil dihapus.")
        else:
            print(f"Data {nama} tidak ditemukan.")

    def ubah(self, nama, nilai_baru):
        """Mengubah data mahasiswa berdasarkan nama"""
        if nama in self.daftar_nilai:
            self.daftar_nilai[nama].nilai = nilai_baru
            print(f"Data {nama} berhasil diubah.")
        else:
            print(f"Data {nama} tidak ditemukan.")
            
daftar_nilai = DaftarNilaiMahasiswa()

while True:
    print("\nMenu:")
    print("1. Tambah Data")
    print("2. Tampilkan Data")
    print("3. Hapus Data")
    print("4. Ubah Data")
    print("5. Keluar")

    pilihan = input("Pilih menu: ")

    if pilihan == "1":
        nama = input("Masukkan nama: ")
        nilai = input("Masukkan nilai: ")
        daftar_nilai.tambah(nama, nilai)
    elif pilihan == "2":
        daftar_nilai.tampilkan()
    elif pilihan == "3":
        nama = input("Masukkan nama: ")
        daftar_nilai.hapus(nama)
    elif pilihan == "4":
        nama = input("Masukkan nama: ")
        nilai_baru = input("Masukkan nilai baru: ")
        daftar_nilai.ubah(nama, nilai_baru)
    elif pilihan == "5":
        break
    else:
        print("Pilihan tidak valid.")
````

# Penjelasan code 

* DaftarNilaiMahasiswa adalah kelas yang mengelola daftar mahasiswa. kelas memiliki metode untuk menambah, mengubah, menghapus, dan menampilkan daftar nilai mahasiswa.
* Method tambah(self, nama, nilai), Menambah data mahasiswa baru kedalam daftar.
* Method tampilkan(self), menampilkan semua data mahasiswa yang tersimpan dalam daftar.
* Method hapus(self, nama), menghapus data mahasiswa berdasarkan nama.
* Method ubah(self, nama, nilai_baru), mengubah nilai mahasiswa yang sudah ada berdasarkan nama.
* Metode daftar_nilai menampilkan daftra nilai semua mahasiswa.

Mencetak menu dengan lima opsi yang dapat dipilih pengguna tersebut:

* Tambah data : untuk menmbah data mahasiswa baru.
* Tampilkan data : untuk menampilkan semua data mahasiswa yang telah dimasukkan.
* Hapus data : menghapus data mahasiswa berdasarkan nama.
* Ubah data : mengubah nilai mahasiswa berdaskan nama.
* Keluar : keluar dari program. 

Berikut Diagram Class : 

  ![Screenshot (93)](https://github.com/user-attachments/assets/14a3d951-d832-4c22-9cf6-57c6249e038b)


Berikut Flowchartnya : 

   ![flowchart_mahasiswa](https://github.com/user-attachments/assets/f382358b-982b-4a4b-84c8-6001e40e3520)










