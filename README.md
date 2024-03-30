Backlog web
===========

Cliente web para el servidor de backlog, que tendrá soporte principalmente para
dispositivos de escritorio, con un soporte básico para dispositivos móviles (al
menos lectura y alguna operación básica). No se dará soporte completo a móviles
porque eso se hará a través de una aplicación móvil específica.

El cliente puede funcionar con login requerido o sin él, y tiene una sección
que será específica de administradores, en la que se podrá acceder a las funcionalidades
de administrador como crear usuarios (si la auto-creación está desactivada) y listar,
modificar y borrar todos los elementos guardados.

Interfaz
--------

En la interfaz básicamente vamos a incluir las siguientes páginas:

- **Página de login**. Un formulario simple que será la página de inicio si el
servidor tiene activado el modo `login-only`.
- **Página de backlog personal**. En ella se mostrarán los juegos a los que se
está jugando ahora mismo y un resumen de la colección.
- **Página de detalle de ficha personal**. En ella se ven los datos del juego,
sus capturas y una lista de reviews. Así como una línea de tiempo de eventos
de backlog y un formulario para añadir notas a los mismos.
- **Página de detalle de review**. Básicamente una página en la que se pueda
ver el detalle de una review y leerla a gusto, con soporte para modo lectura.
- **Formulario de inclusión de ficha personal**. Debe tener zonas extensibles para
poder añadir también juegos o plataformas que aún no existen en la base de
datos.
- **Formulario de escritura de review**. Un editor simple para poder escribir
una reseña. Se buscará un editor WYSIWYG open source para utilizarlo que
de como resultado un formato markdown, ya que éste será el formato base.
- **Formulario de subida multimedia**. Un formulario simple para subir fotos,
vídeos y música.
- **Página de navegación de colección**. Página en la que se pueda ver una
lista organizada por plataformas de todos los juegos de la colección.
- **Página de administración de objetos de la aplicación** (Sólo admins).
Básicamente sirve para poder adminsitrar todos los objetos guardados en la
base de datos y poder realizar correcciones o limpiezas.

Referencia rápida de desarrollo
-------------------------------

Setup de proyecto:

```sh
npm install
```

Compilar y recargar en caliente para desarrollo:

```sh
npm run dev
```

Comprobar tipos y compilar minificado para producción:

```sh
npm run build
```

Ejecutar pruebas unitarias con Vitest:

```sh
npm run test:unit
```

Hacer el lint con ESLint:

```sh
npm run lint
```
