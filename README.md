# IONIC FACEBOOK CLONE

### COMANDOS:
1. Descarga la imagen de Docker de Ionic 5:
```
docker pull chiticariu/ionic5
```

2. Construye la imagen de Docker desde el directorio raíz del proyecto:
```
docker build -t nombre_de_imagen .
```
> _Reemplaza ```nombre_de_imagen``` con el nombre que desees asignarle a tu imagen de Docker._

3. Una vez que la imagen de Docker se haya construido, ejecuta el proyecto en un contenedor Docker:

```
docker run -p 8100:8100 nombre_de_imagen
```

> _Reemplaza ```nombre_de_imagen``` con el nombre que le hayas asignado a tu imagen de Docker._

Ahora puedes acceder a la aplicación Ionic en tu navegador web visitando http://localhost:8100.

---

### ADICIONAL:
Si el puerto local está ocupado por otro proceso, puedes asignar un puerto diferente al contenedor Docker.

Modifica el comando docker run para especificar el mapeo del puerto local al puerto del contenedor. Por ejemplo:
```
docker run -p 8101:8100 nombre_de_imagen
```
> _Aquí, el número antes de : representa el puerto local que deseas utilizar (8101 en este ejemplo), y el número después de : representa el puerto del contenedor que está expuesto (8100 en este caso)._
