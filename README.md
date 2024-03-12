# Modul 5

## Reflection

1) Performance testing menggunakan JMeter fokus pada simulasi penggunaan aplikasi oleh banyak orang sekaligus. Hal ini dapat dilakukan dengan menentukan jumlah thread group (user) saat melakukan testing. Sementara itu, performance testing menggunakan IntelliJ Profiler fokus pada bagian-bagian code spesifik yang memakan waktu banyak. Hal ini dapat dilihat dari jumlahh milisecond pada masing-masing method yang dijalankan.
2) Saya dapat melihat durasi yang dibutuhkan setiap method untuk dieksekusi, dan mencari method mana yang waktu eksekusinya besar. Dari sini sayang dapat melakukan refactoring untuk optimisasi code. Tanpa profiling, saya tidak tahu pasti bagian code mana yang masih lambat.
3) Ya, menurut saya IntelliJ Profiler cukup efektif, karena saya dapat langsung melihat durasi eksekusi method di samping code method itu sendiri, sehingga mudah digunakan.
4) Tidak ada tantangan yang cukup berarti. Instruksi dari tutorial sudah cukup jelas.
5) 1. Saya dapat langsung melihat bagian code mana yang lambat menggunakan data empiris, tidak perlu menganalisis kompleksitas code sendiri. 2. Penyajian data dilakukan tepat di samping code, sehingga nyaman digunakan.
6) Jika terdapat perbedaan, saya akan fokus pada test dengan hasil yang lebih buruk, dan mencoba memperbaikinya secara independen. Misal jika hasil JMeter baik namun hasil Profiling buruk, saya akan fokus memperbaiki profiling yang buruk itu tersebut.
7) Pada tutorial ini, ada 2 strategi yang saya implementasikan. 1. membuat query baru pada repository. Daripada memproses hasil query agar sesuai dengan yang diinginkan, lebih baik mengubah query itu sendiri sehingga langsung memberikan hasil yang diinginkan. 2. Menggunakan StringBuilder ketimbang konkatenasi string (untuk joinStudentNames), karena StringBuilder bersifat mutable, sehingga konkatenasi jauh lebih sederhana untuk dilakukan. Untuk memeriksa fungsionalitas, saya memastikan tipe data output sama, jumlah data pada output sama, dan mengecek beberapa sample output spesifik.


## Screenshots

All Student Names (before profiling)
![all-student](https://github.com/DaWanAnOnli/exercise-profiling/assets/124868777/72ebfaae-9b63-4c05-9eed-aac899cefda5)

All Student Names log
![all-student log](https://github.com/DaWanAnOnli/exercise-profiling/assets/124868777/9627edd9-84ca-4e70-a5a2-a4690cb8ac14)

Highest Gpa (before profiling)
![highest gpa](https://github.com/DaWanAnOnli/exercise-profiling/assets/124868777/440af796-dd2b-4127-8010-53704fa9f812)

Highest Gpa log
![highest gpa log](https://github.com/DaWanAnOnli/exercise-profiling/assets/124868777/1662ff52-d695-4644-be43-6734cc03c045)


All Student Names (after profiling)
![all-student after optimization](https://github.com/DaWanAnOnli/exercise-profiling/assets/124868777/5917f276-3259-4229-9e4b-27d1b1c1dfc7)


Highest Gpa (after profiling)
![highest gpa after optimization](https://github.com/DaWanAnOnli/exercise-profiling/assets/124868777/ddd20521-3928-41c3-80c8-06b5e86ccd18)


Dapat dilihat secara rata-rata sample time dan latency dari request jauh lebih kecil setelah dilakukan profiling. Hal ini menunjukkan aplikasi berjalan jauh lebih cepat setelah dilakukan profiling.

