
---

# STM32 FreeRTOS-Demonstrate that the sharing of resources in a multitasking design can lead to a deterioration in system performance

## Overview
1. Green LED Task : Tugas ini bertanggung jawab untuk mengontrol LED Hijau. Diberikan prioritas "normal."
2. Red LED Task : Tugas ini bertanggung jawab untuk mengontrol LED Merah. Diberikan prioritas "normal."
3. Blue LED Task : Task ini bertanggung jawab untuk mengontrol LED Biru. Diberikan prioritas "di atas normal" (prioritas tertinggi di antara ketiga task).

   Semua task menggunakan shared software item (item perangkat lunak bersama), yang menjadi sumber daya yang dipakai bersama oleh ketiga tugas. Dalam kasus ini, item perangkat lunak bersama bertanggung jawab untuk mengontrol LED Biru.
   Diagram ini menunjukkan bahwa penggunaan sumber daya bersama dalam desain multitasking dapat menurunkan kinerja keseluruhan sistem karena potensi konflik atau penundaan akses ke sumber daya bersama.
   Task dengan prioritas lebih tinggi (LED biru) akan memiliki kesempatan lebih besar untuk mendapatkan akses ke shared software item, sehingga dapat menyelesaikan task lebih cepat dibandingkan tugas lain. Task dengan prioritas lebih rendah (LED Hijau dan Merah) mungkin mengalami penundaan jika task prioritas lebih tinggi sedang menggunakan sumber daya bersama.
   Dengan konfigurasi seperti ini, sistem memperlihatkan bahwa pengaturan prioritas dalam multitasking sangat penting untuk memastikan kelancaran operasional tugas, terutama ketika ada sumber daya yang digunakan bersama.

## Video Demo Execise 7
https://github.com/user-attachments/assets/5d3ad013-8eba-4415-bf3c-cce0940e2583

https://github.com/user-attachments/assets/de296e43-3b00-4b27-9b0f-243d5e906075
