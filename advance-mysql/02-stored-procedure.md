# Stored Procedure
Stored Procedure adalah sebuah fungsi berisi kode SQL yang dapat digunakan kembali. Dalam Stored Procedure juga dapat dimasukkan parameter sehingga fungsi dapat digunakan lebih dinamis berdasarkan parameter tersebut

#### CONTOH 1
1. Cara membuat Store Procedure
```sql
DELIMITER $$
 
CREATE PROCEDURE selectMahasiswa()
BEGIN
    SELECT nim, nama FROM mahasiswa;
END$$

DELIMITER ;
```
2. Cara memanggil Store Procedure
> CALL selectMahasiswa();

#### CONTOH 2 Menggunakan Parameter
1. Membuat Store Procedure
```sql
DELIMITER $$
 
CREATE PROCEDURE alamatMahasiswa
(
	alamatMhs VARCHAR(100)
)
BEGIN
    SELECT * 
    FROM mahasiswa
    WHERE alamat = alamatMhs;

END$$

DELIMITER ;
```
2. Memanggil Store Procedure
> CALL alamatMahasiswa("bandung")

### CONTOH 3 DML Store Procedure
1. Membuat Store Procedure
```sql
DELIMITER $$
 
CREATE PROCEDURE insertMahasiswa
(
	nimMhs INT(10),
	namaMhs VARCHAR(100),
	alamatMhs VARCHAR(100)
)
BEGIN
    INSERT INTO mahasiswa 
    VALUES (nimMhs, namaMhs, alamatMhs);

END$$

DELIMITER ;
```
2. Memenggil Store Procedure
> CALL insertMahasiswa(21400207,"joni","jakarta");



