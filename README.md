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
