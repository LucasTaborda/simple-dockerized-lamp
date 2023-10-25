# LAMP dockerizado

## Versiones del softwware
- PHP 7.4
- MySQL 5.7

## Requisitos:

Tener docker previamente instalado en el sistema.

## Instalación:

1. Clonar proyecto
```
git clone https://github.com/LucasTaborda/simple-dockerized-lamp.git
```
2. Entrar en la carpeta raíz.
```
cd simple-dockerized-lamp
```
3. Levantar imagen
```
docker compose up -d
```

## Volúmenes

- La carpeta db_data tiene los archivos persistentes de mysql. Este contenido no debería ser manipulado manualmente.
- la carpeta public_html es donde debería ir el index. Es adonde apunta el virtual host de apache.
