# Tutorial 8 Subscriber

#### Raquel Nayyara Aulia - 2206826583

### what is amqp?
AMQP adalah singkatan dari Advanced Message Queuing Protocol. Ini adalah protokol lapisan open-standard application layer protocol untuk message-oriented middlewar. Dengan kata lain, ini adalah cara bagi komponen perangkat lunak yang berbeda untuk berkomunikasi satu sama lain dengan mengirimkan pesan. AMQP mendefinisikan serangkaian aturan dan format untuk pertukaran pesan antara sistem yang berbeda, sehingga memudahkan aplikasi perangkat lunak yang berbeda, ditulis dalam bahasa pemrograman yang berbeda dan berjalan pada platform yang berbeda, untuk berkomunikasi satu sama lain secara dapat diandalkan dan efisien

### What does guest:guest@localhost:5672 mean? what is the first guest, and what is the second guest, and what is localhost:5672 is for?
`guest:guest@localhost:5672` adalah URI koneksi yang terdiri dari `<pengguna>:<kata sandi>@<host>:<port>`:

1. `guest` pertama adalah nama pengguna yang digunakan untuk autentikasi pada server RabbitMQ, seringkali merupakan nama pengguna bawaan.
2. `guest` kedua adalah kata sandi pengguna. Pada RabbitMQ, kata sandi standar juga seringkali adalah `guest`.
3. `localhost:5672` adalah nama host dan nomor port yang digunakan oleh broker AMQP. `localhost` menunjukkan broker AMQP dijalankan pada mesin yang sama dengan kode, dan `5672` adalah port bawaan untuk komunikasi AMQP.

### Simulation slow subscriber
![Simulation slow subscriber](assets/image/Simulation%20slow%20subscriber.jpg)Queued Message di broker akan meningkat karena adanya penundaan yang diterapkan, menyebabkan publisher mengirim pesan lebih cepat daripada subscriber menerimanya. Dalam situasi saya, jumlah pesan yang queued message di broker adalah 16 setelah menjalankan Publisher sebanyak 5 kali.