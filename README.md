# Jarkom-Modul-1-IT08-2024

| Nama          | NRP          |
| ------------- | ------------ |
| | 50272210 |
| Aisha Ayya Ratiandari | 5027231056 |

### 1. Advance Sanity Check
![image](https://github.com/user-attachments/assets/f9946ff3-7f82-435a-89ac-1a3bed12c644)
Pertama setelah membuka filenya ke Wireshark, saya menemukan jawaban username setelah mencari satu-satu.
![Screenshot (15)](https://github.com/user-attachments/assets/3cdcbcb9-adf6-45c0-8516-e0e0675c1925)
Lalu untuk bagian nama file dapat dicari dengan melihat satu-persatu lagi
Disana kita mendapatkan informasi bahwa petunjuk berikutnya ada di dalam peraturan praktikum bagian "Soal Shift"
![Screenshot (17)](https://github.com/user-attachments/assets/3074517a-56d1-4008-a727-7497a9f8a646)
Lalu kita mendapatkan "cGVud29yZA==" dimana kita akan men-decodenya dan menghasilkan kata "penword" sebagai jawaban untuk soal terakhir
![Screenshot (19)](https://github.com/user-attachments/assets/cc4de6dd-ad3c-45f7-9f66-d53510a097be)

### 4. FTP Login
![Screenshot (20)](https://github.com/user-attachments/assets/5044a37a-6667-42d5-b6c1-44932cb91bcf)
Pertama mencoba mencari user yang berhasil login, dari sana kita bisa mendapatkan informasi berupa username beserta passwordnya, dari sana kita berhasil mendapatkan flagnya
![Screenshot (19) (1)](https://github.com/user-attachments/assets/e6b54950-ddec-4730-ae19-ce7c41a21297)

### 5. Surprise
melanjutkan soal sebelumnya, disini kita diminta untuk mengetahui service yang digunakan oleh FTP server
![Screenshot (21)](https://github.com/user-attachments/assets/382ca43e-795d-4f25-8b32-305860853daf)
disana kita bisa mengetahui informasi tersebut telah disebut di paling awal
lalu untuk mengetahui nama file yang dikirim oleh attacker beradda di informasi paling bawah
![Screenshot (22)](https://github.com/user-attachments/assets/b532b773-39e5-40e5-9252-0e4661467679)
Selain itu, kita dimint auntuk mencari pesan yang ditinggalkan oleh attacker,
setelah saya mencari-cari, saya menemukan satu file yang cukup janggal dengan nama file yang sama denga yang dikirim oleh attacker
![Screenshot (23)](https://github.com/user-attachments/assets/34081683-d9f6-4dfc-9588-dd02e426a547)
Setelah didecode, hasilnya adalah berbentuk leetspeet yanga dalah pesan dari attackernya
![Screenshot (24)](https://github.com/user-attachments/assets/ebab4cd2-eb4c-4467-bdce-eb6b90ae383f)

### 10. Gajah Terbang (Server Recon)
untuk soal ini, pertama saya mencari satu-satu hingga menemukan satu paket yang berisi informasi berupa nama, email, dan password, disana dapat ditemukan informasi berupa dbms yang digunakan di server tersebut, nama database, email, dan password dari admin
![Screenshot (28)](https://github.com/user-attachments/assets/1e8bc44b-78a5-4326-a2c2-a7895
![Screenshot (29)](https://github.com/user-attachments/assets/4939a533-2ae5-4a3e-aaf4-49a2799bc575)
802d1bf)
untuk port yang digunakan, bisa didapat dari package (174) tersebut juga
![Screenshot (27)](https://github.com/user-attachments/assets/750287bb-c217-4458-a8a3-557b60b9e451)
untuk password sendiri, diperlukan hashing dan hasilnya adalah sebagai berikut
![image](https://github.com/user-attachments/assets/1db2165d-c75f-43e9-9bf9-6693206b1056)

### 11. Gajah Terbang (Attacker Recon)
melanjutkan soal sebelumnya, menggunakan package yang sama, kita bisa mendapatkan informasi berupa
![Screenshot (26)](https://github.com/user-attachments/assets/31fd5099-46d8-47f5-b6ac-2023e807ff5a)
untuk bagian attacker, disini saya mencoba-coba saja, dan setelah mengamati dari informasi tersebut saya mendapatkan hasilnya
![image](https://github.com/user-attachments/assets/694caa7e-a4c2-466f-8117-c8b1a64baf63)
untuk password dari attacker saya dapatkan dari hashing password tersebut, dan ini hasilnya
![Screenshot 2024-09-19 003635](https://github.com/user-attachments/assets/eb82051d-64a6-4358-8cce-ddce1be59543)





