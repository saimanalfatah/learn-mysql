# TRIGGER
TRIGGER adalah kumpulan kode SQL yang berjalan secara otomatis untuk mengeksekusi perintah INSERT, UPDATE, DELETE. Biasanya TRIGGER akan dijalankan sebelum atau sesudah proses INSERT, UPDATE, DELETE (Perintah DML).

BEFORE INSERT -> TRIGGER dijalankan sebelum record dimasukkan ke database
AFTER INSERT  -> TRIGGER dijalankan sesudah record dimasukkan ke database
BEFORE UPDATE -> TRIGGER dijalankan sebelum record dirubah di database
AFTER UPDATE  -> TRIGGER dijalankan sesudah record dirubah database
BEFORE DELETE -> TRIGGER dijalankan sebelum record dihapus di database
AFTER DELETE  -> TRIGGER dijalankan sesudah record dihapus di database

1. Membuat Trigger
```sql
DELIMITER $$
CREATE TRIGGER update_alamat_mahasiswa 
    BEFORE UPDATE 
    ON mahasiswa
    FOR EACH ROW 
BEGIN
    INSERT INTO log_mahasiswa
    set nim = OLD.nim,
    alamat_lama=old.alamat,
    alamat_baru=new.alamat,
    waktu = NOW(); 
END$$
DELIMITER ;
```

2. Testing
> - UPDATE mahasiswa SET alamat = 'surabaya' WHERE nim = 21400200;
> - SELECT * FROM log_mahasiswa;
> - SELECT * FROM mahasiswa WHERE nim=21400200;