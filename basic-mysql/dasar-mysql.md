__Install MySQL__
> - sudo apt install mysql-server
> - sudo mysql_secure_installation
> - SELECT user,authentication_string,plugin,host FROM mysql.user;

__Enable dan Disable Service MySQL__
> - sudo systemctl disable mysql / sudo service mysql disable
> - sudo systemctl enable mysql / sudo service mysql enable

__Menghapus Auto Startup__
> sudo update-rc.d -f mysql remove

__Melihat Status MySQL__
> sudo service mysql status > sudo systemctl status mysql

__Restart, Start dan Stop__
> - sudo service mysql restart / sudo systemctl restart mysql
> - sudo service mysql start / sudo systemctl start mysql
> - sudo service mysql stop / sudo systemctl stop mysql

__Membuat user__
> CREATE USER 'user'@'localhost' IDENTIFIED BY 'password';

__Melihat Daftar User__
> SELECT * FROM mysql.user
> SELECT user, host FROM mysql.user

__Menghapus User__
> DROP USER 'admin'@localhost';

__Rename Database Name__
> CREATE DATABASE sekolah;
> RENAME TABLE school.siswa TO sekolah.siswa, school.guru TO sekolah.guru;
> DROP DATABASE school;

__Cara Export DAN Import MySQL__
> mysqldump -u admin -p sekolah > sekolah.sql
> mysql -u admin -p sekolah-dasar < sekolah.sql

# Dasar MySQL
__1. Masuk MySQL__
> - sudo mysql
> - mysql -u root -p

__2. Hapus Layar__
> - ctrl + l
> - \! clear
> - system clear

__3. Melihat Daftar Database__
> SHOW DATABASES;

__4. Menghapus Database__
> DROP DATABASE universitas;

__5. Menggunakan Database__
> USE universitas;

__6. Melihat Daftar Table__
> SHOW TABLES;

__7. Menghapus Table__
> DROP TABLE mahaiswa;

__8. Menampilkan Struktur Tabel__
> DESCRIBE mahasiswa;
> DESC mahasiswa;

__Catatan__
\G -> perintah untuk mengganti ; hasil bukan berbentuk tabel
Sumber -> ngodingdata.com