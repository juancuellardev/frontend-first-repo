# Primer Repositorio Colaborativo

¡Bienvenidos al primer proyecto colaborativo! En este repositorio, aprenderemos a trabajar juntos utilizando Git y GitHub para gestionar versiones de código y colaborar de manera eficiente.

## Tabla de Contenidos

1. [Crear un repositorio remoto](#1-crear-un-repositorio-remoto)
2. [Invitar a colaboradores](#2-invitar-a-colaboradores)
3. [Crear un repositorio local](#3-crear-un-repositorio-local)
4. [Clonar el repositorio](#4-clonar-el-repositorio-remoto)
5. [Trabajo en archivos diferentes](#5-trabajar-en-archivos-diferentes-parte-1)
6. [Modificar archivos existentes](#6-trabajar-en-archivos-diferentes-parte-2)
7. [Trabajar en el mismo archivo](#7-trabajar-en-el-mismo-archivo)
8. [Resolver un conflicto](#8-resolver-un-conflicto)
9. [Ejercitación libre](#9-ejercitación-libre)
10. [Uso de ramas (branches)](#10-crear-y-usar-ramas-branches)
11. [Buenas prácticas colaborativas](#11-buenas-prácticas-colaborativas)

## 1. Crear un repositorio remoto

El participante A deberá crear un nuevo repositorio en [GitHub](https://github.com). **Importante:** El repositorio debe ser creado vacío (sin seleccionar la opción de añadir README.md).

## 2. Invitar a colaboradores

El participante `A` deberá invitar al participante `B` como colaborador del repositorio.
> Si el participante `B` acaba de crear su cuenta de GitHub, puede tardar unos minutos en estar disponible para la invitación.

## 3. Crear un repositorio local

El participante `A` creará un repositorio local en su máquina, lo vinculará con el repositorio remoto, y subirá un archivo `README.md` con el nombre del repositorio.

### Pasos recomendados:

1. Crear el repositorio local:
    ```bash
    git init
    ```
2. Vincular el repositorio remoto:
    ```bash
    git remote add origin https://github.com/usuario/repositorio.git
    ```
3. Crear el archivo README.md:
    ```bash
    echo "# Nombre del Repositorio" > README.md
    git add README.md
    git commit -m "Añadir README.md"
    git branch -M main
    git push origin main
    ```

## 4. Clonar el repositorio remoto

El participante `B` clonará el repositorio remoto:
```bash
git clone https://github.com/juancuellardev/frontend-first-repo.git
```

## 5. Trabajar en archivos diferentes (Parte 1)

Ambos participantes deben crear 3 archivos con nombres diferentes (ej. pikachu.txt). Subirán estos archivos al repositorio remoto y luego descargarán los cambios del otro.

### Pasos:

1. Crear 3 archivos.
2. Agregar contenido y hacer commit:
    ```bash
    git add .
    git commit -m "Agregar archivos"
    ```
3. Sincronizar con el repositorio remoto:
    ```bash
    git push origin main
    ```
4. Cada participante debe actualizar su repositorio local:
    ```bash
    git pull origin main
    ```

## 6. Trabajar en archivos diferentes (Parte 2)

Cada participante modificará uno de los archivos creados previamente y subirá los cambios.

### Pasos:

1. Modificar archivo.
2. Hacer commit y push:
    ```bash
    git add .
    git commit -m "Modificar archivo"
    git push origin main
    ```

## 7. Trabajar en el mismo archivo

Ambos participantes deberán seleccionar el **mismo archivo** y hacer modificaciones en sus respectivas copias locales.

### Pasos:

1. Cada participante debe editar el archivo seleccionado.
2. El primer participante que haga `git push` subirá su versión sin problemas.
3. El segundo participante intentará hacer `git push` y encontrará un conflicto, lo que lleva al siguiente paso.

## 8. Resolver un conflicto

Cuando ambos participantes hayan modificado el mismo archivo, se generará un conflicto que debe resolverse antes de poder fusionar los cambios en el repositorio remoto.

### Resolución de conflicto:

1. Git notificará el conflicto cuando el segundo participante intente hacer `push`.
2. El conflicto puede resolverse de las siguientes maneras:
   - Conservar el contenido del participante A.
   - Conservar el contenido del participante B.
   - Unificar ambos contenidos.
   
3. Después de resolver el conflicto:
   ```bash
   git add archivo_modificado
   git commit -m "Resolver conflicto"
   git push origin main
   ```

## 9. Ejercitación libre

Ahora es su turno de practicar. Creen nuevos archivos, modifiquen los existentes, generen conflictos y resuélvanlos.

## 10. Crear y usar ramas (branches)

Es importante dividir las tareas para evitar conflictos y mantener el trabajo organizado.

### Pasos para trabajar con ramas:

1. Crear una nueva rama:
    ```bash
    git branch nombre_rama
    ```
2. Moverse a la nueva rama:
    ```bash
    git checkout nombre_rama
    ```
3. Hacer cambios y subirlos:
    ```bash
    git add .
    git commit -m "Cambios en nombre_rama"
    git push origin nombre_rama
    ```

## 11. Buenas prácticas colaborativas

- **Commits descriptivos:** Escribe mensajes de commit claros y detallados para que tus colaboradores puedan entender tus cambios fácilmente.
- **Revisiones de código:** Antes de fusionar una rama al main, revisa los cambios de tus compañeros.
- **Resolución de conflictos colaborativa:** Hablen y acuerden cómo resolver los conflictos para que todos estén alineados.
- **Ramas por funcionalidad:** Trabaja en ramas separadas para cada funcionalidad o feature, lo que facilita el seguimiento y la organización.
- **Documentación clara:** Actualiza este README.md y otros documentos relevantes con instrucciones claras para nuevos colaboradores.