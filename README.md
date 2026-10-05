# DAW Project Hub

Pequeña página web para preacticar un flujo profesional de trabajo con Hit y GitHub.

# Historial del Proyecto

Es preferible relaizar commits cada pequeños cambios para poder controlar mejor las
versiones del proyecto. Porque si haces un único commit de todo el proyecto, no puedes
restaurar los cambios en caso de error.

# Conflicto Resuelto

El conflicto se produce cuando intentas fusionar ramas que tienen cambios en las mismas
líneas. En este caso, el conflicto se produjo en index.html. Se resolvió modificando
el eslogan para dejar puestos los de las dos ramas.

# Instrucciones

Para conseguir trabajar con ramas remotas en GitHub, debemos seguir los siguientes
pasos:

1. Ubicarnos dentro del proyecto local. Para ello:
   - Abrimos Git bash
   - Nos ubicamos en la carpeta de nuestro proyecto
2. Ahora, una vez en nuestro proyecto local, procederemos a crear y publicar la nueva
   rama:
   - Escribimos `git switch -c "Nombre-de-la-rama/sub-rama"`. Con este comando, creamos
     la rama y nos ubicamos dentro de la misma.
   - Una vez creada la rama en el entorno local, debemos subirla al repositorio remoto.
     Para ello, ejecutaremos `git push -u origin docs/instrucciones`. El parámetro `-u`
     ayuda a establecer la conexión de la rama local y la rama remota.
3. Ahora, una vez hemos publicado la rama al repositorio remoto, veremos que la rama
   aparece en la sección _"branches"_ de nuestro repo de GitHub. Este aparece justo
   debajo del nombre del proyecto.

# Modificación del README.md desde la interfaz web de HitHub.

# Diferencias entre Fetch y Pull

## Fetch

`git fetch` descargó toda la información, ramas y commits nuevos desde el repositorio
remoto en nuestro repo local, sin modificar nuestro código actual ni alterar nuestro
entorno de trabajo.

## Pull

`git pull` trajo los últimos cambios del repositorio remoto e inmediatamente los integró
con los archivos de nuestra rama local activa.

## ¿Por qué `fetch` permite revisar antes de integrar?

Porque `git fetch` no toca el directorio de trabajo actual. Los cambios descargados se
quedan guardados en referencias remotas (como `origin/main`), lo que nos permite usar
comandos como `git diff` o `git log` para inspeccionar qué cambió antes de decidir si
queremos unir esos cambios a nuestro código.

## ¿Qué relación existe entre `pull`, `fetch` y la integración posterior?

La relación es que **`git pull` es la suma automática de dos pasos**:
`git pull` = `git fetch` + `git merge` (integración)

Cuando hacemos `git fetch`, realizamos solo la primera parte (descargar).La "integración
posterior" ocurre cuando decidimos ejecutar manualmente un `git merge` para aplicar los
cambios descargados. `git pull` simplemente hace ambas tareas en un solo paso.

# Forks y colaboración

## 1. ¿Qué es un fork en GitHub?

Un `Fork` de GitHub es una herramienta que nos permite modificar el repositorio de
alguien, en el que no tenemos permiso de edición. Tambien se puede usar para modificar
de manera local el contenido del repositorio, sin cambiar nada en el mismo. Es como hacer
una copia local para modificar a tu antojo. En caso de que hagamos una buena modificación
del repo, podemos enviar la contribución al dueño del repositorio, y este podrá aceptarla
o negarla.

## 2. ¿En qué se diferencia un fork de una rama?

El `Fork` de un repositorio, descarga todas las ramas del mismo para poder trabajar con
el proyecto entero.
Por otro lado, una `rama` incluye solo las modificaciones realizadas en la misma, sin
posibilidad de hacer cambios en el proyecto general por tu cuenta.

## 3. ¿En qué cuenta se almacena un fork?

Un `Fork` se almacena en la cuenta de GitHub del que lo hace.

## 4. ¿Cuándo resulta útil trabajar mediante un fork?

Trabajar mediante un `fork` resulta útil para contribuir a un proyecto completo por
cuenta propia, sin necesidad de ser colaborador activo del repositorio.

## 5. ¿Qué relación existe entre el repositorio original y el fork?

La relación entre el **repositorio original** y el **fork** se centra en la versión de la
que sale el fork.

## 6. ¿Qué es el repositorio upstream?

El repositorio `upstream` sirve para descargar los últimos cambios del repositorio.
Es la versión del repositorio original modificada por la comunidad.

## 7. ¿Qué diferencia existe entre origin y upstream?

`origin` es la versión 'oficial' del repositorio, donde tú modificas y subes los cambios
realizados.
Por otro lado, `upstream` recopila los cambios de la comunidad realizados sobre el repo
original.

## 8. ¿Cómo se propone que un cambio del fork llegue al repositorio original?

Para proponer subir un cambio al repo original, se realiza un `Pull Request`.

## 9. ¿Quién decide si se acepta la propuesta?

La persona que decide aceptar la propuesta debe ser el **dueño** del repositorio.

## 10. ¿Puede seguir evolucionando el repositorio original mientras existe el fork?

Sí.
