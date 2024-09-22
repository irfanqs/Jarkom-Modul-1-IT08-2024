# Jarkom-Modul-1-IT08-2024

| Nama          | NRP          |
| ------------- | ------------ |
| Irfan Qobus Salim | 5027221058 |
| Aisha Ayya Ratiandari | 5027231056 |

# Daftar Isi

1. [Advance Sanity Check](#1-advance-sanity-check)
2. [FTP Login](#2-ftp-login)
3. [Surprise](#3-surprise)
4. [Gajah Terbang (Server Recon)](#4-gajah-terbang-server-recon)
5. [Gajah Terbang (Attacker Recon)](#5-gajah-terbang-attacker-recon)
6. [Illegal Breakthrough (break.pcapng)](#6-illegal-breakthrough-breakpcapng)
7. [Packets Barrage (break.pcapng)](#7-packets-barrage-breakpcapng)
8. [Rizzset (riset.pcapng)](#8-rizzset-risetpcapng)
9. [Corporate Breach (breach.pcap)](#9-corporate-breach-breachpcap)
10. [Malicious Code (breach.pcap)](#10-malicious-code-breachpcap)
11. [EZ (ez.pcapng)](#11-ez-ezpcapng)
12. [Stegography (image.pcap)](#12-stegography-imagepcap)
13. [22 Nightmare (oimazrim.pcap)](#13-22-nightmare-oimazrimpcap)
14. [Pegawai Negeri Sebelah (rahasia.pcap)](#14-pegawai-negeri-sebelah-rahasiapcap)

## Revisi
15. [innerRCE](#innerrce)
16. [simba](#simba)
17. [Baby Hengker](#baby-hengker)
18. [Adult Hengker](#adult-hengker)

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
melanjutkan soal sebelumnya, menggunakan package yang sama, kita bisa mendapatkan informasi berupa <br>
![Screenshot (26)](https://github.com/user-attachments/assets/31fd5099-46d8-47f5-b6ac-2023e807ff5a)
untuk bagian attacker, disini saya mencoba-coba saja, dan setelah mengamati dari informasi tersebut saya mendapatkan hasilnya
![image](https://github.com/user-attachments/assets/694caa7e-a4c2-466f-8117-c8b1a64baf63)
untuk password dari attacker saya dapatkan dari hashing password tersebut, dan ini hasilnya
![Screenshot 2024-09-19 003635](https://github.com/user-attachments/assets/eb82051d-64a6-4358-8cce-ddce1be59543)

### 6. Illegal Breakthrough (break.pcapng)
Untuk menjawab pertanyaan pertama hingga terakhir, kita bisa mendapatkan informasi dari `tcp.stream eq 1917`
![image](https://github.com/user-attachments/assets/9c92d715-5622-4fe4-b073-20a314fc3753)
![image](https://github.com/user-attachments/assets/e799e963-21ee-4e0d-9013-9a9e80b606f2)
![image](https://github.com/user-attachments/assets/182d8867-1a3c-43aa-a783-cac73b8ce2fa)
untuk mencapai `tcp.stream eq 1917`, saya melihat stream awal-awal terlebih dahulu dan kelihatan jika kredensial selalu salah saat dimasukkan. Akhirnya saya mencoba untuk mengurutkan stream dari belakang dan akhirnya menemukan kredensial yang tepat.

### 7. Packets Barrage (break.pcapng)
Setelah mencapai stream nomor 1917, stream selanjutnya adalah stream 1918, yang di mana di dalam stream tersebut attacker mengunduh sebuah file. IP address attacker juga tercantum di dalam stream ini.
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
Untuk mengetahui jumlah gambar yang dikirim, kita dapat mengeceknya di `tcp.stream eq 0`
![image](https://github.com/user-attachments/assets/fcd2b941-dd87-49ca-8eb1-52d9874a42da)
Untuk mengetahui pesan yang tersembunyi di dalam foto, kita perlu mengunduh fotonya dengan filezilla
![image](https://github.com/user-attachments/assets/51613226-7a15-4319-b40b-fe358f7f6d6e)
Setelah itu, kita dapat mengetahui foto tersebut memiliki pesan atau tidak menggunakan file python bawaan yang bernama `reversed.py`
![image](https://github.com/user-attachments/assets/fc1b3827-e4a1-4a39-b6c2-02fe5061833a)
![image](https://github.com/user-attachments/assets/38fdd95f-220e-4ba1-a903-56a932adc098)

### 13. 22 Nightmare (oimazrim.pcap)
Saya menggunakan filter untuk mencari tcp, kemudian saya menelusuri streamnya dan saya menemukan kredensial yang tepat di `tcp.stream eq 3`
![image](https://github.com/user-attachments/assets/7cb1b610-d517-4143-9902-c51e1aaa91cd)
Di stream tersebut, saya melihat bahwa ada gambar yang dikirimkan, oleh karena itu saya mencoba untuk mengakses gambar tersebut di filezilla dan menemukan 2 jenis file
![image](https://github.com/user-attachments/assets/208b3adf-a147-4368-abf5-658e2b4f6acb)
Di dalam file foto tersebut, terdapat kata string yang dimaksud di dalam soal
![image](https://github.com/user-attachments/assets/e9ceb007-a510-4865-91e8-faaeff6d4b84)
Untuk mengetahui kapan file kedua dikirim, saya menelusuri tiap stream dan saya menemukan stream ketika file kedua dikirim di stream nomor 141
![image](https://github.com/user-attachments/assets/1a34a933-545c-41b6-88e6-3ba45824ef80)
Untuk mengetahui nama pengirim, saya mencoba mengakses stream 142 dan menemukan informasi berikut
![image](https://github.com/user-attachments/assets/13d97a77-0935-4b5f-b0e5-2c869dcdfb66)
Setelah itu, decode dengan xor menggunakan key yang berada di dalam gambar
![image](https://github.com/user-attachments/assets/a95bab2d-cb4e-420d-a13a-01a5a97e9385)
![image](https://github.com/user-attachments/assets/bdbfed38-43de-40ec-83cf-27cde5c225c9)

### 14. Pegawai Negeri Sebelah (rahasia.pcap)
List nama, password, dan jabatan, langsung ditemukan di `tcp.stream eq 1`. Untuk mencari jawaban dari setiap pertanyaan, saya menggunakan fitur find untuk menemukan kredensial yang cocok
![image](https://github.com/user-attachments/assets/8dab55c7-85d4-4d7a-b607-53dde00f2d28)
![image](https://github.com/user-attachments/assets/7d157b48-2bb9-436f-90b4-b3cca842c7e7)

## Revisi

### innerRCE
1. Kapan hacker berhasil upload webshell?
    ![image](https://github.com/user-attachments/assets/ff071d28-7dc9-4df5-a421-c1de32fe6edc)
    setelah memfilter menggunakan HTTP, ada sebuah package yang menjelaskan bahwa hacker berhasil mengupload, yang dapat dilihat arrival datenya     
2. endpoint url dan server yang rentan
3. nama webshell yang diupload    
     ![image](https://github.com/user-attachments/assets/09fc1bf1-deac-49c8-b292-5429cb970f7c)
    endpoint dan nama webshell ada di package tersebut    
4. command pertama yang berhasil dieksekusi    
    ![image](https://github.com/user-attachments/assets/fe572e0c-47cd-4fd3-98e8-a4182304c20b)
    melihat dari waktunya, maka command pertama yang berhasil dieksekusi tertera diatas yaitu “whoami”    
5. Berdasarkan log, hacker tersebut mencoba menuliskan pesan, apa pesan yang hacker coba tuliskan?    
    selain command “whoami”, hacker juga meng-echo berupa encode base64    
    ![image](https://github.com/user-attachments/assets/956c72a7-0612-4ccc-ba3c-16fcbdf2a473)
    yang dimana, setelah di decode akan menampilkan pesannya    
   ![image](https://github.com/user-attachments/assets/ccc3313d-403e-41c3-ada2-7a9dca3227e2)
soal selesai dan menampilkan flagnya
![image](https://github.com/user-attachments/assets/a8f89d25-bd63-4881-be8d-0aa730b1604c)

### simba
Untuk menjawab pertanyaan pertama, saya mencoba untuk menjawab semua protokol yang ada, kemudian ditemukan jawabannya yaitu SMB
![image](https://github.com/user-attachments/assets/020795d5-c919-4355-a5c4-878198b82939)
Selanjutnya, untuk mencari nama user, saya menggunakan find untuk mencari nama user. Dalam baris ini, terlihat jelas bahwa path tersebut menyebutkan nama usernya, yaitu mmeyers
![image](https://github.com/user-attachments/assets/b33a2679-7f03-47d6-8ac2-319df2a87ed1)
Untuk mendapatkan file yang terleak setiap enumerasinya, saya menggunakan fitur Export Objects > SMB untuk mencari jumlah filenya. Terhitung ada 14 file yang terleak
![image](https://github.com/user-attachments/assets/57b669f7-6866-43ac-a9a3-8f295ba1e16d)
![image](https://github.com/user-attachments/assets/e12d88b3-fec8-4429-b179-081e07088811)

### Baby Hengker
Untuk menemukan kapan attacker masuk, kita dapat melihat data dari frame nomor 8
![image](https://github.com/user-attachments/assets/6ddce9da-e649-4739-92dc-6cc9269693c8)
Setelah itu, untuk mendapatkan informasi lebih terhadap USB tersebut, kita perlu menggunakan USB Keyboard Parser, yang dapat dijalankan menggunakan python
![image](https://github.com/user-attachments/assets/b1ff9667-29f8-4e96-812f-2d9e77e321c0)
Kita perlu menghapus kata yang double, sehingga kalimat menjadi `ini password wifinya apa ya?`. Setelah itu kita bisa mendapatkan flagnya
![image](https://github.com/user-attachments/assets/9352f3aa-beca-4cda-8a2b-dae428a3008b)

### Adult Hengker
Untuk mengetahui device yang digunakan oleh mahasiswa, kita dapat menemukannya pada baris berikut. Terlihat bahwa mahasiswa tersebut menggunakan mouse
![image](https://github.com/user-attachments/assets/b79ae857-98b7-430c-ba8c-2329d33e4cb6)
Untuk mendapatkan string yang ditanyakan, kita perlu menggunakan file USB Mouse Visualizer, yang dijalankan menggunakan python
![image](https://github.com/user-attachments/assets/a0cc1ecb-0abc-4513-b4db-761aca946e7a)
Setelah itu, file csv yang didapatkan perlu dimasukkan ke dalam tools online untuk memvisualisasi csv tersebut
![image](https://github.com/user-attachments/assets/edeaec1f-d3f1-4300-af96-3242954376d7)
Setelah itu, kita bisa mendapatkan flagnya
![image](https://github.com/user-attachments/assets/ec938981-f412-4327-aeaa-e6b08aefd6fd)










