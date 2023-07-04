Instrucciones de ejecución ambiente local IMA+07
Clonar los repositorios:
rest-train (rama main)
rest-admin (rama main)
rest-collections (rama main)
rest-arquitectures (rama main)
rest-predictions (rama main)
Core (rama acumulado)
ima-front (rama master).
Dejar los repositorios en una misma carpeta, de la siguiente forma:
folder/
├── rest-admin/
├── rest-train/
├── rest-collections
├── rest-arquitectures
├── Core
├── Ima-front
Mover el archivo docker-compose.yml en la raíz de la carpeta Core (rama acumulado) en la misma carpeta que los repositorios, de la siguiente forma:
folder/
├── rest-admin/
├── rest-train/
├── rest-collections
├── rest-arquitectures
├── Core
├── Ima-front
├── docker-compose.yml
Tener instalado y configurado Docker (Docker Desktop en Windows).
Ejecutar el comando
docker-compose up
Descargar backup de la DB

Google-Drive-link
Ejecutar el comando de dokcer, para extraer la ID del container de postgres

docker ps -a
Inicializamos la base de datos con el archivo nnmanager-bd.pgsql desde la ubicación del archivos, hacemos el comando:
sudo docker exec -i ID_IMAGEN_POSTGRES psql -U nnmanager nnmanager < nnmanager-bd.pgsql
SHELL PSQL
Lista base de datos:

\l
Entrar a base de datos:

psql -U nnmanager -d NOMBRE_BASE_DATOS
Conectar a otra base de datos:

\c NOMBRE_BASE_DATOS
Listar tablas:

\dt
Listar tablas:

\dt
QUery ejemplo:

SELECT * FROM usuarios;
