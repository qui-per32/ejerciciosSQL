
Ejercicios SQL
LENGUAJE DDL
1.Crea una base de datos denominada vuelos. Con las siguientes características:

Character set = Latin1
Collate = latin1_spanish_ci

solucion:

create database vuelos Character set latin1 collate latin1_spanish_ci;

2.Renombra la base de datos a viajes.

solucion:

ALTER DATABASE viajes;

3.Crea una tabla denominada clientes que contendrá los siguientes campos:

id
Integer
autoincremental
not_null
primary_key
nombre
varchar(50)
apellidos
varchar(50)
direccion
varchar(150)

solucion:

create table clientes(
	id integer auto_increment not null primary key,
    nombre varchar(50),
    apellidos varchar(50),
    direccion varchar(150)
);


4.Crea una tabla denominada viajes que contendrá los siguientes campos:

id

Integer
autoincremental
not_null
primary_key
titulo

varchar(50)
descripcion

varchar(150)
codigoCliente *Integer *Forgein key clientes(id)


solucion:

create table viajes(
	id integer auto_increment not null primary key,
    titulo varchar(50),
    descripcion varchar(150),
    codigoCliente integer,
    foreign key (codigoCliente) references clientes(id)
);