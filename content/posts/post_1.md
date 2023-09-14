---
title: "Git: Básico"
date: 2023-09-14
description: 'Git básico para principiantes.'
---

## ¿Qué es Git?

Git es una herramienta que te ayuda a llevar un registro de los cambios que haces en tus archivos. Es como una especie de "historial" que puedes usar para trabajar en proyectos o guardar tus trabajos personales.

## Pasos Básicos de Git

### 1. Instala Git

El primer paso es obtener Git en tu computadora. Hazlo así:
> - Ve a [este enlace](https://git-scm.com/downloads).
> - Descarga Git para tu sistema operativo (Windows, macOS o Linux).
> - Sigue las instrucciones para instalarlo.

### 2. Configura tu Nombre y Correo

Git necesita saber quién eres para saber quién hizo cada cambio. Configura tu nombre y correo electrónico con estos comandos:

```
git config --global user.name "Tu Nombre"
git config --global user.email "tu@email.com"
```
### 3. Crea un Nuevo Proyecto
Piensa en un proyecto que quieras hacer y crea una carpeta para él en tu computadora. Por ejemplo, podrías llamarla "Mi Proyecto".

### 4. Inicia un Repositorio Git
Abre una ventana de comandos o terminal en tu computadora. Luego, dentro de la carpeta de tu proyecto, ejecuta este comando:
```
git init

```
Esto crea un lugar especial llamado "repositorio" donde Git guardará tus cambios.

### 5. Agrega Archivos al Repositorio

Hasta este punto, Git sabe que tienes un proyecto, pero aún no está rastreando ningún archivo en él. Necesitas decirle a Git qué archivos quieres que siga. Aquí tienes cómo hacerlo:

#### a. Añadir un archivo específico:

Si deseas rastrear un archivo específico, usa el siguiente comando, reemplazando "nombre-del-archivo" con el nombre real de tu archivo:

```
git add nombre-del-archivo

```

Por ejemplo, si tienes un archivo llamado "mi-archivo.txt", usarías:

```
git add mi-archivo.txt

```
#### b. Añadir todos los archivos:
Si prefieres rastrear todos los archivos en tu proyecto, puedes usar el comando siguiente para agregar todos los cambios:
```
git add .

```
Este punto (.) significa "todos los archivos" en la carpeta actual. Ten cuidado con este comando, ya que agregará todos los cambios, ¡incluso los que no desees rastrear!

#### c. Comprobar el Estado de los Archivos:
Puedes usar el siguiente comando para ver el estado de tus archivos y cómo Git los está gestionando:
```
git status

```

Este comando te mostrará una lista de archivos que han sido modificados, agregados o eliminados desde el último commit. Es útil para saber qué archivos están listos para ser commitidos.

#### d. Deshacer Cambios en un Archivo:
Si cometes un error o deseas deshacer los cambios en un archivo antes de hacer un commit, puedes utilizar el siguiente comando:
```
git restore nombre-del-archivo

```
Este comando deshace los cambios en el archivo y lo restaura a su estado anterior a la última confirmación.
### 6. Haz un Commit
Ahora que le has dicho a Git qué archivos seguir, es hora de guardar esos cambios en un "commit". Un commit es como un punto de control o una captura de pantalla de tu proyecto en ese momento. Aquí está cómo hacerlo:

a. Hacer un Commit Básico:
Usa el siguiente comando para hacer un commit básico con un mensaje que describa los cambios que hiciste:
```
git commit -m "Descripción de los cambios que hiciste"

```

Por ejemplo:
```
git commit -m "Agregué información de contacto a mi sitio web"

```
#### b. Detalles Adicionales en el Commit:
Puedes agregar más detalles a tu commit si es necesario. Para ello, simplemente omite el -m y Git abrirá un editor de texto donde puedes escribir una descripción más larga de tus cambios.

```
git commit

```
Esto abrirá el editor de texto configurado en tu sistema y podrás escribir una descripción detallada de tus cambios.

### 7. Revisa tu Historial
Una vez que hayas hecho algunos commits, puedes ver una lista de tus cambios anteriores. Esto puede ser útil para recordar lo que has hecho o para volver a versiones anteriores si algo sale mal. Usa este comando para ver tu historial de commits:

```
git log

```
El comando git log mostrará una lista de commits con detalles como el autor, la fecha y el mensaje de cada commit.

### 8. Trabaja con Ramas (Opcional)
Si tu proyecto se vuelve más grande y complejo, puedes usar "ramas" para organizar tu trabajo. Las ramas te permiten trabajar en diferentes partes de tu proyecto sin afectar el trabajo principal. Aquí te mostramos cómo crear y cambiar entre ramas:

#### a. Crear una Rama:
Utiliza este comando para crear una nueva rama con un nombre descriptivo:
```
git branch nombre-de-la-rama

```

#### b. Cambiar a una Rama:
Puedes cambiar a una rama existente con el siguiente comando:
```
git checkout nombre-de-la-rama

```
### 9. Guarda tus Cambios en un Repositorio Remoto (Opcional)
Si trabajas con otras personas o deseas tener una copia de seguridad en línea de tu proyecto, puedes utilizar un servicio en línea como GitHub o GitLab para guardar tus cambios. Esto te permite colaborar en proyectos y tener una copia segura de tu trabajo.

Espero que estos detalles adicionales te ayuden a comprender mejor Git. Si tienes más preguntas o necesitas más explicaciones, no dudes en preguntar.

### 10. Colaborar con Otros (Opcional)
Si estás trabajando en un proyecto con otras personas, Git te permite colaborar de manera efectiva. Aquí hay más información sobre cómo colaborar:

#### a. Clonar un Repositorio Existente:
Si alguien más ya ha creado un repositorio en línea, puedes copiarlo en tu computadora usando el siguiente comando:
```
git clone URL-del-repositorio

```
Esto crea una copia local de todo el proyecto en tu computadora, para que puedas trabajar en él.

#### b. Enviar Cambios a un Repositorio Remoto:
Cuando quieras compartir tus cambios con otros o guardar una copia de seguridad en línea, puedes enviar tus commits a un repositorio en línea usando estos comandos:

```
git remote add origin URL-del-repositorio
git branch -M main
git push -u origin main

```

Estos comandos configuran tu repositorio local para colaborar con un repositorio en línea, como GitHub.

### 11. Resolución de Conflictos (Opcional)
A veces, cuando varias personas trabajan en el mismo proyecto, pueden ocurrir conflictos. Esto sucede cuando dos personas hacen cambios en la misma parte de un archivo. Git te permite resolver estos conflictos. Aquí está cómo:

#### a. Obtener los Cambios más Recientes:
Antes de resolver un conflicto, es importante asegurarse de que tienes los cambios más recientes del repositorio en línea. Usa el siguiente comando para obtener los cambios:

```
git pull origin main

```
#### b. Resolver Conflictos:
Cuando Git detecta un conflicto, marcará las áreas en conflicto en tus archivos. Deberás editar esos archivos para resolver los conflictos manualmente.

<font style="color: red; font-size: 18px;">¡Atención Importante!</font>

Si estás trabajando en un proyecto con un equipo, asegúrate siempre de hacer un "pull" al comienzo de tu sesión de trabajo. Un "pull" obtiene los cambios más recientes del proyecto desde el repositorio en línea y los actualiza en tu computadora. Esto es esencial para mantener tus archivos actualizados y evitar conflictos con los cambios de tus compañeros de equipo.

Para hacer un "pull", puedes usar el siguiente comando:

```
git pull origin nombre-de-la-rama-o-main

```

Reemplaza "nombre-de-la-rama-o-main" con el nombre correcto de la rama en la que estás trabajando. Hacer esto al principio de tu día de trabajo te ayudará a estar al día y a trabajar de manera más efectiva con tu equipo.
