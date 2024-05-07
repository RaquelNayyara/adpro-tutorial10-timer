# Tutorial 10 - Timer

#### Raquel Nayyara Aulia - 2206826583

## Understanding how it works
![Understanding how it works](assets/images/Understanding%20how%20it%20works.jpg)

Dalam gambar tersebut, terlihat bahwa output `hey hey` muncul sebelum `howdy!` dan `done!`. Output ini berasal dari thread utama, bukan dari tugas asinkron. Oleh karena itu, sampai `run()` di eksekutor dijalankan, pemanggilan `spawner.spawn(async {...});` tidak akan mulai mengeksekusi

## Multiple Spawn and removing drop
![Multiple Spawn and removing drop](assets/images/Multiple%20Spawn%20and%20removing%20drop.jpg)

Dalam output yang terlihat pada gambar, program tidak berhenti berjalan. Ini terjadi karena fungsi `drop` tidak dieksekusi, yang seharusnya memberi tahu eksekutor bahwa antrian tidak akan lagi menerima tugas baru. Selain itu, urutan pelaksanaan tugas tampak tidak konsisten, yang mungkin disebabkan oleh algoritma penjadwalan yang dipakai oleh eksekutor tersebut. Walaupun eksekusi tugas mungkin dilakukan secara berurutan, output yang dicetak tidak selalu menunjukkan urutan yang sama. Setiap tugas yang diciptakan oleh spawner memerlukan sumber daya, dan pembuatan tugas dalam jumlah besar dapat membuat program berjalan lebih lama serta eksekutor mungkin kesulitan dalam mengatur banyak tugas tersebut