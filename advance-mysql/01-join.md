# JOIN
JOIN merupakan perintah di MySQL untuk menggabungkan 2 table atau lebih berdasarkan kolom yang sama

### Inner Join
INNER JOIN membandingkan record di setiap table untuk dicek apakah nilai sama atau tidak. Jika nilai kedua table sama maka akan terbentuk table baru yang hanya menampilkan record yang sama dari kedua table
> SELECT * FROM mahasiswa INNER JOIN transaksi ON mahasiswa.nim = transaksi.nim;

### Left Join
LEFT JOIN menghasilkan nilai berdasarkan table kiri (table1) dan nilai yang sama di table kanan. Jika table kanan tidak ada nilainya maka akan diisi nilai NULL
> SELECT * FROM mahasiswa LEFT JOIN transaksi ON mahasiswa.nim = transaksi.nim;

### Right Join
Konsep RIGHT JOIN hampir sama seperti LEFT JOIN hanya yang menjadi master adalah table kanan. 
> SELECT * FROM mahasiswa RIGHT JOIN transaksi ON mahasiswa.nim = transaksi.nim;