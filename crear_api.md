## Proyecto ASP.NET Core Web API 
### Creación de un nuevo proyecto
1. Inicio
2. Visual Studio 2022
3. Crear un proyecto
4. Seleccionar la plantilla ASP.NET Core Web API ![imagen](https://github.com/user-attachments/assets/55518d04-be1d-4077-9b43-c325c38ca8d0)
5. Siguiente
6. Escribir nombre al proyecto
![imagen](https://github.com/user-attachments/assets/5efdf517-2e87-4917-921d-cc843ad1ff3d)
10. Siguiente
11. Crear
![imagen](https://github.com/user-attachments/assets/719e5474-c6ff-4015-a8a5-c297cdc7b086)
El proyecto creado se mostrará como se ve en la siguiente imagen
![imagen](https://github.com/user-attachments/assets/e99b1252-9d5c-41d7-9317-55bb9543d935)

### Instalación de extensiones
#### Proceso
1. Clic derecho en el proyecto
2. Seleccionar la opción Administrar Paquetes NuGet...
#### Lista de paquetes que debe instalar.
1. Microsoft.EntityFrameworkCore
![imagen](https://github.com/user-attachments/assets/06dea038-50c2-40af-8bf2-d425e9ddc5a5)
3. Microsoft.EntityFrameworkCore.SqlServer
![imagen](https://github.com/user-attachments/assets/66ef0bd9-a130-4018-90da-87dbe7153ceb)
4. Microsoft.EntityFrameworkCore.Tools
![imagen](https://github.com/user-attachments/assets/af0228c4-f503-4932-adf1-45bfab985e8a)
### Crear el modelo a partir de una base de datos existente
#### Proceso
1. Asegurarse de tener una base de datos ya creada en Microsoft SQL Server y credenciales para establecer conexión con el servidor.
2. Crear en el proyecto una carpeta llamada **:file_folder:Models**
3. Seleccionar el menú Herramientas > Elegir Administrador de paquetes NuGet > Luego, Consola del Administrador de paquetes
![imagen](https://github.com/user-attachments/assets/e7138d21-1e66-4de8-8065-a052e5ed8b92)
5. Escribir el comando para crear el modelo a partir de la base de datos existente. El comando es el siguiente y solo debe cambiar los parámetros de el nombre del servidor y de base de datos  
`Scaffold-DbContext "Server=SERVIDOR1;Database=BASEDATOS1;Trusted_Connection=True; Trust Server Certificate=true;" Microsoft.EntityFrameworkCore.SqlServer -OutputDir Models -force`  
**Resultado**  
![imagen](https://github.com/user-attachments/assets/4b4770f9-ce76-415f-81dd-58c0359cfe79)
La carpeta **📁 Models** ahora ya dispone de todas las clases que se corresponden con las tablas de la base de datos  
![imagen](https://github.com/user-attachments/assets/1bb6ae44-3147-40a7-9952-43ff4293d033)
### Crear un controlador
1. Haga clic derecho en la carpeta **📁Controllers**
2. Seleccione **Agregar**
3. Haga clic en **Controlador...**
4. Haga clic en **API**
5. Seleccione la opción **Controlador de API con acciones que usan Entity Framework**
6. Seleccione la clase de modelo, la case Db Context y si prefiere, cambie el nombre del controlador.
![imagen](https://github.com/user-attachments/assets/73d59158-87d8-473b-9b87-398ddc605deb)
7. Haga clic en **Agregar**
![imagen](https://github.com/user-attachments/assets/ab78caea-1580-4313-9f80-c7a3b2d09450)
### Pruebe la API
1. Ejecute la aplicación.
![imagen](https://github.com/user-attachments/assets/9bbab468-50cf-4cef-92d2-c9b5fc35b56e)
Si intenta probar un método de la API, va a tener un mensaje como el siguiente
![imagen](https://github.com/user-attachments/assets/5d158fb7-445b-41b3-b95f-227d0d2c28d7)
Para corregir este problema, será necesario hacer algunos cambios en el archivo **appsettings.json** y en la clase **Program**
2. Modificar el archivo **appsettings.json**. Antes de la modificación, el archivo luce así:
  ![imagen](https://github.com/user-attachments/assets/b82c6bbc-078b-4e7a-b5cd-04e3599cb46c)
y después de la modificación:
![imagen](https://github.com/user-attachments/assets/7e46b7ee-c876-4e7d-80d3-db0d4fbbef5f)
4. Modificar la clase **Program**
Antes de la modificación:
![imagen](https://github.com/user-attachments/assets/ed58d5a9-78d5-461a-b4fa-4fd3dcde5ff6)
Después de la modificación:
![imagen](https://github.com/user-attachments/assets/7d800dc8-f4ad-4fc3-a45c-be7115324b45)
5. Pruebe nuevamente la API, ahora ya puede consultar datos provenientes desde la base de datos
![imagen](https://github.com/user-attachments/assets/e76a210b-8c93-4b05-ad3e-56335a9adc2c)
6. Borre el bloque de instrucciones que se muestra en la imagen
![imagen](https://github.com/user-attachments/assets/791c98c6-25ad-48a2-9b79-cdf4448ba1d2)

