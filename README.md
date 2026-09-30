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
