# Contenedores

### Crear un contenedor
Para crear un nuevo contenedor Docker a partir de una imagen específica, pero sin iniciarlo automáticamente. 

```
docker create --name <nombre contenedor> <nombre imagen>:<tag>
```
Crear el contenedor  **srv-web** usando la imagen nginx version alpine

![Contenedor creado](./images/image.png)

# COMPLETAR

Si creas un contenedor en Docker sin asignarle un nombre específico utilizando la opción --name, Docker asignará automáticamente un nombre aleatorio al contenedor. Este nombre suele consistir en una combinación de palabras y números.  

Crear el contenedor usando la imagen hello-world

![Contenedor creado sin nombre](./images/image-1.png)

# COMPLETAR

### Listar los contenedores ejecutándose o no

```
docker ps -a
```

![listar contenedores ejecutandose](./images/image-9.png)

### Para iniciar un contenedor

```
docker start <nombre contenedor o identificador>
```
Iniciar el contenedor srv-web 

![iniciar contenedor](./images/image-10.png)

# COMPLETAR

### Listar los contenedores ejecutándose
```
docker ps 
docker ps | grep <nombre contenedor>
```

![listar contenedores ejecutandose](./images/image-11.png)

### Para detener un contenedor

```
docker stop <nombre contenedor>
```

![detener un contenedor](./images/image-12.png)

### Para crear un contenedor y ejecutarlo inmediatamente

```
docker run --name <nombre contenedor> <nombre imagen>:<tag>
```
![Ecosistema de Docker](dockerRun.PNG)

Crear y ejecutar inmediatamente el contenedor **srv-web2** usando la imagen nginx:alpine

![crear y ejecutar contenedor](./images/image-13.png)

# COMPLETAR

**¿Qué sucede luego de la ejecución del comando?**

Se ejecuta el script dentro de la imagen para inicializar el servidor de forma inmediata.

# COMPLETAR  

Cuando ejecutas un contenedor en primer plano sin la opción -d (modo detach), el contenedor captura la entrada estándar (stdin) del terminal, lo que significa que el terminal queda "atrapado" y no puedes introducir más comandos hasta que detengas el contenedor.

### Para crear un contenedor y ejecutarlo inmediatamente sin estar vinculados al mismo
-d: Es la opción que indica a Docker que ejecute el contenedor en segundo plano (en modo "detach").
Cuando un contenedor se ejecuta en segundo plano, Docker devuelve el control al terminal inmediatamente después de iniciar el contenedor, lo que permite al usuario seguir ejecutando otros comandos en el mismo terminal sin que el contenedor detenga la interacción.

```
docker run -d --name <nombre contenedor> <nombre imagen>:tag
```
Crear y ejecutar inmediatamente el contenedor **srv-web3** en modo detach usando la imagen nginx:alpine

![ejecutar el comando](./images/image-14.png)

![contenedor ejecutandose en segundo plano](./images/image-15.png)

# COMPLETAR

### Para eliminar un contenedor

```
docker rm <nombre contenedor>
```
Eliminar el contenedor que se creó a partir de la imagen hello-world 

![eliminar contenedor](./images/image-16.png)

# COMPLETAR

Verificar que el contenedor que se eliminó

![verificacion de eliminacion](./images/image-17.png)

# COMPLETAR

### Para eliminar un contenedor que esté ejecutándose

```
docker rm -f <nombre contenedor>
```
Eliminar el contenedor **srv-web3** 

![eliminar contenedor ejecutandose](./images/image-18.png)

# COMPLETAR

Verificar que el contenedor que se eliminó

![verificacion de eliminacion](./images/image-19.png)

# COMPLETAR

### Para inspecionar un contenedor 

Inspeccionar el contenedor **srv-web**

![inspeccionar contenedor](./images/image-20.png)

# COMPLETAR
