# Minpro2

from prettytable import PrettyTable

# Daftar semua mata kuliah 
semua_mata_kuliah = [
    {"kode": "3W004", "nama": "Pengantar Teknologi Informasi", "sks": 3},
    {"kode": "3W002", "nama": "Dasar Dasar Pemrograman", "sks": 3},
    {"kode": "3W028", "nama": "Matematika Diskrit", "sks": 3},
    {"kode": "063W0", "nama": "Bahasa Inggris", "sks": 3},
    {"kode": "1063W", "nama": "Konsep Sistem Informasi", "sks": 3},
    {"kode": "2W002", "nama": "Pendidikan Agama MKWK", "sks": 3},
    {"kode": "3UX29", "nama": "Pendidikan Pancasila MKWK", "sks": 2},
    {"kode": "3UX56", "nama": "Fisika Dasar", "sks": 3},
    {"kode": "3UX76", "nama": "Kimia Dasar", "sks": 3},
    {"kode": "3CX29", "nama": "Sistem Basis Data", "sks": 3},
]

# KRS
krs = []

# Menu Admin
def menu_admin():
    username = "Manisha"
    password = "7890"

    input_username = input("Username: ")
    input_password = input("Password: ")

    if input_username == username and input_password == password:
        print("Login berhasil.")
        while True:
            print("\n1. Tampilkan semua mata kuliah")
            print("2. Tambah Daftar Mata Kuliah")
            print("3. Update Mata Kuliah")
            print("4. Hapus Mata Kuliah")
            print("5. Keluar")

            pilih = input("Masukkan Pilihan: ")

            if pilih == "1":
                tampilkan_semua_matkul()
            elif pilih == "2":
                tambah_matkul()
            elif pilih == "3":
                update_matkul()
            elif pilih == "4":
                hapus_matkul()
            elif pilih == "5":
                print("Anda memerlukan login kembali.")
                break
            else: 
                print("Pilihan tidak valid, silakan coba lagi.")
    else:
        print("Username atau Password salah, coba lagi.")

# Fungsi untuk menampilkan semua Matkul oleh admin
def tampilkan_semua_matkul():
    tabel = PrettyTable()
    tabel.field_names = ["Kode", "Nama Mata Kuliah", "SKS"]
    for matkul in semua_mata_kuliah:
        tabel.add_row([matkul["kode"], matkul["nama"], matkul["sks"]])
    print("\nDaftar Semua Mata Kuliah:")
    print(tabel)

# Fungsi menambah matkul oleh admin
def tambah_matkul():
    kode_matkul = input("Masukkan kode mata kuliah: ")
    nama_matkul = input("Masukkan nama mata kuliah: ")
    sks = input("Masukkan jumlah SKS: ")

    semua_mata_kuliah.append({"kode": kode_matkul, "nama": nama_matkul, "sks": int(sks)})
    print(f"Mata kuliah {nama_matkul} berhasil ditambahkan.")

# Fungsi update matkul oleh admin
def update_matkul():
    kode_matkul = input("Masukkan kode mata kuliah yang ingin diperbarui: ")
    matkul = next((m for m in semua_mata_kuliah if m["kode"] == kode_matkul), None)

    if matkul:
        nama_baru = input(f"Masukkan nama baru untuk mata kuliah {matkul['nama']} (kosongkan jika tidak ingin mengubah): ")
        sks_baru = input(f"Masukkan SKS baru untuk mata kuliah {matkul['sks']} (kosongkan jika tidak ingin mengubah): ")

        if nama_baru:
            matkul['nama'] = nama_baru
        if sks_baru:
            matkul['sks'] = int(sks_baru)

        print("Mata kuliah berhasil diperbarui.")
    else:
        print("Mata kuliah tidak ditemukan.")

# Fungsi menghapus matkul
def hapus_matkul():
    kode_matkul = input("Masukkan kode mata kuliah yang ingin dihapus: ")
    global semua_mata_kuliah
    semua_mata_kuliah = [m for m in semua_mata_kuliah if m["kode"] != kode_matkul]
    print(f"Mata kuliah dengan kode {kode_matkul} berhasil dihapus.")

# Fungsi untuk login Mahasiswa
def login_Mahasiswa():
    mahasiswa = {
        "2409116058": {"Password": "890403", "CAPTCHA": "U7XJ"}
    }

    while True:
        username = input("Username: ")
        password = input("Password: ")

        if username in mahasiswa and mahasiswa[username]["Password"] == password:
            print("Login berhasil.")
            return username
        else:
            print("Username atau password salah. Silakan coba lagi.")

# Menu Mahasiswa
def menu_mahasiswa():
    while True:
        print("\nMenu Mahasiswa:")
        print("1. Tampilkan Daftar Mata Kuliah")
        print("2. Tambah Mata Kuliah ke KRS")
        print("3. Tampilkan KRS")
        print("4. Keluar")

        pilihan = input("Pilih menu (1-4): ")

        if pilihan == "1":
            tampilkan_semua_matkul()
        elif pilihan == "2":
            tambah_ke_krs()
        elif pilihan == "3":
            tampilkan_krs()
        elif pilihan == "4":
            print("Terima kasih telah menggunakan sistem.")
            break
        else:
            print("Pilihan tidak valid, coba lagi.")

# Fungsi tambah mata kuliah ke KRS
def tambah_ke_krs():
    kode = input("Masukkan kode mata kuliah yang ingin ditambahkan ke KRS: ")
    matkul = next((m for m in semua_mata_kuliah if m["kode"] == kode), None)
    if matkul:
        krs.append(matkul)
        print(f"{matkul['nama']} berhasil ditambahkan ke KRS.")
    else:
        print("Mata kuliah tidak ditemukan.")

# Fungsi tampilkan KRS
def tampilkan_krs():
    tabel = PrettyTable()
    tabel.field_names = ["Kode", "Nama Mata Kuliah", "SKS"]
    total_sks = 0
    for matkul in krs:
        tabel.add_row([matkul["kode"], matkul["nama"], matkul["sks"]])
        total_sks += matkul["sks"]
    print("\nKartu Rencana Studi:")
    print(tabel)
    print(f"Total SKS: {total_sks}")

# Fungsi utama
def main():
    while True:
        print("\n=== Selamat datang di website AIS Unmul ===")
        print("1. Admin")
        print("2. Mahasiswa")
        user = input("Pilih peran user: ")

        if user == "1":
            menu_admin()
        elif user == "2":
            login_Mahasiswa()
            menu_mahasiswa()
        else:
            print("Pilihan tidak valid. Coba lagi.")

if __name__ == "__main__":
    main()
