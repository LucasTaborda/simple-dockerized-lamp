# LAMP dockerizado

## Instalación:

Clonar proyecto y levantar la imagen.

```
docker compose up -d
```

## Volúmenes

- La carpeta db_data tiene los archivos persistentes de mysql. Este contenido no debería ser manipulado manualmente.
- la carpeta public_html es donde debería ir el index. Es adonde apunta el virtual host de apache.
