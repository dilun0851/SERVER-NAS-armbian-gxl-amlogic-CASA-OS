# SERVER-NAS-armbian-gxl-amlogic-CASA-OS
SERVER NAS armbian gxl amlogic ( CASA OS ) adalah server nas menggunakan hardware stb hg680p ram 2 GB software armbian gxl menggunakan Casa OS

# BAHAN INSTALL NAS CASA OS STB HG680P ARMBIAN 21 AMLOGIC GXL:

1. FLSHDISK ATAU SD CARD ORIGINAL MINIMAL 4 GB MAKSIMAL 1 TB

2. DOWNLOAD "BAHAN NAS CASA OS"

3. ZEROTIER NETWORK ID

4. BELI STB HG680P UNLOCK AKSES ROOT SD CARD & FLASHDISK


# PANDUAN INSTALL NAS CASA OS STB HG680P ARMBIAN 21 AMLOGIC GXL:

1. SIAPKAN BAHAN FILE FLASHING

2. SIAPKAN FLASHDISK ATAU MEMORI SD Card. Catatan: flashing memori SD Card 
   atau flashdisk original jangan KW nanti gagal booting ke file armbian

4. Nyalakan PC/Laptop untuk proses download bahan flashing lalu di flashing

5. Download Bahan FLASHING INSTALL NAS CASA OS STB HG680P ARMBIAN 21 AMLOGIC GXL DI LINK INI: 

6. EKTRAK FILE BAHAN TERSEBUT APLIKASI RAR.EXE

7. INSTALL BALENA ETCHER DI WINDOWS 7/8/10/11/MAC OS

8. INSTALL PUTTY DI WINDOWS 7/8/10/11/MAC OS

9. Colokan flashdisk atau memori sd card ke pc atau laptop

10. BUKA BALENA ETCHER klik "Flash from file" lalu cari file "Armbian_
    21.08.1_Amlogic-GXL_bullseye_current_5.10.60.img.xz"

11. Select target flashdisk atau memori SD Card ORIGINAL yang akan di 
    flashsing lalu tunggu sampai flashing selesai. saat ada tulisan validating 
    boleh di "skip>>"

12. Cabut flashdisk atau memori sd card dari laptop atau PC

13. Colok flashdisk atau memori sd card ke stb hg680p

14. HUBUNGKAN STB HG680P KE LUBANG LAN ROUTER ATAU MIKROTIK

15. HUBUNGKAN LAPTOP ATAU PC KE LUBANG LAN ROUTER ATAU MIKROTIK YANG 
    TERHUBUNG KE STB HG680P

16. Nyalakan stb hg680p tunggu sampai booting selesai

17. Cek IP Address STB HG680P di router atau mikrotik

18. Untuk melihat IP Address semua devices terhubung ke router di bagian:

    Tenda N301: IP defaults: 192.168.0.1 > Bandwidth Control > Attached Devices

    Mikrotik: Neighbors > "Klik IP Address 192.168._._/10._._._" > Connect > IP > DHCP   
              Server > Leases

    TL-WR844N: IP defaults: 192.168.0.1/192.168.1.1 > Local Password defaults: 
              admin/user > Network Map > Clients

    TL-WR940N: IP defaults: 192.168.1.1 > Username defaults: admin/user dan 
               Password defaults: admin/user > Network Map > Clients

19. Buka putty windows/mac os

20. Masukan IP Address router ke putty di bagian Host Name (or IP address):    
    192.168._._/10._._._ dan Port: 22 lalu Open

21. Masukan login defaults as: root dan password: 1234

22. Isi new root password dan repeat password

23. Ketik "1"

24. Isi profile a username (eg. your forename)

25. Isi create password dan repeat password lalu enter 2 kali

26. Ketik "y"

27. Ketik "3"

28. Ketik "3"

29. Ketik "sudo apt update"

30. Ketik "curl -fsSL https://get.casaos.io | sudo bash"

31. Buka tab baru di browser lalu cari "http://*.*.*.*"

32. Enter lalu klik go

33. Isi new username dan password lalu confirm password


# PANDUAN MENGONLINEKAN SERVER LOCAL KE PUBLIK VIA ZEROTIER:

1. CARI DI BROWSER ZEROTIER.COM

2. KLIK GET ZEROTIER

3. LOGIN MENGGUNAKAN GOOGLE BIAR CEPAT

4. CREATE A NETWORK

5. HALAMAN BROWSER ZEROTIER JANGAN DI TUTUP DULU

6. BUKA PUTTY WINDOWS/MAC OS

7. Masukan IP Address router ke putty di bagian Host Name (or IP address):    
    192.168._._/10._._._ dan Port: 22 lalu Open

9. Masukan login as: root dan password: "BARU KALIAN GANTI BARU"

10. ketik "curl -s https://install.zerotier.com | bash"

11. ketik "systemctl enable zerotier-one.service"

12. ketik "zerotier-cli join "network_id""

13. INSTALL ZEROTIER DI HANDPHONE ANDROID

14. ADD NETWORK LALU MASUKAN NETWORK ID TADI YANG SUDAH DI BUAT DI BROWSER

15. CENTANG HIJAU ROUTE ALL TRAFFIC LALU ADD

16. IZINKAN AKSES NETWORK ID DI BROWSER URL: 
    https://my.zerotier.com/network/"NETWORK_ID"

17. BAGIAN MEMBERS > SWITCH TO BETA LIST > AUTH? CENTANG HIJAU SEMUA LALU DI 
    KASIH "SHORT-NAME"
