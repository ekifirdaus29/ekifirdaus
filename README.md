Enter password: ***
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 6
Server version: 5.5.51 MySQL Community Server (GPL)

Copyright (c) 2000, 2016, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> create database mahasiswa;
Query OK, 1 row affected (0.01 sec)

mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| latihan01          |
| mahasiswa          |
| mhs                |
| mysql              |
| performance_schema |
| praktikum          |
| sekolah            |
| test               |
+--------------------+
9 rows in set (0.01 sec)

mysql> use mahasiswa;
Database changed
mysql> create table mahasiswa01
    -> (nim char (10) primary key,
    -> nama varchar (20) not null,
    -> alamat_jalan varchar (20) not null,
    -> kota varchar (15) not null,
    -> kode_pos varchar (10) not null,
    -> no_hp varchar (15) not null,
    -> jenis_kelamin varchar (15) not null,
    -> tgl_lahir varchar (15) not null,
    -> kode_dosen varchar (20) not null);
Query OK, 0 rows affected (0.13 sec)

mysql> desc mahasiswa01;
+---------------+-------------+------+-----+---------+-------+
| Field         | Type        | Null | Key | Default | Extra |
+---------------+-------------+------+-----+---------+-------+
| nim           | char(10)    | NO   | PRI | NULL    |       |
| nama          | varchar(20) | NO   |     | NULL    |       |
| alamat_jalan  | varchar(20) | NO   |     | NULL    |       |
| kota          | varchar(15) | NO   |     | NULL    |       |
| kode_pos      | varchar(10) | NO   |     | NULL    |       |
| no_hp         | varchar(15) | NO   |     | NULL    |       |
| jenis_kelamin | varchar(15) | NO   |     | NULL    |       |
| tgl_lahir     | varchar(15) | NO   |     | NULL    |       |
| kode_dosen    | varchar(20) | NO   |     | NULL    |       |
+---------------+-------------+------+-----+---------+-------+
9 rows in set (0.00 sec)

mysql> insert into mahasiswa01
    -> (nim, nama, alamat_jalan, kota, kode_pos, no_hp, jenis_kelamin, tgl_lahir, kode_dosen)
    -> values
    -> ("11223344", "Ari Santoso", "", "Bekasi", "", "", "Laki-laki", "19981012", ""),
    -> ("11223345", "Ario Talib", "", "Cikarang", "", "", "Laki-laki", "19991116", ""),
    -> ("11223346", "Dina Marlina", "", "Karawang", "", "", "Perempuan", "19971201", ""),
    -> ("11223347", "Lisa Ayu", "", "Bekasi", "", "", "Perempuan", "19960102", ""),
    -> ("11223348", "Tiara Wahidah", "", "Bekasi", "", "", "Perempuan", "19800205", ""),
    -> ("11223349", "Anton Sinaga", "", "Cikarang", "", "", "Laki-laki", "19880310", "");
Query OK, 6 rows affected (0.06 sec)
Records: 6  Duplicates: 0  Warnings: 0

mysql> select * from mahasiswa01;
+----------+---------------+--------------+----------+----------+-------+---------------+------------+------------+
| nim      | nama          | alamat_jalan | kota     | kode_pos | no_hp | jenis_kelamin | tgl_lahir  | kode_dosen |
+----------+---------------+--------------+----------+----------+-------+---------------+------------+------------+
| 11223344 | Ari Santoso   |              | Bekasi   |          |       | Laki-laki     | 19981012 |            |
| 11223345 | Ario Talib    |              | Cikarang |          |       | Laki-laki     | 19991116 |            |
| 11223346 | Dina Marlina  |              | Karawang |          |       | Perempuan     | 19971201 |            |
| 11223347 | Lisa Ayu      |              | Bekasi   |          |       | Perempuan     | 19960102 |            |
| 11223348 | Tiara Wahidah |              | Bekasi   |          |       | Perempuan     | 19800205 |            |
| 11223349 | Anton Sinaga  |              | Cikarang |          |       | Laki-laki     | 19880310 | 
