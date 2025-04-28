# Multiprosessor-Multiple
Multiprocessor dan Multiple Processor sebenarnya istilah yang mirip, tapi dalam konteks teknis mereka sedikit beda penekanan:
Multiprocessor: Sistem terintegrasi yang memiliki lebih dari satu CPU, biasanya dalam satu sistem berbagi memori, bus, dan I/O.
Multiple Processor: Hanya menekankan ada banyak prosesor, tapi belum tentu saling terhubung erat atau berbagi memori

## Gambar sebelah kiri: (Symmetric Multiprocessor Architecture)
- Ini adalah Symmetric Multiprocessor Architecture (SMP).
- Sistem Controller Mengatur akses ke Memory System controller memastikan CPU yang mau baca/tulis ke memory tidak bentrok dengan CPU lain.
Jadi kalau ada banyak CPU mau akses memory barengan, system controller yang mengatur siapa duluan (arbitrasi). Jadi System Controller itu seakan Polisi lalu lintas yang mengatur jalannya data antara CPU, memory, dan I/O device, supaya semuanya teratur dan tidak tabrakan.
- Semua CPU memiliki hak akses yang sama terhadap memori dan I/O Devices, dan setiap CPU bisa mengambil tugas sendiri tanpa harus minta izin prosesor lain.
- Setiap CPU memiliki L1 Cache untuk mempercepat akses data lokal.
- Semua CPU berkomunikasi melalui System Bus yang sama.

## Gambar sebelah kanan: (Asymmetric Multiprocessor Architecture)
- Ini adalah arsitektur multiprosesor tipe Master-Slave.
- Terdapat Master Processor yang mengontrol seluruh sistem.
- Slave Processor bertugas untuk menjalankan perintah atau tugas yang diberikan oleh Master.
- Semua komunikasi antar prosesor dilakukan lewat System Bus.
- Setiap Slave memiliki Memory masing-masing.
- I/O Devices juga terhubung ke System Bus.

  - Kesimpulannya: Symmetric Multiprocessor (SMP): Semua CPU setara, berbagi memori dan I/O secara bersama-sama lewat sistem bus yang sama, diatur oleh system controller.
Asymmetric Multiprocessor (AMP): Ada satu Master Processor yang mengontrol sistem, mengatur dan memerintah, dan Slave Processor hanya menjalankan perintah dari Master, masing-masing dengan memori sendiri.
