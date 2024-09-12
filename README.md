# tp6-app6


## Organización del repositorio

El repositorio está organizado de la siguiente manera:

```bash
backend/
   ├── app completa
   ├── db.sqlite
   ├── Dockerfile
   └── package.json

frontend/
   ├── app completa
   ├── Dockerfile
   └── package.json

images/
docker-compose.yaml
README.md

```


## Creación de imágenes y `docker-compose.yaml`

Para armar las imágenes y el archivo `docker-compose.yaml`, utilizamos los siguientes recursos:

- Consultamos el material de clase y el prompt para ChatGPT proporcionado en la presentación.
- Realizamos búsquedas en Google para resolver dudas específicas.
- Adaptamos y escribimos desde cero algunas partes según nuestras necesidades.

## Persistencia del servicio tras reinicio del servidor

Configuramos la política de reinicio en el `docker-compose.yaml` utilizando `restart: always`. Esto asegura que los contenedores se reinicien automáticamente si el servidor se reinicia, manteniendo el servicio en funcionamiento.

## Problemas interesantes encontrados

- **Backend:** Tuvimos problemas al construir la imagen porque no se encontraba el `package.json`. Esto se debía a errores en las rutas especificadas en el `Dockerfile` durante el paso de `COPY`. Después de varias pruebas, logramos corregir las rutas y solucionar el problema. Tambien tuvimos problemas porque no se habian subido archivos necesarios para el backend y si bien se buildeaban bien las imagenes, no corria a la hora de entrar al link.
- **Memoria:** Surgió un problema de memoria que se resolvió reiniciando la sesión.
- **Frontend:** Actualmente enfrentamos un problema en el último paso al construir el frontend y estamos trabajando para resolverlo.
- **ChatGPT:** Nos ayudó significativamente a entender la estructura de directorios y la ubicación adecuada de cada archivo.
- **Tiempo:** Tuvimos limitaciones de tiempo debido a otras materias y a la dificultad para solucionar el build del backend.

## Aprendizajes

Aprendimos bastante sobre el propósito y funcionamiento de Docker, y cómo crear y gestionar contenedores de manera efectiva.

