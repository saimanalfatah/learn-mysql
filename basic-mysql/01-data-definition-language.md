# Data Definition Language (DDL)
DDL merupakan perintah untuk menambah, merubah, dan menghapus struktur database
## CREATE
__a. Membuat Database__
> CREATE DATABASE school;

__b. Membuat Table__
> CREATE TABLE teachers (nis INT(10), nama VARCHAR(100), alamat VARCHAR(100), PRIMARY KEY(nis));

## Alter Table
__a. Menambah Kolom Table__
> ALTER TABLE teachers ADD umur INT(2);

__b. Modifikasi Kolom Table__
> ALTER TABLE teachers MODIFY COLUMN alamat VARCHAR(150);

__c. Menghapus Kolom Table__
> ALTER TABLE teachers DROP umur;

## TRUNCATE
__a. Menghapus semua record table__
> TRUNCATE TABLE teachers;

## RENAME
__a. Mengganti Nama Table__
> RENAME TABLE teachers to students;

## DROP
__a. Menghapus Table__
> DROP TABLE students

__b. Menghapus Database__
> DROP DATABASE school