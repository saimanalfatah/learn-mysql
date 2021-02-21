# Data Control Language
DCL adalah perintah SQL untuk control dan permission database
### GRANT
memberikan hak akses kepada pengguna
> - GRANT ALL PRIVILEGES ON *.* TO 'user'@'localhost';
> - GRANT CREATE ON school.students TO 'user'@'localhost';
> - GRANT CREATE, INSERT, UPDATE, DELETE ON school.students TO 'user'@'localhost';

mengkonfirmasi perubahan
> FLUSH PRIVILEGES

melihat hak akses user
> SHOW GRANTS FOR 'user'@'localhost' \G
> SHOW GRANTS FOR 'user'@'localhost';


Beberapa opsi perintah GRANT antara lain:
1. ALL PRIVILEGES -> memberikan akses full kecuali GRANT OPTION
2. CREATE -> memberikan akses membuat table / database;
3. DROP -> memberikan akses menghapus table / database
4. SELECT -> memberikan akses query table
5. INSERT -> memberikan akses menambah table
6. UPDATE -> memberikan akses menghapus table
7. DELETE -> memberikan akses menghapus table
8. Dan lain-lain

## REVOKE 
mencabut hak akses yang diberikan melalui perintah GRANT
> - REVOKE ALL ON *.* FROM 'user'@'localhost';
> - REVOKE INSERT ON *.* FROM 'user'@'localhost';