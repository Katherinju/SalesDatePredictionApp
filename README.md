# 📊 Sales Date Prediction - Prueba Técnica

Este repositorio contiene la solución completa. El objetivo del proyecto es permitir la creación de órdenes y la predicción de la fecha estimada de la siguiente orden por cliente, además de visualización de datos mediante D3.js.

---

## 🧩 Estructura del Proyecto

- **Backend**: Web API .NET Core
- **Frontend SPA**: Angular 17+
- **Gráfica D3.js**: Vanilla JS con D3.js
- **Base de Datos**: SQL Server

---

## ⚙️ Requisitos Previos

- [.NET SDK](https://dotnet.microsoft.com/) (.NET 6 o superior)
- [Node.js + Angular CLI](https://angular.io/guide/setup-local)
- [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)
- Un editor como VSCode o Visual Studio 2022+

---

## 🚀 Instrucciones para ejecutar el proyecto

### 🗄️ 1. Base de Datos

1. Asegúrate de tener una instancia activa de SQL Server.
2. Ejecuta el script `DBSetup.sql` (provisto) para crear la base de datos `StoreSample` y poblarla con datos de prueba.

### 🔙 2. Web API (.NET)

```bash
cd SalesDatePrediction.API
dotnet restore
dotnet build
dotnet run

La API quedará disponible en https://localhost:7229 (u otro puerto que configure tu entorno).

Endpoints expuestos:

GET /api/customers/with-order-info

GET /api/orders/by-customer/{id}

GET /api/employees

GET /api/shippers

GET /api/products

POST /api/orders

🖥️ 3. Web App (Angular)
```bash
cd SalesDatePrediction.WebApp
npm install
ng serve
La aplicación SPA estará disponible en http://localhost:4200.

📉 4. Gráfica con D3.js
Abre el archivo grafico-d3/index.html en el navegador.

Ingresa números enteros separados por coma y presiona "Update Data" para ver el gráfico generado dinámicamente.

💡 Consideraciones y decisiones tomadas
Aplicación de principios SOLID en la arquitectura de la API.

Se incluyó paginación y ordenamiento en las tablas de la SPA usando Angular Material.

Filtrado por nombre de cliente implementado desde el servidor, como se pidió.

La vista de predicción de órdenes se configuró como la vista principal de la SPA.

Se aplicaron buenas prácticas en el uso de D3.js, como validación de datos, limpieza previa del SVG y asignación controlada de colores.

Las pruebas unitarias se implementaron con xUnit para los servicios de negocio.

🧪 Pruebas
Las pruebas unitarias están en la carpeta SalesDatePrediction.Tests. Para ejecutarlas:

dotnet test
