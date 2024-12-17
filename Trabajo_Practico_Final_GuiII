CREATE database FinalGuiII;
GO
USE FinalGuiII;
GO

CREATE TABLE Transacciones(
Id INT IDENTITY (1,1) PRIMARY KEY,
Nombre NVARCHAR (150) NOT NULL,
Importe DECIMAL (10,2) NOT NULL
);
GO

CREATE PROCEDURE InsertarTransaccion
    @Nombre NVARCHAR(100),
    @Importe DECIMAL(10,2)
AS
BEGIN
    INSERT INTO Transacciones (Nombre, Importe)
    VALUES (@Nombre, @Importe);
END;
GO

CREATE PROCEDURE ActualizarTransaccion
@Id INT,
@Nombre  NVARCHAR (100),
@Importe DECIMAL(10,2)
AS

BEGIN
UPDATE Transacciones
SET 
Nombre = @Nombre,
Importe = @Importe
WHERE Id =  @Id;
END;
GO

CREATE PROCEDURE EliminarTransaccion
@Id INT

AS
BEGIN

DELETE FROM Transacciones
WHERE Id = @Id;
END;
GO


EXEC InsertarTransaccion @Nombre = 'Juan Perez', @Importe = 1500.50;
EXEC InsertarTransaccion @Nombre = 'Charly Garcia', @Importe = 1800.50;
EXEC InsertarTransaccion @Nombre = 'Leon Gieco', @Importe = 1700.50;
EXEC InsertarTransaccion @Nombre = 'Freddy Mercury', @Importe = 1800.60;

EXEC ActualizarTransaccion @Id = 1, @Nombre = 'Joaquin Sabina', @Importe = 2000.75;
EXEC ActualizarTransaccion @Id = 2, @Nombre = 'Mercedes Sosa', @Importe = 5000.65;

EXEC EliminarTransaccion @Id = 1;

SELECT*FROM Transacciones;
