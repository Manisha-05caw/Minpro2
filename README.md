# Minpro2
Nama : Syawe Manisha P. Siregar
NIM  : 2409116058

# Flowchart
![Flowchart Minpro(2) drawio (1)](https://github.com/user-attachments/assets/6ec46487-381c-4af3-bee6-c625606e8444)


# Input
![Screenshot 2024-10-15 004118](https://github.com/user-attachments/assets/9c9a8635-ee0a-440f-bc5e-fee094f4bc8c)
Program di atas adalah proram yang menampilkan menu utama yang terdapat pada website AIS Unmul. Program tersebut menawarkan 3 pilihan kepada user yaitu sebagai Admin, sebagai Mahasiswa, dan Program untuk keluar dari website.
Program main -> merupakan program yang dijalankan terlebih dahulu ketika program dimulai, sehingga tidak berpengaruh jika di letakkan di atas maupun di bawah.
while True -> merupakan program untuk melakukan looping. Loop akan tetap berjalan sampai pengguna memilih opsi 3, dikarenakan opsi 3 telah diakhiri program break yang dapat menghentikan looping.

![Screenshot 2024-10-15 033119](https://github.com/user-attachments/assets/bf94ac98-320d-4892-995d-77d3ca8b10de)


Selanjutnya, Mencetak menu utama dengan opsi:
1. Admin -> jika memilih opsi 1 maka pengguna akan di arahkan oleh program untuk melakukan login. Program akan mengarahkan pengguna ke Menu Admin

![Screenshot 2024-10-15 012653](https://github.com/user-attachments/assets/571a4bf7-280f-4a16-a56a-f2008ee77b70)

Di Menu Admin, pengguna akan diarahkan untuk menginput Username dan Password.

![Screenshot 2024-10-15 013015](https://github.com/user-attachments/assets/bbebfa5e-c9c5-4e6c-826a-de2b7582a47a)

Kemudian, jika input dari username dan password benar maka program akan mencetak "Login berhasil.". Program berjalan melakukan looping dengan opsi program menu admin yaitu: 1. Menampilkan semua mata kuliah
                          2. Tambah Daftar Mata Kuliah
                          3. Update Mata Kuliah
                          4. Hapus Mata Kuliah
                          5. Keluar -> Program akan mencetak " Anda memerlukan login kembali." yang kemudian program berhenti berjalan karena diakhiri oleh break.
Namun, jika pengguna menginput diluar dari pilihan tersebut (else) maka program akan mencetak "Pilihan tidak valid, silahkan coba lagi."
                  
![Screenshot 2024-10-15 014430](https://github.com/user-attachments/assets/fe429136-ae3c-4869-a470-c6edf5e33336)

Pengguna melakukan kesalahan dalam penginputan Username atau Password, sehingga program berjalan sebagai 'else' dan mencetak "Username dan Password salah, coba lagi."

Selanjutnya, program akan berjalan sesuai dengan opsi yang dipilih oleh pengguna. Anggap saja pengguna mencoba satu per satu opsi yang ada pada menu Admin.
Pengguna menginput opsi 1 pada menu admin

![Screenshot 2024-10-15 015540](https://github.com/user-attachments/assets/0e3551cd-8b05-479d-a1de-c3e7824f32eb)

Program Definisi digunakan untuk mendefinisikan fungsi tampilkan_semua_matkul():
Nah, Program ini dibuat menggunakan tabel agar penempatannya lebih rapi.
Prettytable merupakan library dalam program python yang bertujuan agar menampilkan data format tabel yang terstruktur sehingga terlihat rapi dan mudah dibaca.
Pada fungsi tampilkan semua matkul ini program akan menyajikan data dalam tabel.

Pengguna menginput Opsi 2 

![Screenshot 2024-10-15 015540](https://github.com/user-attachments/assets/ad2c09bf-1531-4cdd-a13a-ff155342dc30)

Program def mendefinisikan fungsi tambah_matkul():
untuk melakukan penambahan matkul perlu melakukan penginputan kode_matkul, nama_matkul dan sks.
Untuk melakukan penambahan matkul diperlukan untuk memasukkan kode serta nama matkul agar dapat di masukkan dalam KRS. Setelah menginput keduanya, maka matkul berhasil ditambah.

Pengguna menginput Opsi 3

![Screenshot 2024-10-15 021729](https://github.com/user-attachments/assets/499788b1-7be1-477e-ab48-15cd84babd35)

Program def untuk mendefinisikan fungsi update_matkul():
Untuk melakukan update matkul pengguna perlu menginput kode matkul, kemudian pengguna dapat memasukkan nama baru atau tetap menggunakan nama lama dan juga dapat memperbarui SKS atau tetap dengan SKS yang lama. Di akhir Program akan mencetak "Mata kuliah berhasil diperbarui"

Pengguna menginput opsi 4

![Screenshot 2024-10-15 022721](https://github.com/user-attachments/assets/17fbb7d1-46f3-47ca-b9b1-6b0af09174bb)

Program def digunakan untuk mendefinisikan fungsi hapus_matkul():
Untuk menghapus matkul perlu menginput kode matkul.
Fungsi hapus_matkul() digunakan untuk menghapus mata kuliah dari daftar berdasarkan kode yang dimasukkan pengguna. Cara kerjanya yaitu:
- Meminta input kode mata kuliah yang ingin dihapus.
- Menggunakan variabel global semua_mata_kuliah (daftar semua mata kuliah).
  Perintah ini digunakan untuk memberitahukan Python bahwa kita ingin mengakses dan memodifikasi variabel global "semua_mata_kuliah."
- Membuat daftar baru yang berisi semua mata kuliah kecuali yang kodenya sesuai dengan input pengguna.
- Menampilkan pesan konfirmasi kalau mata kuliah dengan kode tersebut sudah dihapus.

Pengguna menginput opsi 5
Program akan mencetak "Anda memerlukan login kembali.", kemudian program akan kembali ke menu utama.


2. Mahasiswa -> jika memilih opsi 2 maka pengguna akan diarahkan oleh program ke menu Mahasiswa. Program akan mengarahkan pengguna untuk login sebagai mahasiswa

![Screenshot 2024-10-15 024110](https://github.com/user-attachments/assets/5353bf86-0d74-459d-aabf-f7f9e16fa007)

Program def digunakan untuk mendefinisikan fungsi login_mahasiswa():
kemudian while True digunakan untuk melakukan looping jika username dan password benar, program akan mencetak "Login berhasil.", program juga akan berjalan ke tahap selanjutnya dan jika input username atau password salah, program akan mencetak "Username atau password salah, silahkan coba lagi" dan program akan kembali ke login mahasiswa.

![image](https://github.com/user-attachments/assets/f417bf32-23ec-41a6-8e1c-e35198523d85)

Program def digunakan untuk mendefinisikan fungsi menu_mahasiswa():
while True digunakan agar program dapat berjalan secara berulang, hingga pengguna memilih opsi 4 karena terdapat break yang dapat menghentikan looping.
Jika pengguna menginput diluar opsi (1-4), maka program yang berjalan akan mencetak "Pilihan tidak valid, coba lagi".


   ![Screenshot 2024-10-15 025919](https://github.com/user-attachments/assets/dc194e96-9584-4c35-b0e4-8ff5f608dd82)

Program def mendefiniskan fungsi tambah_ke_krs():
untuk menambahkan matkul ke krs perlu menginput kode matkul. Jika kode yang di input benar maka program akan mencetak nama matkul yang berhasil ditambah ke dalam krs dan jika kode yang di input tidak sesuai maka program akan mencetak "mata kuliah tidak ditemukan".

Kemudian program def untuk mendefinisikan fungsi tampilkan_krs():
membuat format pada tabel yaitu kode, nama mata kuliah dan sks,
setelah semua mata kuliah ditambahkan ke dalam tabel, fungsi mencetak judul "Daftar Semua Mata Kuliah" diikuti dengan isi tabel yang sudah diformat.

3. Keluar -> jika memilih opsi 3 maka pengguna akan diarahkan oleh program untuk keluar dari website dan program berakhir.

# Output

![Screenshot 2024-10-15 033611](https://github.com/user-attachments/assets/5bf6f9c0-b5dc-4adc-a61e-03cdc7cd4aab)

Gambar diatas merupakan output original dari input tampilkan semua matkul.

![Screenshot 2024-10-15 033703](https://github.com/user-attachments/assets/89e7208a-ec2f-4da3-a357-2a251245bd1e)

Gambar diatas merupakan output hasil tambah, update dan hapus matkul
output tambah akan menambahkan mata kuliah
output update akan memperbarui mata kuliah
output hapus akan menghapus mata kuliah dari krs

![Screenshot 2024-10-15 033808](https://github.com/user-attachments/assets/e3970830-eab7-4265-bef3-6024669101ed)

Gambar diatas merupakan hasil rombak dari program yang telah dilakukan sebelumnya seperti penambahan matkul, perbarui matkul dan penghapusan matkul
kemudian opsi 5 yaitu keluar, program akan keluar dari menu admin dan harus melakukan pemilihan user.

![Screenshot 2024-10-15 034831](https://github.com/user-attachments/assets/33142b55-5be2-4825-a600-8ef7bce14994)
Kemudian di opsi 2 kita memasuki user mahasiswa
seperti sebelumnya program menampilkan Daftar semua mata kuliah

![Screenshot 2024-10-15 035314](https://github.com/user-attachments/assets/113db42a-68c2-4de2-93ca-cdae59b36ff3)

Tidak seperti penambahan matkul di menu admin, di menu mahasiswa hanya bisa menginput matkulnya ke dalam krs tetapi tidak melakukan penambahan matkul

Opsi 4 melakukan program keluar dari menu Mahasiswa dan kembali ke menu utama.
Di menu utama terdapat opsi 3 untuk menghentikan program secara permanen.


