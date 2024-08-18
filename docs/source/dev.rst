Activación del Proyecto para Desarrollo Local
=============================================

Este documento proporciona instrucciones paso a paso para configurar y ejecutar el proyecto en un entorno de desarrollo local de nuestro Simulador

Requisitos Previos
------------------

Asegúrate de tener instalado lo siguiente en tu sistema:

- Node.js (versión 14.0 o superior)
- npm (normalmente se instala con Node.js)
- Git

Pasos para la Activación
------------------------

1. Clonar el Repositorio
^^^^^^^^^^^^^^^^^^^^^^^^

Primero, clona el repositorio de GitHub a tu máquina local:

.. code-block:: bash

   git clone https://github.com/psychofizz/Uber-sim.git
   cd uber-sim

2. Instalar Dependencias
^^^^^^^^^^^^^^^^^^^^^^^^

Una vez dentro del directorio del proyecto, instala las dependencias necesarias:

.. code-block:: bash

   npm install

3. Configurar Variables de Entorno
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

El proyecto necesita de una API key de google, esta puede ser conseguida en este link
https://developers.google.com/maps/documentation/javascript/get-api-key

.. code-block:: bash

   cp .env.example .env

Una vez obtenia esta llave de google se debe copiar el archivo .env.example
y colocar la API_key en REACT_APP_GOOGLE_API_KEY sin comillas

4. Iniciar el Servidor de Desarrollo
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Para iniciar el servidor de desarrollo de Vite:

.. code-block:: bash

   npm run dev

Esto iniciará el servidor en `http://localhost:5173` (o en otro puerto si el 5173 está ocupado).

5. Compilar para Producción (Opcional)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Si deseas crear una versión de producción:

.. code-block:: bash

   npm run build

Los archivos compilados se generarán en el directorio `dist/`.

Solución de Problemas Comunes
-----------------------------

- **Error de dependencias**: Si encuentras errores relacionados con las dependencias, intenta eliminar el directorio `node_modules` y el archivo `package-lock.json`, luego ejecuta `npm install` nuevamente.

- **Conflictos de versiones**: Asegúrate de que tu versión de Node.js sea compatible con las dependencias del proyecto. Puedes usar nvm (Node Version Manager) para cambiar fácilmente entre versiones de Node.js.

- **Errores de compilación**: Si encuentras errores de TypeScript o ESLint, asegúrate de que tu editor esté configurado correctamente y considera ejecutar `npm run lint` para identificar y corregir problemas de estilo de código.

Contribuciones
--------------

Para contribuir al proyecto:

1. Crea una nueva rama para tu función o corrección.
2. Realiza tus cambios y asegúrate de que todos los tests pasen.
3. Envía un pull request a la rama principal del repositorio.

Recursos Adicionales
--------------------

- Documentación de ViteJS: https://vitejs.dev/guide/
- Documentación de TypeScript: https://www.typescriptlang.org/docs/
- Guía de Tailwind CSS: https://tailwindcss.com/docs


Si no le podes seguir, mira tutoriales de Youtube de como arrancar un proyecto de Vitejs.