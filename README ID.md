![2025-05-18_01-49](https://raw.githubusercontent.com/Jcllynnaf/HeRecon/refs/heads/main/assets/HeRecon.jpg)



# HeRecon adalah alat OSINT (Open-Source Intelligence) yang dirancang untuk pengintaian domain dan analisis keamanan.

# Apa fungsinya?
Pencacahan subdomain melalui crt.sh
HeRecon memanfaatkan layanan CRT.sh yang tersedia untuk umum untuk mencari data sertifikat SSL/TLS, mengekstraksi nama domain dan subdomain yang terkait dengan domain target.Ini membantu Anda mengidentifikasi subdomain tambahan yang mungkin terpapar secara publik.

# Penemuan subdomain brute-force
Alat ini menggunakan wordlist (disediakan dalam file yang disebut subdomain.txt) dan melakukan pemeriksaan brute-force untuk menemukan subdomain tambahan.Ia mencoba untuk menyelesaikan setiap awalan (mis., "WWW," "Mail," "API") dikombinasikan dengan domain target menggunakan kueri DNS.Setiap nama host yang berhasil diselesaikan dianggap sebagai subdomain yang valid.

# Integrasi Shodan
Dengan memasukkan API Shodan, HeRecon dapat mengambil informasi lebih lanjut tentang alamat IP yang diperoleh dari proses brute-force.Shodan adalah mesin pencari yang mengindeks perangkat yang terhubung ke Internet.Dengan integrasi ini, alat ini menampilkan detail seperti sistem operasi, port terbuka, dan informasi organisasi yang ditautkan ke setiap IP yang ditemukan.

# Penyimpanan Hasil
Pengguna dapat menyimpan hasilnya-subdomain yang ditemukan melalui CRT.SH, subdomain brute-force, dan data Shodan-ke file dalam format TXT dan JSON.Ini memudahkan analis atau profesional keamanan untuk meninjau data yang dikumpulkan nanti atau mengintegrasikannya ke dalam proses otomatis lebih lanjut.

Antarmuka Interaktif Berbasis # Kutukan
HeRecon menampilkan antarmuka pengguna berbasis teks interaktif yang dibangun dengan modul Kutukan Python.Antarmuka dirancang dengan skema warna bertema merah dan branding seni ASCII untuk menciptakan pengalaman baris perintah yang menarik secara visual.Ini menyediakan sistem navigasi berbasis menu yang memungkinkan pengguna untuk memilih dari berbagai fungsi (mis., Tetapkan domain target, inisiasi pemindaian subdomain, lihat hasil, dan simpan laporan).

# Singkatnya
HeRecon adalah alat OSINT multi-fungsional yang mengotomatiskan proses mengumpulkan intelijen pada domain dengan:

Menghitung subdomain menggunakan data sertifikat publik.

Menemukan subdomain tambahan melalui metode brute-force.

Meningkatkan pengintaian dengan memasukkan informasi IP terperinci melalui Shodan.

Menawarkan antarmuka interaktif berbasis terminal untuk memandu pengguna melalui setiap langkah.

Memungkinkan ekspor laporan untuk analisis lebih lanjut.

Alat ini sangat berguna untuk penguji penetrasi, peneliti keamanan, dan administrator jaringan yang perlu melakukan pengintaian komprehensif pada domain target menggunakan data sumber terbuka.

# HeRecon

HeRecon adalah alat OSINT untuk pengintaian domain.Ini dapat menyebutkan subdomain melalui crt.sh, melakukan penemuan subdomain brute-force (menggunakan wordlist), dan mengambil informasi IP dari Shodan.Alat ini menggunakan antarmuka berbasis kutukan untuk memberikan pengalaman baris perintah interaktif.

## Fitur

- ** Enumerasi subdomain: ** Temukan subdomain menggunakan crt.sh.
- ** subdomain brute-force: ** Temukan subdomain dengan mencoba awalan wordlist.
- ** Integrasi Shodan: ** Cari informasi IP dengan API Shodan.
- ** Pembuatan Laporan: ** Simpan Hasil ke File TXT dan JSON.
- ** UI interaktif: ** Antarmuka menu berbasis kutukan, penuh warna, dan paginated.
## Persyaratan

- Python 3.6 atau lebih tinggi.
- [permintaan] (https://pypi.org/project/requests/)
- ** Untuk UNIX/Linux/MacOS: ** Modul `CURSES` disertakan secara default.
-** Untuk pengguna Windows: ** instal [`windows-curses`] (https://pypi.org/project/windows-curses/) untuk mendukung modul kutukan.

Instalasi ##

1. ** Kloning repositori: **

`` `Bash
git clone https://github.com/Jcllynnaf/HeRecon.git
cd HeRecon
`` `

2. ** Instal dependensi: **

    ```bash
    pip install -r requirements.txt
    ```

3. ** Siapkan daftar kata Anda: **

Pastikan Anda memiliki file bernama `subdomain.txt` di root repositori yang berisi awalan subdomain Anda (satu per baris).


4. ** Jalankan alat: **

    ```bash
    python3 HeRecon.py
    ```

## Penggunaan

Saat Anda menjalankan alat, Anda akan melihat menu interaktif di mana Anda bisa:

- Atur atau ubah domain target.
- Cari subdomain melalui crt.sh.
- Lakukan penemuan subdomain brute-force.
- Pindai IP yang ditemukan menggunakan Shodan.
- Simpan hasil yang dikumpulkan ke dalam file TXT dan JSON.

Ikuti petunjuk di layar untuk berinteraksi dengan alat ini.

Lisensi ##

*Sertakan informasi lisensi Anda di sini.*

## Kontak

Untuk dukungan atau pertanyaan, silakan kunjungi:
- **Contact:** [https://instagram.com/bytelonecode](https://instagram.com/bytelonecode)
