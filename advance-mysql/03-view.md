# View
VIEW adalah perintah untuk membuat table virtual yang menyimpan kode SQL. Dengan view kita bisa membuat kode SQL yang komplek dikemas menjadi satu table sederhana. View akan menyimpan kode SQL yang komplek tadi menjadi single table virtual yang lebih mudah untuk digunakan

### Cara Menggunakan View
```sql
CREATE VIEW transaksiMhs AS 
SELECT mahasiswa.nim, nama, alamat, buku
FROM mahasiswa
INNER JOIN transaksi
ON mahasiswa.nim = transaksi.nim
```
> - SELECT * FROM transaksiMhs
> - SELECT nama, buku FROM transaksiMhs WHERE buku="Buku Matematika";

### Cara Menghapus View
> DROP VIEW transaksiMhs