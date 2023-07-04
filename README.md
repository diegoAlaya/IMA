# Instrucciones de ejecución ambiente local IMA+07

1. Clonar los repositorios:

-   _rest-train_ (rama main)
-   _rest-admin_ (rama main)
-   _rest-collections_ (rama main)
-   _rest-arquitectures_ (rama main)
-   _rest-predictions_ (rama main)
-   _Core_ (rama acumulado)
-   _ima-front_ (rama master).

2. Dejar los repositorios en una misma carpeta, de la siguiente forma:

```
folder/
├── rest-admin/
├── rest-train/
├── rest-collections
├── rest-arquitectures
├── Core
├── Ima-front
```

3. Mover el archivo _docker-compose.yml_ en la raíz de la carpeta Core (_rama acumulado_) en la misma carpeta que los repositorios, de la siguiente forma:

```
folder/
├── rest-admin/
├── rest-train/
├── rest-collections
├── rest-arquitectures
├── Core
├── Ima-front
├── docker-compose.yml
```

4. Tener instalado y configurado Docker (Docker Desktop en Windows).
5. Ejecutar el comando

```
docker-compose up
```

6. Descargar backup de la DB

    - [Google-Drive-link](https://drive.google.com/drive/folders/1Akn5rsF60Y_ZtA2dypwyD3464ncfqMbY?usp=sharing)

7. Ejecutar el comando de dokcer, para extraer la ID del container de _postgres_
  - De esto solo es necesario copiar los dos primeros caracteres del ID 
 

```
docker ps -a
```

7. Inicializamos la base de datos con el archivo _nnmanager-bd.pgsql_ desde la ubicación del archivos, hacemos el comando reemplazando _ID_IMAGEN_POSTGRES_ por los caracteres del ID:

```
sudo docker exec -i ID_IMAGEN_POSTGRES psql -U nnmanager nnmanager < nnmanager-bd.pgsql
```

## SHELL PSQL

Lista base de datos:

```
\l
```

Entrar a base de datos:

```
psql -U nnmanager -d NOMBRE_BASE_DATOS
```

Conectar a otra base de datos:

```
\c NOMBRE_BASE_DATOS
```

Listar tablas:

```
\dt
```

Listar tablas:

```
\dt
```

QUery ejemplo:
```
SELECT * FROM usuarios;
```
