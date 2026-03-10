[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/J9HR2HBe)
[![Open in Codespaces](https://classroom.github.com/assets/launch-codespace-2972f46106e565e64193e422d61a12cf1da4916b45550586e14ef0a7c637dd04.svg)](https://classroom.github.com/open-in-codespaces?assignment_repo_id=22982702)
<div align="center">

## LAPORAN [NAMA MATAKULIAH]

![Logo PNL](/img/logo-pnl.png)

### Disusun Oleh:  
Nama               : [Nasywa Humairah]  
NIM                : [2024903430028]  
Kelas              : [TRKJ 2A]


### Program Studi Teknologi Rekayasa Komputer Jaringan
### Jurusan Teknologi Informasi dan Komputer
### Politeknik Negeri Lhokseumawe
### 2025


---


## Lembar Pengesahan


| No. Praktikum     | : | [6] |
|------------------:|:-:|:--------------|
| Judul Praktikum   | : | [Cloud Computing] |
| Tanggal Praktikum | : | [5 maret 2026] |
| Tanggal Penyerahan| : | [10 maret 2026] |
| Nama Praktikan    | : | [Nasywa Humairah] |
| NIM/Kelas Praktikan| : | [2024903430028] / [TRKJ 2A] |
| Nilai Praktikum   | : | .......................... |
| Dosen Pengampu    | : | Muhammad Davi, S.Kom., M.Cs. |

Mengetahui,  
Dosen Pengampu
<br><br><br><br><br>

Muhammad Davi, S.Kom., M.Cs.
</div>


## Daftar Isi
- [Lembar Pengesahan](#lembar-pengesahan)
- [Daftar Isi](#daftar-isi)
- [Tujuan Praktikum](#tujuan-praktikum)
- [Dasar Teori](#dasar-teori)
- [Alat dan Bahan](#alat-dan-bahan)
- [Langkah Kerja](#langkah-kerja)
- [Hasil dan Pembahasan](#hasil-dan-pembahasan)
- [Kesimpulan](#kesimpulan)
- [Referensi](#referensi)
---

## A. Tujuan Praktikum
Membangun kontainer Docker: Pesan praktikum difokuskan agar mahasiswa dapat membangun kontainer Docker menggunakan alat pengembangan baris perintah (command line).

Menggunakan alat pengembangan: Melatih penggunaan command line development tools dalam ekosistem Docker.

Menguasai perintah dasar Docker: Melalui berbagai lab (1.1 hingga 1.5), mahasiswa diharapkan memahami siklus hidup kontainer, mulai dari instalasi, menjalankan perintah, hingga manajemen image dan Docker Hub.

## B. Dasar Teori
1. Pengenalan Docker
Docker adalah sebuah proyek sumber terbuka (open source) yang menyediakan platform terbuka bagi pengembang dan administrator sistem untuk membangun, mengemas, dan menjalankan aplikasi di mana saja sebagai kontainer ringan. Docker mengotomatiskan penyebaran aplikasi di dalam kontainer perangkat lunak.

2. Teknologi Kontainer
Isolasi: Kontainer memungkinkan aplikasi dikemas dengan semua bagian yang dibutuhkannya, seperti pustaka (libraries) dan dependensi lainnya, lalu mengirimkannya sebagai satu paket.

Efisiensi: Berbeda dengan mesin virtual (Virtual Machine), kontainer tidak menyertakan sistem operasi lengkap, sehingga lebih efisien dan cepat untuk dijalankan.

Portabilitas: Dengan menggunakan kontainer, pengembang dapat menjamin bahwa aplikasi akan berjalan di mesin lain terlepas dari pengaturan lokal mesin tersebut yang mungkin berbeda dari mesin yang digunakan untuk menulis kode.

3. Komponen Utama dalam Praktikum
Docker Engine: Teknologi dasar yang menjalankan dan mengelola kontainer.

Images: Paket statis yang berisi kode, runtime, pustaka, dan pengaturan yang diperlukan untuk menjalankan aplikasi (contoh: image Alpine).

Containers: Instansiasi dari sebuah image yang sedang berjalan.

Docker Hub: Layanan registry berbasis cloud yang digunakan untuk berbagi dan menyimpan image kontainer.

## C. Alat dan Bahan
1. Laptop
2. Sistem Operasi
3. Docker Desktop
4. Terminal atau Command Line


## D. Langkah Kerja
Lab 1.1 & 1.2: Instalasi dan Persiapan
Instalasi: Mengunduh dan menginstal Docker Desktop pada sistem operasi yang digunakan.

Verifikasi: Membuka terminal (PowerShell/Command Prompt) dan mengetikkan perintah docker version untuk memastikan Docker sudah terpasang dengan benar.

Lab 1.3: Menjalankan Container Pertama (Interactive)
Menarik Image: Menjalankan perintah docker pull alpine untuk mengunduh image Alpine Linux dari Docker Hub.

Melihat Image: Menjalankan perintah docker images untuk memastikan image sudah ada di penyimpanan lokal.

Menjalankan Mode Interaktif: Menjalankan perintah docker run -it alpine untuk masuk ke dalam terminal container.

Eksplorasi: Mencoba perintah Linux dasar seperti ls atau cat /etc/os-release di dalam container.

Keluar: Mengetik exit untuk keluar dari container.

Lab 1.4: Manajemen Image dan Container
Perintah Sekali Jalan: Menjalankan perintah docker run alpine ls -l untuk mengeksekusi perintah tanpa masuk ke mode interaktif.

Pemeriksaan Status: Menggunakan docker ps untuk melihat container yang aktif dan docker ps -a untuk melihat riwayat container yang sudah berhenti (Exited).

Pembersihan: Menghapus container yang sudah tidak terpakai menggunakan perintah docker rm <container_id>.

Menghapus Image: Menggunakan perintah docker rmi alpine untuk menghapus image dari sistem lokal.

Lab 1.5: Docker Hub
Registrasi: Membuat akun gratis di situs resmi Docker Hub.

Login: Menjalankan perintah docker login pada terminal dan memasukkan username serta password yang telah dibuat.

Berbagi Image: Menggunakan perintah docker push (jika ingin mengunggah image kustom ke repositori online).

## E. Hasil dan Pembahasan
[](/img/picture1.png)
Sebelum menjalankan Docker, sistem memerlukan pembaruan pada komponen kernel Windows Subsystem for Linux (WSL) agar Docker Engine dapat berkomunikasi dengan kernel Linux di Windows.
[](/img/picture2.png)
Setelah dilakukan update dan restart, Docker Desktop berhasil masuk ke status aktif.
Tampilan ini menunjukkan bahwa Docker Engine telah berhasil dijalankan setelah dilakukan pembaruan WSL dan restart sistem. Indikator hijau bertuliskan "Engine running" di pojok kiri bawah menandakan Docker siap digunakan. Terlihat juga penggunaan sumber daya (resource usage) seperti RAM sebesar 1.29 GB, yang menunjukkan bahwa kontainer sedang dalam posisi standby untuk menerima perintah.
[](/img/picture3.png)
[](/img/picture4.png)
[](/img/picture5.png)
[](/img/picture6.png)
[](/img/picture7.png)
[](/img/picture8.png)
[](/img/picture9.png)
[](/img/picture10.png)
[](/img/picture11.png)
[](/img/picture12.png)
[](/img/picture13.png)
Akses Terminal: Terlihat perubahan pada command prompt menjadi / #, yang menandakan bahwa pengguna kini berada di dalam shell Linux Alpine, bukan lagi di terminal Windows.

Efisiensi: Keberhasilan ini membuktikan bahwa Docker dapat menjalankan sistem operasi yang sangat ringan hanya dalam hitungan detik.

Verifikasi Perintah: Di dalam mode ini, perintah-perintah Linux seperti ls (untuk melihat daftar folder) dapat dijalankan dan memberikan hasil secara langsung dari dalam container.
[](/img/picture14.png)
Pada gambar ini, perintah yang benar yaitu docker run -it alpine telah dijalankan. Terlihat perubahan pada prompt terminal menjadi / #, yang menandakan pengguna telah berhasil masuk ke dalam sistem operasi Alpine Linux di dalam kontainer. Ini membuktikan bahwa Docker mampu menjalankan lingkungan sistem operasi yang terisolasi secara instan.
[](/img/picture15.png)
[](/img/picture16.png)
[](/img/picture17.png)
[](/img/picture18.png)
ambar ini menampilkan daftar riwayat kontainer yang pernah dijalankan. Status "Exited" menunjukkan bahwa kontainer tersebut sudah berhenti beroperasi setelah tugasnya (seperti perintah ls atau echo) selesai dilakukan. Melalui perintah ini, kita dapat memantau kontainer mana saja yang masih tersimpan di memori dan perlu dibersihkan agar tidak memenuhi ruang penyimpanan.

## F. Kesimpulan
Pemahaman Dasar Docker: Praktikum ini berhasil memberikan pemahaman mendasar mengenai penggunaan Docker sebagai platform untuk membangun, mengemas, dan menjalankan aplikasi dalam lingkungan yang terisolasi.

Efisiensi Sumber Daya: Penggunaan image Alpine Linux membuktikan bahwa kontainer jauh lebih ringan dan efisien dibandingkan Virtual Machine karena hanya menyertakan dependensi yang diperlukan tanpa sistem operasi utuh.

Manajemen Siklus Hidup: Mahasiswa mampu menguasai siklus hidup kontainer, mulai dari mengambil image dari registry (pull), menjalankan kontainer secara interaktif maupun sekali jalan (run), hingga membersihkan sisa kontainer dan image yang tidak terpakai (rm dan rmi).

Portabilitas dan Konektivitas: Melalui integrasi dengan Docker Hub, praktikum ini menunjukkan betapa mudahnya mendistribusikan aplikasi secara konsisten, yang merupakan pilar utama dalam teknologi Cloud Computing.
## G. Referensi
1] Docker Lab, "Lab 1.1 - Lab 1.5 Guide," [Online]. Available:.

[2] Docker, "Docker Documentation," Docker Hub, [Online]. Available: https://docs.docker.com.

[3] Docker Hub Registry, "Official Alpine Image," [Online]. Available: https://hub.docker.com/_/alpine.

