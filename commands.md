## Inicializar un proyecto

- `npm init`: Inicializa un proyecto. Luego tienes que responder preguntas básicas del proyecto
- `npm init -y`: Inicializa un proyecto con una descripción por defecto de las preguntas bases

## Instalando dependencias

- `npm install`: Instala las dependencias escritas del `package.json`
- `npm install package-name`: Instala el paquete de nombre __package-name__ y lo guarda como dependencia para producción
- `npm install package-name --save-dev`: Instala el paquete y lo guarda como dependencia de desarrollo
- `npm install package-name@version`: Instala una versión específica del paquete
- `npm install package-name@latest`: Instala una versión más reciente del paquete
- `npm install pacakge-name -g`: Instala el paquete de forma global
- `npm uninstall package-name`: Con eso elimina la dependencia y los paquetes de los cuales depend

## Listando dependencias

- `npm list`: Lista los paquetes instalados en el proyecto
- `npm list -g`: Lista los paquetes instalados de forma global
- `npm outdate`: Nos permite mostrar los paquetes que estan desactualizados

## Auditando y corrigiendo vulneravilidades

- `npm audit`: Audita las dependencias que tenemos instaladas en busca de vulnerabilidades
- `npm audit fix`: Audita e intenta arreglar las vulnerabilidades de nuestras dependencias
- `npm audit --json`: Muestra los resultados de la auditoría a manera más profunda en formato json
- `npm audit fix --force`: Corrige los problemas encontrados en las librerías instalando otras dependencias por debajo si es necesario

## Build de los proyectos

- `npm run build --dd`: Activa el build en formato verbose. Lo cual entrega una información más robusta de lo que se creó en el build
- `npm ci`: también llamado `npm clean install`. Este comando es similar al comando `npm install`. Con la diferencia que está pensado para ser utilizado en ambientes automatizados.

## Publicar un paquete a npm

- `npm link`: Crea un enlace simbólico para reconocer este paquete dentro del estado de paquete que contiene npm, pero sin publicarlo. De esta forma se puede probar el paquete y garantizar que cumple con lo que se programó
- `npm adduser`: Inicia sesión en npm desde la terminal
- `npm publis`: Publica el proyecto creado
- `npm version x.x.x`: Cambia la version del proyecto a x.x.x