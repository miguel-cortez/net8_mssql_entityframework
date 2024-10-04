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

