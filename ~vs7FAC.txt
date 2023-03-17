CREATE DATABASE UC12SA3

USE UC12SA3

CREATE TABLE Usuarios
	(
	UsuarioId INT PRIMARY KEY IDENTITY,
	Email VARCHAR(100) UNIQUE NOT NULL,
	Senha VARCHAR(50) NOT NULL
	)

INSERT INTO Usuarios VALUES ('email@email.com', 1234)

SELECT * FROM Usuarios

INSERT INTO Usuarios VALUES ('outroemail@email.com', 4321)

SELECT UsuarioId, Email, HASHBYTES('MD2', Senha) FROM Usuarios
SELECT UsuarioId, Email, HASHBYTES('MD4', Senha) FROM Usuarios
SELECT UsuarioId, Email, HASHBYTES('MD5', Senha) FROM Usuarios
SELECT UsuarioId, Email, HASHBYTES('SHA', Senha) FROM Usuarios
SELECT UsuarioId, Email, HASHBYTES('SHA2_256', Senha) FROM Usuarios
SELECT UsuarioId, Email, HASHBYTES('SHA2_512', Senha) FROM Usuarios