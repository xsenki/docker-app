# docker-app

Imagen Docker de la web biblioteca-web (Apache + PHP 8.2) para desplegarla en cualquier servidor con Docker.
Autor/a: Steven Arce · 2º DAW · Despliegue de Aplicaciones Web

## Requisitos

- Docker Engine
- Git

## Estructura

- `apache/Dockerfile`: imagen de la web con Apache, PHP 8.2 y la extensión pdo_mysql.
- `apache/biblioteca-web/`: la web; tiene su propio repositorio, por eso no está aquí y se clona aparte.

## Puesta en marcha

1. Clonar:

```
git clone https://github.com/xsenki/docker-app.git
cd docker-app/apache
git clone https://github.com/AnaFlames/biblioteca-web.git
```

2. Construir y arrancar:

```
docker build -t my-php-image .
docker run -d --name my-php-container -p 8090:80 my-php-image
```

3. Abrir `http://192.168.56.102:8090`.

## Puertos

| Servidor | Contenedor | Servicio |
|----------|------------|----------|
| 8090     | 80         | Apache (web) |

## Pendiente

- La base de datos MySQL: la página Libros todavía no funciona.# docker-app
