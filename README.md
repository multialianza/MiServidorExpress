# MiServidorExpress
🛠️ E2-M6 Ejercicio
Estructura Profesional de un Proyecto Node.js 🏗️
Objetivo: Aprender el flujo de trabajo estándar para iniciar un proyecto en Node.js, incluyendo la gestión de paquetes con NPM y la creación de un servidor web básico utilizando Express, el framework más popular para el desarrollo de aplicaciones web con Node.

Instrucciones:

Paso 1: Preparación del Entorno
Crea una nueva carpeta en tu computadora para este proyecto (ej: mi-servidor-express).

Abre tu terminal y navega dentro de esa carpeta. Todos los comandos siguientes se ejecutarán desde allí.

Paso 2: Inicialización del Proyecto con NPM
El package.json es el acta de nacimiento de tu proyecto. Contiene metadatos y gestiona las dependencias.

En tu terminal, ejecuta el siguiente comando para crear un archivo package.json con valores por defecto:

 
npm init -y

Paso 3: Instalación de Dependencias
Ahora instalaremos los paquetes que necesitamos: Express para construir el servidor y Nodemon como una herramienta de desarrollo que reiniciará el servidor automáticamente cada vez que guardes un cambio.

Instala Express como una dependencia de producción:

 
npm install express

Instala Nodemon como una dependencia de desarrollo (solo la usaremos mientras programamos):

 
npm install nodemon --save-dev

Ahora, si revisas tu package.json, verás estas librerías listadas en dependencies y devDependencies.

Paso 4: Creación del Script de Ejecución
Para facilitar la ejecución de nuestro servidor, crearemos un script personalizado en package.json.

Abre el archivo package.json en tu editor de código.

Busca la sección "scripts".

Añade un nuevo script llamado "start" que utilice Nodemon para ejecutar tu archivo principal (que llamaremos app.js). La sección de scripts debería quedar así:

 
"scripts": {
  "start": "nodemon app.js"
},

Paso 5: Creación del Servidor Básico con Express
Ahora, vamos a escribir el código del servidor.

Crea un archivo llamado app.js en la raíz de tu proyecto.

Escribe el siguiente código, siguiendo la estructura básica de una aplicación Express:

Importa la librería Express.

Crea una instancia de la aplicación Express.

Define un puerto para el servidor (ej: 3000).

Define una ruta para la raíz (/) que responda a peticiones GET. Cuando se acceda a esta ruta, debe enviar una respuesta simple como '¡Hola Mundo con Express!'.

Inicia el servidor para que comience a escuchar peticiones en el puerto que definiste, mostrando un mensaje en la consola para confirmar que está funcionando.

Paso 6: Ejecución y Verificación
En tu terminal, en lugar de usar node app.js, ejecuta el script que creaste:

 
npm start

Verás el mensaje de confirmación en tu consola.

Abre tu navegador y visita http://localhost:3000. Deberías ver tu mensaje.

Prueba Nodemon: Vuelve a app.js, cambia el mensaje de respuesta, y guarda el archivo. Verás que tu terminal reinicia el servidor automáticamente. Refresca el navegador para ver el cambio.

Conceptos a Aplicar:

NPM (Node Package Manager): El gestor de paquetes de Node.js.

npm init: Para inicializar un proyecto.

npm install: Para instalar paquetes/dependencias.

package.json: El archivo de manifiesto del proyecto que define sus propiedades, scripts y dependencias.

Scripts de NPM: Comandos personalizados (como npm start) para automatizar tareas.

Express.js: El framework para construir aplicaciones web.

require('express'): Importación del módulo.

express(): Creación de la instancia de la aplicación.

app.get(): Definición de una ruta para peticiones GET.

app.listen(): Método para iniciar el servidor.

Dependencias de Desarrollo: Paquetes que solo se usan durante el desarrollo (--save-dev).

Entrega:

El trabajo deberá ser entregado a través de un repositorio público en GitHub. Asegúrate de incluir un archivo .gitignore para no subir la carpeta node_modules. Por favor, comparte únicamente el enlace a dicho repositorio. 📤
