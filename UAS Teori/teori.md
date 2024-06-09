<h2>01.Querry Demo :</h2>

SELECT nama_user
FROM user
WHERE jenis_kelamin="P"
ORDER BY nama_user ASC

![Screenshot 2024-06-10 004057](https://github.com/elsa177/Learn-MyPHP-Admin/assets/160198836/1d8b1b85-f915-496f-b8e2-83dd57f0e1c7)


![Screenshot 2024-06-08 230734](https://github.com/elsa177/Learn-MyPHP-Admin/assets/160198836/17ca34c7-cb9a-43d5-82ef-08587355a5b0)

<h2>02.Querry Soal</h2>

SELECT nama_user, tanggal_lahir
FROM user
WHERE jenis_kelamin="L"
ORDER BY tanggal_lahir DESC;

![Screenshot 2024-06-10 004148](https://github.com/elsa177/Learn-MyPHP-Admin/assets/160198836/ccb4be8d-91a3-4aec-b698-aa39c67f4e2d)

![Screenshot 2024-06-08 231115](https://github.com/elsa177/Learn-MyPHP-Admin/assets/160198836/b8477166-acd1-43f9-8f5e-ee95b863a3f7)

<h2>03.Course Join</h2>

SELECT
  kursus.judul,
  SUM(transaksi.total) AS total
FROM kursus
JOIN detail_transaksi ON detail_transaksi.id_kursus=kursus.id
JOIN transaksi ON detail_transaksi.id_transaksi=transaksi.id
WHERE transaksi.status = 'Completed'
GROUP BY kursus.judul
ORDER BY total DESC;

![Screenshot 2024-06-10 004220](https://github.com/elsa177/Learn-MyPHP-Admin/assets/160198836/578fd961-bf42-42b6-8c08-82cc977ba353)


![Screenshot 2024-06-08 232953](https://github.com/elsa177/Learn-MyPHP-Admin/assets/160198836/333ca7bc-8011-4777-b81d-8ac68b32e51b)

<h2>04.Hewan Join</h2>

SELECT
  user.nama,
  SUM(pelayanan.harga) AS total
FROM reservasi
JOIN user ON user.id = reservasi.id_user
JOIN pelayanan ON reservasi.id_pelayanan = pelayanan.id
WHERE reservasi.status = 'Completed'
GROUP BY user.nama
ORDER BY total DESC
LIMIT 1;

![Screenshot 2024-06-10 004343](https://github.com/elsa177/Learn-MyPHP-Admin/assets/160198836/38724e49-cc3f-4c65-ba0e-0ab5cda2678e)


![Screenshot 2024-06-08 232235](https://github.com/elsa177/Learn-MyPHP-Admin/assets/160198836/7ead354a-9444-4599-a185-da9f3c5b6ae5)

<h2>05.Hewan Reservasi</h2>

SELECT jenis_peliharaan, COUNT(jenis_peliharaan) AS total
FROM reservasi
GROUP BY jenis_peliharaan;

![Screenshot 2024-06-10 004423](https://github.com/elsa177/Learn-MyPHP-Admin/assets/160198836/cff1e930-5403-4866-9e70-6a2177a6fa77)


![Screenshot 2024-06-08 233439](https://github.com/elsa177/Learn-MyPHP-Admin/assets/160198836/16f919bb-1183-4eab-8ce9-0e5cb09e4ebb)
