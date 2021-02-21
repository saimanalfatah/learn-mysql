# Transaction Control Language
TCL adalah perintah SQL yang berhubungan dengan transaksi di database
## COMMIT
menyimpan transaksi secara permanen
> - START TRANSACTION;
> - INSERT INTO siswa VALUES(10, 'fabino', 23, 'brazil');
> - COMMIT;
## ROLLBACK
mengembalikan database ke bentuk awal / COMMIT terakhir
> - START TRANSACTION;
> - INSERT INTO siswa VALUES(10, 'fabino', 23, 'brazil');
> - ROLLBACK;
