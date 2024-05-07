# Tutorial 10 - Timer

#### Raquel Nayyara Aulia - 2206826583

## Understanding how it works
![Understanding how it works](assets/images/Understanding%20how%20it%20works.jpg)

Dalam gambar tersebut, terlihat bahwa output `hey hey` muncul sebelum `howdy!` dan `done!`. Output ini berasal dari thread utama, bukan dari tugas asinkron. Oleh karena itu, sampai `run()` di eksekutor dijalankan, pemanggilan `spawner.spawn(async {...});` tidak akan mulai mengeksekusi tugasnya.