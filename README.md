# labpy6

Soal Praktikum 1
Buat program sederhana dengan mengaplikasikan penggunaan fungsi
yang akan menampilkan daftar nilai mahasiswa, dengan ketentuan:
1. Fungsi tambah() untuk menambah data
2. Fungsi tapilkan() untuk menampilkan data
3. Fungsi hapus(nama) untuk menghapus data berdasarkan nama
4. Fungsi ubah(nama) untuk mengubah data berdasarkan nama

KODE PYTHON:

    # Daftar untuk menyimpan data mahasiswa
    data_mahasiswa = []

    # Fungsi untuk menambah data mahasiswa
    def tambah():
    nama = input("Masukkan nama mahasiswa: ")
    nim = input("Masukkan NIM: ")
    nilai = float(input("Masukkan nilai: "))
    data_mahasiswa.append({"nama": nama, "nim": nim, "nilai": nilai})
    print("Data berhasil ditambahkan.")

    # Fungsi untuk menampilkan data mahasiswa
    def tampilkan():
      if not data_mahasiswa:
        print("Tidak ada data mahasiswa.")
    else:
        print("Daftar Data Mahasiswa:")
        for i, mahasiswa in enumerate(data_mahasiswa, start=1):
            print(f"{i}. Nama: {mahasiswa['nama']}, NIM: {mahasiswa['nim']}, Nilai: {mahasiswa['nilai']}")

    # Fungsi untuk menghapus data mahasiswa berdasarkan nama
    def hapus(nama):
    for mahasiswa in data_mahasiswa:
        if mahasiswa['nama'].lower() == nama.lower():
            data_mahasiswa.remove(mahasiswa)
            print(f"Data mahasiswa dengan nama {nama} berhasil dihapus.")
            return
    print(f"Data mahasiswa dengan nama {nama} tidak ditemukan.")

    # Fungsi untuk mengubah data mahasiswa berdasarkan nama
    def ubah(nama):
    for mahasiswa in data_mahasiswa:
        if mahasiswa['nama'].lower() == nama.lower():
            print(f"Data lama: Nama: {mahasiswa['nama']}, NIM: {mahasiswa['nim']}, Nilai: {mahasiswa['nilai']}")
            mahasiswa['nama'] = input("Masukkan nama baru: ")
            mahasiswa['nim'] = input("Masukkan NIM baru: ")
            mahasiswa['nilai'] = float(input("Masukkan nilai baru: "))
            print("Data berhasil diubah.")
            return
    print(f"Data mahasiswa dengan nama {nama} tidak ditemukan.")

    # Menu utama
    def menu():
    while True:
        print("\nMenu:")
        print("1. Tambah Data")
        print("2. Tampilkan Data")
        print("3. Hapus Data")
        print("4. Ubah Data")
        print("5. Keluar")
        pilihan = input("Pilih menu (1-5): ")

        if pilihan == "1":
            tambah()
        elif pilihan == "2":
            tampilkan()
        elif pilihan == "3":
            nama = input("Masukkan nama mahasiswa yang akan dihapus: ")
            hapus(nama)
        elif pilihan == "4":
            nama = input("Masukkan nama mahasiswa yang akan diubah: ")
            ubah(nama)
        elif pilihan == "5":
            print("Keluar dari program.")
            break
        else:
            print("Pilihan tidak valid. Silakan coba lagi.")

    # Menjalankan menu utama
    menu()

PENJELASAN:
Data Mahasiswa: Data mahasiswa disimpan dalam list data_mahasiswa, yang berisi dictionary dengan kunci 'nama', 'nim', dan 'nilai'.
1.  Fungsi tambah(): Meminta input nama, NIM, dan nilai mahasiswa, lalu menambahkannya ke dalam daftar.
2. Fungsi tampilkan(): Menampilkan semua data mahasiswa yang ada dalam daftar.
3. Fungsi hapus(nama): Menghapus data mahasiswa berdasarkan nama yang diberikan.
4. Fungsi ubah(nama): Mengubah data mahasiswa berdasarkan nama yang diberikan, termasuk nama, NIM, dan nilai.
5. Menu Utama: Menyediakan antarmuka pengguna untuk memilih operasi yang diinginkan.

INPUT

<img width="736" alt="Cuplikan layar 2024-11-28 225025" src="https://github.com/user-attachments/assets/17b6a93a-748b-4829-a0f4-6acd155ee215">
<img width="744" alt="Cuplikan layar 2024-11-28 224931" src="https://github.com/user-attachments/assets/4158a138-6e2f-48d9-83f5-1293b36a19d2">
<img width="472" alt="Cuplikan layar 2024-11-28 224945" src="https://github.com/user-attachments/assets/9719d113-1718-42f5-9ebf-47ed07e0d8d9">
<img width="736" alt="Cuplikan layar 2024-11-28 225025" src="https://github.com/user-attachments/assets/4e89f834-1653-40f6-a64f-38c8cdd1d77e">

OUTPUT:

<img width="334" alt="Cuplikan layar 2024-11-28 225238" src="https://github.com/user-attachments/assets/e3d973d4-60dd-4751-b147-d0f8df611e51">
<img width="348" alt="Cuplikan layar 2024-11-28 225253" src="https://github.com/user-attachments/assets/b01793f0-1ede-4e8d-85c9-c642b72e1d01">
<img width="344" alt="Cuplikan layar 2024-11-28 225311" src="https://github.com/user-attachments/assets/9100061a-dbcc-4660-95f8-23079a5a63fe">

FLOWCHART:

![FLOWCHART PRAKTIKUM 6](https://github.com/user-attachments/assets/e1b4bc44-d464-481b-a8dc-69742ba33072)

Latihan 1:

    import math

    # Menggunakan lambda untuk mendefinisikan fungsi
    a = lambda x: x**2
    b = lambda x, y: math.sqrt(x*2 + y*2)
    c = lambda *args: sum(args) / len(args)
    d = lambda s: "".join(set(s))

    if __name__ == "__main__":

    print("a(5):", a(5))

    print("b(3, 4):", b(3, 4))

    print("c(1, 2, 3, 4, 5):", c(1, 2, 3, 4, 5))

    print("d('hello world'):", d('hello world'))

INPUT:

<img width="385" alt="Cuplikan layar 2024-11-28 231000" src="https://github.com/user-attachments/assets/905f5eca-cdb1-4d1f-8885-80ce97e61254">

OUTPUT:

<img width="221" alt="Cuplikan layar 2024-11-28 231006" src="https://github.com/user-attachments/assets/68854776-de0c-493b-a2f1-838bf8a4f0f6">

