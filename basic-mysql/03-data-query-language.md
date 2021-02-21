# Data Query Language
DQL adalah perintah SQL untuk query data, perintah DQL yaitu SELECT. Carapenulisan perintah select yaitu;
> SELECT nama, alamat, umur FROM siswa;
 
Jika ingin membaca semua field table
> SELECT * FROM siswa;

### WHERE
Digunakan untuk filter pencarian data
> SELECT * FROM siswa WHERE nama="salah";

### AND, OR, NOT
> - SELECT * FROM siswa WHERE nama="salah" AND alamat="mesir";
> -  SELECT * FROM siswa WHERE nama="salah" OR alamat="mesir";
> - SELECT * FROM siswa WHERE NOT nama="salah";

### LIKE
Digunakan untuk mencari data yang lebih spesifik
> SELECT * FROM siswa WHERE NOT nama LIKE "%la%";

### ORDER BY
Digunakan untuk mengurutkan data
> - SELECT * FROM siswa ORDER BY nama ASC;
> - SELECT * FROM siswa ORDER BY nama DESC;

### LIMIT
Digunakan untuk membatasi hasil pencarian
> SELECT * FROM siswa ORDER BY nama DESC LIMIT 2;

### AGGREGATION
Digunakan untuk mendapatkan satu nilai berdasarkan hasil kalkulasi. beberapa fungsi yang banyak digunakan seperti COUNT(), MIN(), MAX(), AVG(), SUM()
1. COUNT
Digunkan untuk mencari jumlah data
> SELECT COUNT(*) FROM siswa;

2. MIN
Digunakan untuk mencari nilai terkecil
> SELECT MIN(umur) FROM siswa;

3. MAX
Digunakan untuk mencari nilai terbesar
> SELECT MAX(umur) FROM siswa;

4. AVG
Digunakan untuk mencari rata-rata
> SELECT AVG(umur) FROM siswa;

5. SUM
Digunakan untuk mencari jumlah siswa
> SELECT SUM(umur) FROM siswa;

### GROUP BY
Mengelompokkan nilai yang sama berdasarkan field;
> - SELECT alamat, COUNT(*) FROM siswa GROUP BY alamat;

> - SELECT alamat, COUNT(*) as jumlah FROM siswa GROUP BY alamat ORDER BY jumlah DESC;

> - SELECT alamat, AVG(umur) as rata FROM siswa GROUP BY alamat ORDER BY rata ASC;

