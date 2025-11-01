Proyecto WinFormsProductos (Ejemplo .NET Framework 4.8 + ADO.NET) - Estructura 4 capas

Instrucciones rápidas:
1. Abrir `WinFormsProductos.sln` en Visual Studio 2022.
2. Ajustar cadena de conexión en CapaDatos/Conexion.cs según tu servidor SQL Server.
   Ejemplo: "Server=.\SQLEXPRESS;Database=DBProductos;Trusted_Connection=True;"
3. Crear la base de datos y tabla `Producto` (usa el script SQL incluido más abajo).
4. Compilar y ejecutar (F5).

Script SQL (crear en SQL Server Management Studio):
--------------------------------
CREATE DATABASE DBProductos;
GO
USE DBProductos;
GO
CREATE TABLE Producto (
    IdProducto INT IDENTITY(1,1) PRIMARY KEY,
    Nombre NVARCHAR(100),
    Precio DECIMAL(10,2),
    Stock INT
);
GO
INSERT INTO Producto (Nombre, Precio, Stock)
VALUES ('Mouse', 10.5, 100), ('Teclado', 15.0, 50), ('Monitor', 150.0, 20);
--------------------------------

Nota:
- El proyecto WinForms construye la interfaz por código para evitar dependencias con archivos .Designer.cs generados por versiones diferentes de Visual Studio.
- Si quieres, puedo actualizar para incluir diseñador y recursos o agregar autenticación, logging, validaciones más robustas o manejo de transacciones.
