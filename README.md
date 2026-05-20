# LabCrud
# Laboratorio - Uso de CRUD con Laravel

**Universidad Tecnológica de Panamá**  
**Facultad de Ingeniería de Sistemas Computacionales**  
**Departamento de Programación de Computadoras**

| | |
|---|---|
| **Asignatura** | Desarrollo de Software VII |
| **Tema** | CRUD y Laravel |
| **Semestre** | I Semestre |
| **Grupo** | 1GS132 |
| **Estudiante** | Carlos Abadía - 4-823-2233 |
| **Correo** | carlos.abadia1@utp.ac.pa |
| **Facilitador** | Irina Fong |

---

## Introducción

En este laboratorio se implementó un sistema CRUD (Create, Read, Update, Delete) utilizando el framework Laravel bajo el patrón de arquitectura Modelo-Vista-Controlador (MVC). El objetivo principal fue comprender cómo Laravel organiza y gestiona las operaciones básicas sobre una base de datos, en este caso sobre una tabla de productos, utilizando herramientas propias del framework como Eloquent ORM para la interacción con la base de datos, las migraciones para el control de la estructura de las tablas, y las vistas Blade para la presentación de la información al usuario. Adicionalmente se aplicaron estilos personalizados mediante Bootstrap y CSS para mejorar la experiencia visual de la aplicación.

---

<img width="1918" height="410" alt="image" src="https://github.com/user-attachments/assets/fc590f05-8aa0-4331-afed-7b8e5bc99775" />

Muestra de la creación de un producto.


<img width="1908" height="651" alt="image" src="https://github.com/user-attachments/assets/89c0f8bc-99fe-450d-ab39-872330080b99" />

Formulario para crearlos.

---

## Conclusiones Técnicas

1. Separación de responsabilidades con MVC

La implementación del CRUD en Laravel demostró en la práctica cómo el patrón MVC distribuye claramente las responsabilidades del sistema. El modelo Product gestionó exclusivamente la interacción con la base de datos mediante Eloquent, el controlador ProductController concentró toda la lógica de negocio para las operaciones crear, leer, actualizar y eliminar, mientras que las vistas Blade se encargaron únicamente de presentar la información al usuario. Esta separación facilita el mantenimiento del código, ya que cualquier cambio en la base de datos no afecta directamente a las vistas y viceversa.

2. Migraciones como control de versiones de la base de datos

El uso de migraciones para definir la estructura de la tabla products demostró ser una práctica superior a la creación manual de tablas en phpMyAdmin. Al definir los campos name, description, price y quantity directamente en código PHP, se garantiza que cualquier miembro del equipo pueda reproducir exactamente la misma estructura de base de datos ejecutando un solo comando, eliminando inconsistencias entre entornos de desarrollo y producción.

3. Generación automática de código con herramientas Artisan

El uso del paquete ibex/crud-generator junto con los comandos Artisan permitió generar automáticamente el controlador, modelo, vistas y rutas del CRUD en segundos. Sin embargo, se observó que el código generado automáticamente requiere ajustes manuales, como agregar los campos al $fillable del modelo, completar las vistas vacías y configurar las reglas de validación en el ProductRequest. Esto evidencia que las herramientas de scaffolding aceleran el desarrollo pero no reemplazan la comprensión de la arquitectura subyacente.
