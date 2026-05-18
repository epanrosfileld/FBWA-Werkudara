## >TAHAP 1 Persiapan Otak dan Sinyal
### 1. Reset Trim Remote 
reset seluruh trim remote radiomaster (subtrim=0)

### 2. Sesuaikan Pin dan Channel
Sesuaikan pin dan channel radiomaster dengan pin servo pixhawk baik secara wiring maupun program
<br> ++Werkudara menggunakan sistem pin AETR pada remote dan juga FC (Pixhawk). 

### 3. Radio Calibration 
Kalibrasi sinyal PWM remote radiomaster pada FC untuk mengetahui Trim, Min, dan Max sinyal dari remote.
<br> **SETUP -> Mandatory->Radio CAlibration**

### 4. Accelerometer Calibration & Level Calibration
Sebelum terbang menggunakan mode FBWA, wajib mengkalibrasi level dan accelerometer dahulu supaya FC mengetahui setiap posisi pesawat.
<br> **kalibrasi dahulu Level, lalu kalibrasi Accelerometer**
<img width="857" height="190" alt="image" src="https://github.com/user-attachments/assets/2fdef68c-d264-41bd-acb5-7acfa3abfaf2" />

### 5. Servo Output
Kondisi ideal trim pada servo output adalah Min=1100, Trim=1500, dan Max=2000. Namun jika kondisi visual dari flap atau rudder belum sejajar, maka angka bisa diganti dengan catatan tidak terlalu jauh dari angka ideal (Batas paling aman min=1400, trim=1500, max=1600.

### 6. Switch Mode
Pastikan sudah terdapat switch dengan mode FBWA diremote dan sudah terhubung pada FC. Tmbahkan mode autotune jika ingin mentunning PID dari pesawat secara otomatis.

### 7. ESC & Motor
Pastikan ESC dan motor bisa bergerak

# PENTING!!
### 1. PASTIKAN SELURUH TUAS DARI REMOTE SUDAH SESUAI DENGAN KELUARAN RADIO CALIBRATION PADA FC
### 2. PASTIKAN SWITCH SUDAH BISA TERHUBUNG PADA FC. PADA PIN DARI TUAS SWITCH (RC1-RC7), PASTIKAN VALUE BERNILAI 0 (do nothing)
### 3. SEBELUM TERBANG DI MODE FBWA, PASTIKAN KOREKSI DARI PROGRAM SUDAH BENAR. JIKA PESAWAT MIRING, PASTIKAN AILERON, RUDDER, DAN ELEVATOR MELAKUKAN COUNTER DARI POSISI MIRING SEHINGGA BERUSAHA MEMBALIKAN PESAWAT MENJADI CENTER


## FULL PARAMETER YANG KRUSIAL:
**RC1-RC7 (MIN)** -> Untuk mengatur sinyal PWM Min pada input (Disesuaikan dengan sinyal remote)
<br> **RC1-RC7 (MAX)** -> Untuk mengatur sinyal PWM Max pada input (Disesuaikan dengan sinyal remote)
<br> **RC1-RC7 (TRIM)** -> Untuk mengatur sinyal PWM trim (titik tengah) pada input (Disesuaikan dengan sinyal remote)
<br> **RCMAP** -> untuk mapping pin (PWM) pada FC terkait AETR.
<br> **LIM_ROLL_DEG** -> berguna untuk membatasi sudut roll dari pesawat 
<br> **LIM_PITCH_DEG** -> berguna untuk membatasi sudut pitch dari pesawat 
<br> **LIM_YAW_DEG** -> berguna untuk membatasi sudut yaw dari pesawat 






