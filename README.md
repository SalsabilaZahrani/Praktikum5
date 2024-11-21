# Praktikum5
# LATIHAN 1

• Buat Dictionary daftar kontak
• Nama sebagai key, dan nomor sebagai value
• Tampilkan kontaknya Salsa
• Tambah kontak baru dengan nama Dica, nomor 081281751238
• Ubah kontak Caca dengan nomor baru 089615271097
• Tampilkan semua Nama
• Tampilkan semua Nomor
• Tampilkan daftar Nama dan nomornya
• Hapus kontak Caca.

    # 1. Buat Dictionary daftar kontak
    daftar_kontak = {
    "Salsa": "085673198712",
    "Dica": "081281751238",
    "Caca": "089615271097"
    }

    # 2. Tampilkan kontaknya Salsa
    print("Kontak Salsa:", daftar_kontak.get("Salsa"))

    # 3. Tambah kontak baru dengan nama Dica, nomor 081281751238
    daftar_kontak["Dica"] = "081281751238"
    print("Kontak Dica telah ditambahkan.")

    # 4. Ubah kontak Caca dengan nomor baru 089615271097
    daftar_kontak["Caca"] = "089615271097"
    print("Kontak Caca telah diubah.")

    # 5. Tampilkan semua Nama
    print("Semua Nama:", list(daftar_kontak.keys()))

    # 6. Tampilkan semua Nomor
    print("Semua Nomor:", list(daftar_kontak.values()))

    # 7. Tampilkan daftar Nama dan nomornya
    print("Daftar Nama dan Nomornya:")
    for nama, nomor in daftar_kontak.items():
    print(f"{nama}: {nomor}")

    # 8. Hapus kontak Caca
    if "Caca" in daftar_kontak:
    del daftar_kontak["Caca"]
    print("Kontak Caca telah dihapus.")
    else:
    print("Kontak Caca tidak ditemukan.")
![Cuplikan layar 2024-11-21 103949](https://github.com/user-attachments/assets/c15306d4-c92f-4ce8-9dfa-2bf0c6b43386)

PENJELASAN:
1. Membuat Dictionary Daftar Kontak
 Di sini, sebuah dictionary bernama daftar_kontak dibuat. Kunci (key) dari dictionary ini adalah nama-nama kontak (Salsa, Dica, Caca), dan nilainya (value) adalah nomor telepon yang       sesuai. 
2. Menampilkan Kontak Salsa
Menggunakan metode get(), kode ini menampilkan nomor telepon yang terdaftar untuk kontak "Salsa". Jika "Salsa" tidak ada dalam dictionary, get() akan mengembalikan None tanpa             menghasilkan error. 
3. Menambahkan Kontak Baru
Di sini, kontak baru dengan nama "Dica" dan nomor "081281751238" ditambahkan ke dalam dictionary. Jika nama tersebut sudah ada, nilainya akan diperbarui. Secara keseluruhan, kode ini    menunjukkan bagaimana cara membuat, mengubah, menampilkan, dan menghapus data dalam sebuah dictionary yang digunakan untuk menyimpan daftar kontak.
4. Mengubah Kontak Caca
Kontak "Caca" diubah dengan nomor baru "089615271097". Jika "Caca" tidak ada, maka kontak baru akan ditambahkan.
5. Menampilkan Semua Nama
digunakan untuk mendapatkan semua kunci (nama) dari dictionary, yang kemudian diubah menjadi list untuk ditampilkan
6. Menampilkan Semua Nomor
digunakan untuk mendapatkan semua nilai (nomor telepon) dari dictionary, yang juga diubah menjadi list untuk ditampilkan.
7. Menampilkan Daftar Nama dan Nomornya
digunakan untuk mendapatkan pasangan kunci-nilai dari dictionary. Dalam loop, setiap nama dan nomor ditampilkan dalam format yang rapi.
8. Menghapus Kontak Caca

# PRAKTIKUM 5

    # Pastikan dictionary mahasiswa sudah didefinisikan
    mahasiswa = {}

    def tambah_data():
    print("\n=== TAMBAH DATA MAHASISWA ===")
    nama = input("Masukkan Nama: ")
    
    if nama in mahasiswa:  # Cek apakah nama sudah ada
        print("Data mahasiswa sudah ada!")
        return
    
    try:
        # Input nilai
        tugas = float(input("Nilai Tugas (0-100): "))
        uts = float(input("Nilai UTS (0-100): "))
        uas = float(input("Nilai UAS (0-100): "))
        
        # Validasi rentang nilai
        if not (0 <= tugas <= 100 and 0 <= uts <= 100 and 0 <= uas <= 100):
            print("Nilai harus berada dalam rentang 0-100!")
            return
        
        # Hitung nilai akhir
        nilai_akhir = (tugas * 0.3) + (uts * 0.35) + (uas * 0.35)
        
        # Simpan ke dictionary
        mahasiswa[nama] = {
            "tugas": tugas,
            "uts": uts,
            "uas": uas,
            "nilai_akhir": nilai_akhir
        }
        print("Data berhasil ditambahkan!")
    
    except ValueError:
        print("Input tidak valid! Pastikan untuk memasukkan angka.")

    # Contoh pemanggilan fungsi
    tambah_data()
![Cuplikan layar 2024-11-21 111644](https://github.com/user-attachments/assets/922110e7-0633-4310-a962-56af6858837d)

PENJELASAN:
1. Fungsi lihat_data():
        Menampilkan daftar nilai mahasiswa dalam format tabel.
        Jika tidak ada data, menampilkan pesan bahwa tidak ada data.
        Menghitung nilai akhir berdasarkan bobot: 30% untuk tugas, 35% untuk UTS, dan 35% untuk UAS.
        Menggunakan enumerate untuk menampilkan nomor urut mahasiswa.
2. Fungsi tambah_data():
        Meminta input dari pengguna untuk menambahkan data mahasiswa baru.
        Data yang dimasukkan (NIM, nama, nilai tugas, UTS, dan UAS) disimpan dalam dictionary dan ditambahkan ke list data_mahasiswa.
        Menampilkan pesan konfirmasi bahwa data berhasil ditambahkan.
3. Fungsi ubah_data():
        Menampilkan data yang ada dengan memanggil lihat_data().
        Meminta pengguna untuk memasukkan nomor data yang ingin diubah.
        Jika nomor valid, pengguna diminta untuk memasukkan data baru, yang kemudian menggantikan data lama di list.
        Menampilkan pesan konfirmasi bahwa data berhasil diubah.
4. Fungsi hapus_data():
        Menampilkan data yang ada dengan memanggil lihat_data().
        Meminta pengguna untuk memasukkan nomor data yang ingin dihapus.
        Jika nomor valid, data dihapus dari list menggunakan pop().
        Menampilkan pesan konfirmasi bahwa data berhasil dihapus.
5. Fungsi cari_data():
        Meminta pengguna untuk memasukkan NIM yang ingin dicari.
        Mencari data mahasiswa berdasarkan NIM dan menampilkan hasilnya dalam format tabel.
        Jika tidak ditemukan, menampilkan pesan bahwa data tidak ditemukan.

![flowchart](https://github.com/user-attachments/assets/3f6e9078-9b5d-400e-abba-44211690ee4e)
