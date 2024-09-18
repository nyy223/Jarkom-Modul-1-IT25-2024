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

## Ez
Langkah pengerjaan
1. Menggunakan filter tcp lalu follow tcp stream
2. Jawaban dari log langsung langsung ada
3. Port yang digunakan untuk service tersebut bisa dilihat di dest. port
![Screenshot 2024-09-18 192927](https://github.com/user-attachments/assets/8af3c409-d401-4151-99f8-ce799e8a1eb0)
![Screenshot 2024-09-18 192843](https://github.com/user-attachments/assets/78ac9a5a-dd07-41f5-93fa-53f3993a235c)

## FTP Login
Langkah pengerjaan
1. Soal pertama mencari IP Address dari korban. Jawabannya bisa dilihat langsung di wireshark IP yang sering muncul, yaitu 172.21.88.207
2. Selanjutnya mencari port yang digunakan untuk web server, saya menggunakan filter "http" lalu mengecek informasi dari package.
3. Kemudian, diminta untuk endpoint mana yang terdapat login. Saya menggunakan filter POST kemudian follow http stream dan informasi mengenai endpoint begitu juga tools yang digunakan.
4. Terakhir, untuk mencari username dan password yang digunakan untuk login, saya mencari hasil terakhir dari filter "http" sebelum akhirnya berhasil login.
![Screenshot 2024-09-18 202230](https://github.com/user-attachments/assets/9cecb478-e514-4239-a70a-6d49cd815e0a)
![Screenshot 2024-09-18 202509](https://github.com/user-attachments/assets/66dd6d1b-d65c-4585-bd26-7d4001d87123)

## Corporate Breach
Langkah Pengerjaan
1. Mencari nama penyerang, saya menggunakan filter "http" lalu menemukan salah satu package yang berisi pesan yang terdapat nama penyerang.
2. Selanjutnya mencari email dan password yang digunakan penyerang, saya menggunakan filter "http.response.code == 200" sebagai tanda bahwa login berhasil, dan ditemukan email dan password setelah di follow stream di salah satu package.
![Screenshot 2024-09-18 213208](https://github.com/user-attachments/assets/44f97a80-124c-4b12-bc1f-16532092853f)
![Screenshot 2024-09-18 213237](https://github.com/user-attachments/assets/5f3efef7-4b95-47f5-95e5-3234a5366fa5)

## Malicious Code
Langkah Pengerjaan
1. Mencari berapa kali penyerang melakukan dir listing, saya menggunakan filter "http.request.method == GET" untuk mengecek berapa kali penyerang mencoba melakukan dir listing, dan disana di dapat ada 52 package.
2. Untuk mencari endpoint yang berhasil didapatkan, saya menggunakan filter "http.request.method == POST" menandakan bahwa penyerang berhasil login, lalu saya follow stream dan didaptkan endpoint yang digunakan penyerang.
3. Mencari jumlah attempt dari penyerang, bisa menggunakan filter yang sama dengan sebelumnya lalu di cek ada berapa kali percobaan login dilakukan.
4. Terakhir, untuk memecahkan soal dari penyerang, saya sempat bingung dengan susunan angkanya, tapi akhirnya saya mencoba untuk memisahkan angkanya menjadi range antara 32-126 karena merupakan kode ASCII untuk karakter yang sering digunakan, akhirnya saya berhasil melihat pertanyaan dari penyerang. Untuk menjawabnya saya hanya mencoba-coba hingga benar.
![Screenshot 2024-09-18 213936](https://github.com/user-attachments/assets/51de02fa-18e3-4a03-88f6-2ca66d4ea4aa)
![Screenshot 2024-09-18 214710](https://github.com/user-attachments/assets/b3625770-6854-4d65-bddf-d95aa4b5dc57)
![Screenshot 2024-09-18 215610](https://github.com/user-attachments/assets/bad1275d-8950-4d02-9285-5526844e4105)
![Screenshot 2024-09-18 232114](https://github.com/user-attachments/assets/14459d80-4465-4959-b283-72f7fd671e01)
![Screenshot 2024-09-18 232226](https://github.com/user-attachments/assets/e532fdc5-79dc-43f9-b953-9223046024c9)

## Rizzset
Langkah Pengerjaan
1. Mengecek domain pada DNS Query bisa langsung terlihat di wireshark, yaitu www.its.ac.id
2. Untuk mengecek IP dari www.its.ac.id, saya melakukan ping.
3. Terakhir, untuk melihat JARM Fingerprint saya menggunakan tools JARM dengan command "python jarm.py its.ac.id -p 443 -o result.txt" yang kemudian hasilnya dapat dilihat di file result.txt.csv
![Screenshot 2024-09-18 222827](https://github.com/user-attachments/assets/2dd65cd5-5eae-42a1-9bcf-454befe96c57)
![Screenshot 2024-09-18 223437](https://github.com/user-attachments/assets/340ec42a-d51d-46f2-940c-18a1ef30a1ee)
![Screenshot 2024-09-18 223717](https://github.com/user-attachments/assets/9906f5d6-914c-44df-bbc8-30b42e037126)

















