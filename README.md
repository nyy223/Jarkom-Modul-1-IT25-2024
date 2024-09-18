# Jarkom-Modul-1-IT25-2024

# Anggota Kelompok
Fikri Aulia As Sa'adi / 5027231026

Nayla Raissa Azzahra / 5027231054


## Advance Sanity Check
Langkah pengerjaan
1. Menggunakan filter http dan mencari di masing-masing package. Package di line 64 mengandung username JaneD03.
2. Pertanyaan selanjutnya adalah apa nama filename yg dikirm. Lanjut saya scroll package dan menemukan informasi mengenai filename dan clue untuk menjawab pertanyaan selanjutnya
3. Petunjuk selanjutnya adalah cGVud29yZA, dimana jika di decode menjadi "penword"
<img width="1440" alt="Screenshot 2024-09-18 at 23 33 11" src="https://github.com/user-attachments/assets/8d3ff10b-cac5-438a-90d0-2180f3709d7d">

## Pegawai Negeri Sebelah
Langkah pengerjaan
1. Menggunakan filter FTP dan membuka package yang menyimpan data pns dan mencari nama orang yang memiliki password nNnM%coQuF sesuai dengan soal
2. Selanjutnya menjawab pertanyaan sesuai dengan isi dari package yang sama.
![WhatsApp Image 2024-09-18 at 19 54 49](https://github.com/user-attachments/assets/908d48dc-ef29-4c06-bcbf-921f980809d6)
<img width="820" alt="Screenshot 2024-09-18 at 23 39 58" src="https://github.com/user-attachments/assets/4e04b487-adf7-4b55-8ace-2914e9dbc03f">

## FTP Login
Langkah pengerjaan 
1. Menggunakan filter FTP dan mencari package yang mengandung kalimat "Login successfull"
2. Follow stream package tersebut
3. Terdapat informasi terkait username dan password yang benar yang dapat digunakan untuk menjawab soal dan mendapatkan flag
<img width="1440" alt="Screenshot 2024-09-18 at 23 43 24" src="https://github.com/user-attachments/assets/8954e01d-52b1-412f-b05e-0b9c34dcf276">
![WhatsApp Image 2024-09-18 at 20 20 22](https://github.com/user-attachments/assets/eeae2dbb-1186-4fd7-8daa-8f0fdea6b9b5)

## Surprise
Langkah pengerjaan
1. Menggunakan filter FTP dan follow stream package yang sama dengan soal FTP Login. Dalam package tersebut, terdapat informasi mengenai service yang digunakan oleh FTP Server.
2. Dalam beberapa package tersebut juga ada informasi mengenai nama file yang dikirim oleh attacker, yaitu g0tcha.cpp. File ini juga bsia dicari dengan menggunakan filter frame contains "STOR"
3. Mencari package dengan protocol FTP-Data dan follow stream, maka akan keluar kode seperti berikut
![WhatsApp Image 2024-09-18 at 20 52 42](https://github.com/user-attachments/assets/57a1d3d7-d93d-49bd-b8b8-14bb5a3fac80)
4. Hasil dari kode tersebut adalah g0tchu n0w l1ttl3 m0us3, yang dapat digunakan untuk menjawab pertanyaan untuk mendapatkan flag

## Packets Barrage
Langkah pengerjaan
1. Menggunakan file yang sama dengan soal Illegal Breakthrough, kami diminta untuk mencari IP address dari attacker.
2. Saya notice bahwa IP yang paling sering muncul adalah 172.21.80.1 dan 172.21.88.207. Ketika saya masukkan 172.21.80.1 sebagai IP attacker, jawabannya benar.
3. Pertanyaan selanjutnya adalah Berapa total attempt dari bruteforce attacker? Karena tidak mungkin saya hitung satu-satu, maka saya coba follow stream salah satu package dan menemukan jawabannya adala 1917.
![WhatsApp Image 2024-09-18 at 22 25 16](https://github.com/user-attachments/assets/a85e2069-14a6-4735-b972-ac8889d5d5e7)

