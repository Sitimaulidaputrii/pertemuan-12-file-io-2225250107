# Pertemuan 12 - File I/O dan Error Handling

Nama: Siti Maulida Putri Irawan
NIM: 2225250107
Kelas: 3A

## Tujuan

Memahami penggunaan file untuk membaca dan menyimpan data nilai mahasiswa, mengolah data yang valid untuk menghasilkan rekap nilai, serta menangani kesalahan yang terjadi saat pemrosesan file.

## Format File Input

Data nilai mahasiswa disimpan dalam file data/nilai.txt dengan format NIM,nilai.
A001,85
A002,78
A003,92
A004,abc
A005,74
A006,88

## Cara Menjalankan

Melalui terminal VS Code dari folder utama tugas dengan perintah:

```bash
python tugas/rekap_nilai_file.py
```

Program membaca data dari data/nilai.txt dan menyimpan hasil rekap ke data/hasil_rekap.txt.

## Error yang Ditangani

FileNotFoundError: Menangani kondisi ketika file input tidak ditemukan dengan menampilkan pesan.
ValueError: Menangani nilai yang tidak dapat dikonversi menjadi angka dengan melewati baris yang tidak valid.

## Test Case

| Kondisi | Hasil yang Diharapkan | Hasil Aktual | Status |
| --- | --- | --- | --- |
| File berisi 6 data mahasiswa, dengan 5 nilai valid dan 1 nilai tidak valid (abc) | Data tidak valid dilewati dan 5 data valid diproses | Baris 4 dilewati: A004,abc. Jumlah data valid: 5 | Berhasil |
| Data nilai valid: 85, 78, 92, 74, 88 | Rata-rata: 83.40, minimum: 74.00, maksimum: 92.00, dan jumlah lulus: 5 | Berhasil |
| File data/nilai.txt tidak ditemukan | Program menampilkan pesan bahwa file tidak ditemukan tanpa mengalami crash | File tidak ditemukan: data/nilai.txt | Berhasil |

## Refleksi

Kesalahan yang ditemukan adalah nilai abc pada file input yang tidak dapat diubah menjadi angka. Program menangani kesalahan tersebut menggunakan ValueError, sehingga baris yang tidak valid dilewati dan data lainnya tetap dapat diproses.