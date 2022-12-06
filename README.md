# Praktikum--6
Nama : Aas Novitasari

NIM : 312210167

Kelas : TI.22.A1


LATIHAN
Ubahlah kode di bawah ini menjadi fungsi menggunakan lambda

import math

def a(x):
return x**2

def b(x, y):
return math.sqrt(x**2 + y**2)

def c(*args):
return sum(args)/len(args)

def d(s):
return "".join(set(s))
Rumus :
# Latihan

print("Nama : Aas Novitasari")
print("NIM  : 312210167")
print("--------------------------------")

import math
def a(x):
    return x**2
    a = lambda x: x**2, a
print(a(2))

def b(x, y):
    return math.sqrt(x**2 + y**2)
    b = lambda x, y: x**2 + y**2, b
print(b(2, 4))

def c(*args):
    return sum(args) / len(args)
    c = lambda*args: sum(args) / len(args)
print(c(10, 50))

def d(s):
    return "".join(set(s))
    d = lambda s: "".join(set(s))
print(d("Aas"))

Program :

![LATIHAN](https://user-images.githubusercontent.com/116045324/205871314-d26ee70c-ad61-400c-9ad2-694757bd3aa2.PNG)


Hasil Run :

![HasilRunLATIHAN](https://user-images.githubusercontent.com/116045324/205871505-a0f3c95a-2af8-4526-8ce4-19f4d80b3b43.PNG)


Praktikum 6
Buat program sederhana dengan mengaplikasikan penggunaan fungsi yang akan menampilkan daftar nilai mahasiswa, dengan ketentuan :

Fungsi tambah() untuk menambah data.
Fungsi tampilkan() untuk menampilkan data.
Fungsi hapus(nama) untuk menghapus data berdasarkan nama.
Fungsi ubah(nama) untuk mengubah data berdasarkan nama.
Buat Flowchart dan Penjelasan Programnya pada README.md.
Commit dan push repository ke github.
Rumus :
from os import system
s_nama = []
s_nim = []
s_tugas = []
s_uts = []
s_uas = []
s_akhir = []


def judul():
    print('==================================')
    print('|     Daftar Nilai Mahasiswa     |')
    print('==================================')


def menu():
    system('cls')
    print('=====================================')
    print('Input Data Nilai Mahasiswa'.center(40))
    print('=====================================')
    print('|    1. Tambah Data                 |')
    print('|    2. Tampilkan Data Mahasiswa    |')
    print('|    3. Ubah Data Mahasiswa         |')
    print('|    4. Hapus Data Mahasiswa        |')
    print('|    5. Selesai                     |')
    print('=====================================')
    choose = input('Pilih Menu  : ')
    if choose == '1':
        tambah()
    elif choose == '2':
        tampilkan()
    elif choose == '3':
        ubah()
    elif choose == '4':
        hapus()
    elif choose == '5':
        selesai()
    else:
        tidak = input('Menu Tidak Ada')
        system('cls')
        menu()


def tambah():
    system('cls')
    judul()
    print('Tambah Data'.center(40))
    print('==================================')
    nama = input('Nama     : ')
    s_nama.append(nama)
    nim = input('NIM       : ')
    s_nim.append(nim)

    system('cls')
    judul()
    print('Tambah Data'.center(40))
    print('==================================')
    tugas = float(input('Nilai Tugas    : '))
    s_tugas.append(tugas)

    uts = float(input('Nilai UTS        : '))
    s_uts.append(uts)

    uas = float(input('Nilai UAS        : '))
    s_uas.append(uas)

    total = tugas * 0.30 + uts * 0.35 + uas * 0.35
    s_akhir.append(total)
    print('Data Tersimpan'.center(40))
    kembali = input('Kembali [Enter]')
    menu()


def tampilkan():
    system('cls')
    judul()

    for i in range(len(s_nim)):
        print('%d. Nama         : %s' % (i + 0, s_nama[i]))
        print('    NIM          : %s' % s_nim[i])
        print('    Nilai Tugas  : %.2f' % s_tugas[i])
        print('    UTS          : %.2f' % s_uts[i])
        print('    UAS          : %.2f' % s_uas[i])
        print('    Nilai Akhir  : %.2f' % s_akhir[i])
        print('-----------------------------')
    kembali = input('Kembali Tekan [Enter]')
    menu()


def ubah():
    rubah = input('Ubah Biodata Tekan [B]   : ')
    if rubah == 'B' or rubah == 'b':
        i = int(input('Masukkan Nomor Urut  : '))
        if (i > len(s_nim[i])):
            print('Nomor Urut Salah')
        else:
            namabaru = input('Nama      : ')
            s_nama[i] = namabaru
    kembali = input('Kembali Tekan [Enter]')
    menu()


def hapus():
    system('cls')
    judul()
    print('Hapus Data'.center(40))
    print('=================================')
    i = int(input('Masukkan Nomor Urut  : '))

    if (i > len(s_nim[i])):
        tidak = input('NIM Tidak Ada')
        hapus()

    else:
        s_nim.remove(s_nim[i])
        s_nama.remove(s_nama[i])
        s_tugas.remove(s_tugas[i])
        s_uts.remove(s_uts[i])
        s_uas.remove(s_uas[i])
        s_akhir.remove(s_akhir[i])

    print('Data Berhasil Di Hapus')
    kembali = input('Kembali Tekan [Enter]')
    menu()


def selesai():
    system('cls')


menu()

Program :

![PROGRAM](https://user-images.githubusercontent.com/116045324/205874239-c8a18b74-f8e6-411d-b058-171d73515e26.PNG)


Hasil Run :

Menambah data

![MENAMBAHKANDATA](https://user-images.githubusercontent.com/116045324/205874353-46282687-c29a-49c7-adf1-aa73a62ad52c.PNG)

![HASILRUNMENAMBAHKAN](https://user-images.githubusercontent.com/116045324/205874430-1c10c82e-4b3f-4893-8769-220bd6f3ef79.PNG)



Menampilkan data

![MENAMPILKANDATA](https://user-images.githubusercontent.com/116045324/205874510-581ab5c5-f126-45b6-95a8-f050e51408fe.PNG)


Mengubah data

![mengubahdata](https://user-images.githubusercontent.com/116045324/205874599-91ebf9f1-60d5-43ab-864f-d94da91d3a0c.PNG)


![mengubahdataa](https://user-images.githubusercontent.com/116045324/205874647-61c05859-628e-4e6b-b90a-65e6e1006dd9.PNG)


Menghapus data

![menghapusdata](https://user-images.githubusercontent.com/116045324/205874712-db468cde-5ab1-46b3-87f6-599494c83f0b.PNG)


Selesai

![SELESAI](https://user-images.githubusercontent.com/116045324/205876049-1577672a-ebf0-4f50-a3a1-eddfa77cc35c.PNG)


Penjelasan Program :
Definisikan dictionary terlebih dahulu data = {}.
Membuat fungsi
Fungsi tampilkan(), untuk menambahkan data def tampilkan()
Fungsi tambah(), untuk menampilkan data def tambah()
Fungsi hapus(nama), untuk menghapus nama pada data def hapus(nama)
Fungsi ubah(nama), untuk mengubah nama pada data def ubah(nama)
Menggunakan Perulangan while True: dapat diartikan perulangan akan terus mengulang jika inputan benar dan masuk kedalam proses jika tidak maka perulangan berhenti atau lanjut ke proses selanjutnya. Gunakan statement if untuk memproses perintah yang di inginkan sesuai inputan.
Untuk menambahkan data pilih "[1] Tambah" gunakan fungsi if gunakan perintah "1", lalu masukan nama, nim, tugas, uts, uas, nilaiakhir, nilai akhir didapat dari = ((tugas)*30/100 + (uts)*35/100 + (uas)*35/100.
Lalu jika ingin memilih "[2] Lihat" gunakan fungsi 'elif' dan gunakan fungsi 'for x in data.items():' untuk melihat data pada tabel data yang kita inputkan, dengan perintah "2". Jika data tidak terdaftar maka akan tampil "TIDAK ADA DATA" atau = 0.
Lalu untuk menampilan pilihan "[3] Ubah" gunakan fungsi 'elif' kemudian gunakan fungsi 'if nama in data.keys():' kemudian input nama, nim, nilai tugas, nilai uts, nilai uas untuk mengubah data nama kemudian gunakan fungsi 'else' untuk menampilkan data nama yang kita ingin ubah tidak ada.
Untuk menghapus data pilih "[4] Hapus" gunakan fungsi 'elif' kemudian gunakan fungsi 'if nama in data.keys():' kemudian fungsi 'del.data[nama] jika nama yang kita hapus tidak ada dalam tabel maka gunakan fungsi 'else' untuk menampilkan "TIDAK ADA DATA".
Untuk keluar maka gunakan fungsi else dan exit() atau gunakan perintah [5] Keluar.
Selesai.
Flowchart Praktikum 6

![FLOWCHART6](https://user-images.githubusercontent.com/116045324/205876740-9ee8d9a2-9298-4aca-87a2-1dd076ff6a10.jpg)


Sekian, Terima kasih
