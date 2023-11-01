# LAMP dockerizado

## Versiones del software
- PHP 7.4
- MySQL 5.7

## Requisitos:

Tener docker previamente instalado en el sistema.

## Instalación:

1. Clonar proyecto
```bash
git clone https://github.com/LucasTaborda/simple-dockerized-lamp.git
```
2. Entrar en la carpeta raíz.
```bash
cd simple-dockerized-lamp
```
3. Levantar imagen
```bash
docker compose up -d
```
### Agregar virtual hosts

1. Agrega el archivo .conf en la carpeta ./virtual_hosts y usa el siguiente comando cambiando mi-nuevo-virtualhost.conf por el nombre que corresponda:

```bash
docker exec -it lamp-web-1 a2ensite mi-nuevo-virtualhosts.conf
```
2. Reinicia apache para que tome los cambios.

```bash
docker exec -it lamp-web-1 serviche apache2 restart
```

## Volúmenes

- La carpeta db_data tiene los archivos persistentes de mysql. Este contenido no debería ser manipulado manualmente.
- la carpeta public_html es donde debería ir el index. Es adonde apunta el virtual host de apache.
