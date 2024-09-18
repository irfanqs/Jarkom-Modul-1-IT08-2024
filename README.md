# Jarkom-Modul-1-IT08-2024

| Nama          | NRP          |
| ------------- | ------------ |
| Irfan Qobus Salim | 5027221058 |
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

### 2. FTP Login
![Screenshot (20)](https://github.com/user-attachments/assets/5044a37a-6667-42d5-b6c1-44932cb91bcf)
Pertama mencoba mencari user yang berhasil login, dari sana kita bisa mendapatkan informasi berupa username beserta passwordnya, dari sana kita berhasil mendapatkan flagnya
![Screenshot (19) (1)](https://github.com/user-attachments/assets/e6b54950-ddec-4730-ae19-ce7c41a21297)

### 3. Surprise
melanjutkan soal sebelumnya, disini kita diminta untuk mengetahui service yang digunakan oleh FTP server
![Screenshot (21)](https://github.com/user-attachments/assets/382ca43e-795d-4f25-8b32-305860853daf)
disana kita bisa mengetahui informasi tersebut telah disebut di paling awal
lalu untuk mengetahui nama file yang dikirim oleh attacker beradda di informasi paling bawah
![Screenshot (22)](https://github.com/user-attachments/assets/b532b773-39e5-40e5-9252-0e4661467679)
Selain itu, kita dimint auntuk mencari pesan yang ditinggalkan oleh attacker,
setelah saya mencari-cari, saya menemukan satu file yang cukup janggal dengan nama file yang sama dengan yang dikirim oleh attacker
![Screenshot (23)](https://github.com/user-attachments/assets/34081683-d9f6-4dfc-9588-dd02e426a547)
Setelah didecode, hasilnya adalah berbentuk leetspeet yanga dalah pesan dari attackernya
![Screenshot (24)](https://github.com/user-attachments/assets/ebab4cd2-eb4c-4467-bdce-eb6b90ae383f)

### 4. Gajah Terbang (Server Recon)
untuk soal ini, pertama saya mencari satu-satu hingga menemukan satu paket yang berisi informasi berupa nama, email, dan password, disana dapat ditemukan informasi berupa dbms yang digunakan di server tersebut, nama database, email, dan password dari admin
![Screenshot (28)](https://github.com/user-attachments/assets/1e8bc44b-78a5-4326-a2c2-a7895
![Screenshot (29)](https://github.com/user-attachments/assets/4939a533-2ae5-4a3e-aaf4-49a2799bc575)
802d1bf)
untuk port yang digunakan, bisa didapat dari package (174) tersebut juga
![Screenshot (27)](https://github.com/user-attachments/assets/750287bb-c217-4458-a8a3-557b60b9e451)
untuk password sendiri, diperlukan hashing dan hasilnya adalah sebagai berikut
![image](https://github.com/user-attachments/assets/1db2165d-c75f-43e9-9bf9-6693206b1056)

### 5. Gajah Terbang (Attacker Recon)
melanjutkan soal sebelumnya, menggunakan package yang sama, kita bisa mendapatkan informasi berupa
![Screenshot (26)](https://github.com/user-attachments/assets/31fd5099-46d8-47f5-b6ac-2023e807ff5a)
untuk bagian attacker, disini saya mencoba-coba saja, dan setelah mengamati dari informasi tersebut saya mendapatkan hasilnya
![image](https://github.com/user-attachments/assets/694caa7e-a4c2-466f-8117-c8b1a64baf63)
untuk password dari attacker saya dapatkan dari hashing password tersebut, dan ini hasilnya
![Screenshot 2024-09-19 003635](https://github.com/user-attachments/assets/eb82051d-64a6-4358-8cce-ddce1be59543)

### 6. Illegal Breakthrough (break.pcapng)
untuk menjawab pertanyaan pertama hingga terakhir, kita bisa mendapatkan informasi dari `tcp.stream eq 1917`
![image](https://github.com/user-attachments/assets/9c92d715-5622-4fe4-b073-20a314fc3753)
![image](https://github.com/user-attachments/assets/e799e963-21ee-4e0d-9013-9a9e80b606f2)
![image](https://github.com/user-attachments/assets/182d8867-1a3c-43aa-a783-cac73b8ce2fa)
untuk mencapai `tcp.stream eq 1917`, saya melihat stream awal-awal terlebih dahulu dan kelihatan jika kredensial selalu salah saat dimasukkan. Akhirnya saya mencoba untuk mengurutkan stream dari belakang dan akhirnya menemukan kredensial yang tepat.

### 7. Packets Barrage (break.pcapng)
setelah mencapai stream nomor 1917, stream selanjutnya adalah stream 1918, yang di mana di dalam stream tersebut attacker mengunduh sebuah file. IP address attacker juga tercantum di dalam stream ini.
![image](https://github.com/user-attachments/assets/26c7dbd1-d8b0-44b6-8387-9b61a7ee2b9e)
![image](https://github.com/user-attachments/assets/f5084c8a-2a57-400b-9c04-db98ebe4be7f)
![image](https://github.com/user-attachments/assets/5adeb7f6-c0fd-41d0-aac7-2472550f89a8)
![image](https://github.com/user-attachments/assets/19d965d7-3739-4c7f-abee-43da9be2522b)

### 8. Rizzset (riset.pcapng)
Dari wireshark, saya hanya mendapat informasi mengenai domain dari dns query pada log, yaitu www.its.ac.id. Untuk mendapat dns nya, saya melakukan ping kepada website ITS.
![image](https://github.com/user-attachments/assets/d990ce8f-12a1-4718-a9cb-f745b274d169)
![image](https://github.com/user-attachments/assets/283c16e2-ed1c-47c7-9f86-5aa26094b891)
Untuk mendapatkan JARM Fingerprint dari website ITS, saya menggunakan program python bernama `jarm.py` untuk mendapatkan JARM nya.
![image](https://github.com/user-attachments/assets/8130002b-c380-42f8-abf2-141aafbebf2a)
![image](https://github.com/user-attachments/assets/a21abce5-41e8-41f9-82cb-170af6787a75)

### 9. Corporate Breach (breach.pcap)
Untuk mendapatkan nama attacker, kita dapat melihat informasinya di `tcp.stream eq 0`
![image](https://github.com/user-attachments/assets/74a0136b-acca-42ce-ba67-5b490fb10316)
Untuk mendapatkan kredensial login, saya mengecek secara manual setiap stream dan saya menemukannya di `tcp.stream eq 207`
![image](https://github.com/user-attachments/assets/abe47863-0cdd-447a-865f-923d9998573e)
![image](https://github.com/user-attachments/assets/9663c278-545b-4d5a-a2a1-d7f6ea3ff971)

### 10. Malicious Code (breach.pcap)
Attacker melakukan bruteforce sebanyak 52 kali, dimulai dari stream 3 hingga stream 54 hingga ia mendapatkan `index.php`
![image](https://github.com/user-attachments/assets/006aecad-b327-4437-9f78-4d66b69e833c)
Di stream 207, attacker menemukan kredensialnya. Percobaan dilakukan dari stream ke 55 hingga 207 (153 kali)
![image](https://github.com/user-attachments/assets/885d9ae8-c123-4b27-a485-f40fba4b4e59)
Di stream 221, attacker meninggalkan sebuah pesan yang dapat dipecahkan menggunakan charcode, namun dengan pemenggalan angka yang baik
![image](https://github.com/user-attachments/assets/f5240607-d937-4dfe-b0de-2351b32aca15)
![image](https://github.com/user-attachments/assets/39083cab-12b2-477f-aae3-ef9c80985508)
![image](https://github.com/user-attachments/assets/04c707c1-15e2-4bc2-a085-1df83519a4b2)
![image](https://github.com/user-attachments/assets/47e5a8e8-bcc4-4d0e-957a-7fa5db0cc24b)

### 11. EZ (ez.pcapng)
Jawaban langsung ditemukan di `tcp.stream eq 0`
![image](https://github.com/user-attachments/assets/8e3e30ea-964f-4668-a47b-ef9f2d928646)
![image](https://github.com/user-attachments/assets/fc5b2903-b3c7-4aa7-a00e-a95191673d12)
![image](https://github.com/user-attachments/assets/b2983813-9232-4e28-9422-cc925cefadcb)

### 12. Stegography (image.pcap)

### 13. 22 Nightmare (oimazrim.pcap)

### 14. Pegawai Negeri Sebelah (rahasia.pcap)



