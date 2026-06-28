# CREADOR DE URL



**1. Crea las carpetas en tu ordenador**



Abre el Explorador de Windows

Ve a Escritorio → GC-PORTAL

Crea una carpeta con el nombre del administrador, por ejemplo admin-martinez

Dentro crea otra con el nombre de la obra, por ejemplo obra-fachada





**2. Copia la plantilla**



Coge el index.html de la raíz de GC-PORTAL

Cópialo y pégalo dentro de la carpeta de la obra





**3. Edita el CONFIG en VS Code**



Abre VS Code

Abre la carpeta GC-PORTAL con File → Open Folder

Navega hasta el index.html de la obra nueva

Usa Ctrl+F y busca CONFIG

Cambia: contraseña, nombre del cliente, título, dirección, fechas, tipo de obra y timeline





**4. Guarda**



Ctrl+S





## SIGUIENTE PASO

OJO COPIAR LINEA POR LINEA



git add .

git commit -m "*poner el cambio que se ha hecho*"

git push



## URL DEL CLIENTE



https://gc-portal-one.vercel.app/NOMBRE CON GUION DE LA ADMI./NOMBRE CON GUION DE LA OBRA



EJEMPLO: https://gc-portal-one.vercel.app/admin-coruna/calle-betanzos



## NUEVO (28/06/2026): login por administradora, no por obra



Desde ahora cada carpeta de administradora (admin-carlos, admin-coruna, admin-zaragoza...) tiene SU PROPIO index.html en la raíz de esa carpeta, con UNA SOLA contraseña para la administradora. Al entrar, la administradora ve una lista de TODAS sus obras y pincha en la que quiere ver.



**URL que se le da ahora a la administradora:**

https://gc-portal-one.vercel.app/NOMBRE CON GUION DE LA ADMI.



EJEMPLO: https://gc-portal-one.vercel.app/admin-carlos



**Cómo añadir una obra nueva a una administradora que ya existe:**

1. Crea la carpeta de la obra dentro de la carpeta de la administradora (como siempre, copiando el index.html de la raíz de GC-PORTAL y editando su CONFIG)

2. Abre el index.html que está en la RAÍZ de la carpeta de la administradora (ej. admin-carlos/index.html)

3. Añade una entrada nueva dentro de CONFIG.obras con: titulo, direccion, estado, y link

4. **IMPORTANTE — el "link" tiene que ser una ruta ABSOLUTA, empezando por "/"** (ej. "/admin-carlos/calle-salamanca/"). Si se pone solo "calle-salamanca/" sin la barra inicial, el botón da error al pinchar porque el navegador interpreta mal la ruta relativa.

5. Guarda y sube los cambios (ver más abajo)



**Importante sobre la contraseña:** ahora vive en el index.html de la administradora (la raíz), no en el de cada obra. El index.html de cada obra sigue teniendo su propio campo "password" por si se accede directamente a esa URL, pero en el flujo normal no se pide otra vez porque la sesión ya queda guardada al entrar por la página de la administradora.



## OJO: este repositorio es "gc-portal", no "claude-workspace"



Este proyecto vive en su PROPIO repositorio de GitHub: `juanbautistagracia-collab/gc-portal` (rama `main`). Es el repositorio al que está conectado Vercel — si subes los cambios a otro repositorio (por ejemplo al workspace general de Claude), Vercel NO se entera y la web no se actualiza, aunque parezca que el "git push" ha funcionado bien. Asegúrate siempre de que la carpeta donde haces `git add / commit / push` es un clon de `gc-portal`, no una copia dentro de otra carpeta.

