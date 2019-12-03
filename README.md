# HA: Infinity Stones Vulnhub Walkthrough

### Anggota Kelompok
1. M Imam Pratama (09021281722063) - Ketua
2. Farhan Furqan (09021281722045) - Anggota
3. Defrian Afandi (09021281722075) - Anggota
4. Hafiz Mursid (09021281722066) - Anggota
5. Adinda Aisyah Rismayani (09021181722074) - Anggota
6. Tita Dwi Yulian (09021181722079) - Anggota

Kelompok kami akan menyelesaikan tantangan **HA: Infinity Stones. Tantangan ini menggambarkan Thanos yang<br>
berusaha mengumpulkan 6 Batu Infinity yang telah disembunyikan para Avanger di seluruh CTF. Thanos berpikir<br>
jika dia membunuh setengah dari seluruh kehidupan di alam semesta, dia akan mengembalikan keseimbangan (bisa <br>
lihat di film "Avangers : Infinity War"). Untuk melakukannya ia membutuhkan keenam Batu Infinity untuk menguatkan<br>
Infinity Gauntlet-nya (sarung tangan untuk menyatukan kekuatan 6 batu infinity), yang akan memberinya kemampuan<br>
untuk mengubah waktu, ruang, energi dan hukum fisika serta kenyataan. Beberapa informasi di film "Avangers: Infinity<br>
War" dapat membantu kita menyelesaikan CTF ini. Flag yang akan kita cari dalam tantangan ini antara lain:

- Mind Stone
- Reality Stone
- Time Stone
- Power Stone
- Soul Stone
- Space Stone

**Download HA: Infinity Stones** [di sini](https://www.vulnhub.com/entry/ha-infinity-stones,366/)<br>
**Level : Intermediate**<br>
**Tugas : Mencari 6 Flag (Stone)**

* ## Network Scanning
    - Netdiscover
    - Nmap Scan

* ## Enumaration
    - Browsing HTTP Service
    - Dirb-Brute forcing web directory
    - Exiftool-Metadata extracting for 1st stone
    - 2nd stone from ssl certificate
    - Brainfuck Language - Decoder
    - Crunch-generate dictionary
    - Aircrack-ng-cracking password of pcap
    
* ## Exploiting
    - Metasploit - Jenkins

* ## Post Enumaration
    - Obtain 4th stone
    - John the ripper-crack Keepaas hashes
    - Obtain 5th stone

* ## Privilege Escalation
    - Abusing sudo rights
    - Get the Final stone

# Walkthrough

## Network Scanning

## Enumaration

## Exploiting

## Post Enumaration

## Privilage Escalation


### Batu 1
Buka virtual box emulator HA: Infinity Stones, maka tampilannya seperti dibawah ini:<br>
![](img/1.png)<br>
Lakukan scanning network dengan netdiscover untuk mendapat IP dari virtual box HA: Infinity Stones, letak IP nya terdapat pada IP dengan MAC Vendor/ Hostname: _PCS Systemtechnik GmbH_.  
![](img/2.png)<br>
Scanning IP yang didapat dengan NMap, hasil dari scanning tersebut terdapat flag (stone) yaitu **MINDSTONE**.
![](img/3.png)

### Batu 2
Buka IP di browser, dan hasilnya:
![](img/4.png)<br>
Pilih tab either pada laman browser yang dibuka. Terdapat beberapa pertanyaan, tetapi ada kata kunci yang menerangkan _Computers tell us Binary is the path to Reality_ yang artinya nilai binary ini menunjukkan pada Reality (Reality Stones). Untuk jawaban false = 0 dan true = 1. Didapat jawaban yang benar dengan dari 8 pertanyaan yaitu **01101001**.
![](img/5.png)<br>
Lalu buka IP/Hasil jawaban yang berupa binary di laman browser. Terdapat hints.txt yang isinya berupa code.
![](img/6.png)<br>
Code yang didapat di decode dengan Brainfuck Decoder Language. Didapat hasil **admin: avangers**.
![](img/7.png)
![](img/8.png)
![](img/9.png)
![](img/10.png)
![](img/11.png)
![](img/12.png)

<!--
### Batu 3
![](img/13.png)
![](img/14.png)
![](img/15.png)
-->

### Batu 3
![](img/16.png)
![](img/17.png)
![](img/18.png)
![](img/19.png)
![](img/20.png)
![](img/21.png)
![](img/22.png)

### Batu 4
![](img/23.png)
![](img/24.png)
![](img/25.png)

### Batu 5
![](img/26.png)
![](img/27.png)
![](img/28.png)
![](img/29.png)
![](img/30.png)

### Batu 6
![](img/31.png)
![](img/32.png)
![](img/33.png)
![](img/34.png)
![](img/35.png)
