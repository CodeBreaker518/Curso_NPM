# Dependencias

- Las dependencias de desarrollo son aquellos paquetes que necesitamos en un proyecto mientras estamos desarrollándolo, pero una vez tenemos el código generado del proyecto, no vuelven a hacer falta. Los paquetes instalados con el flag --save-dev o -D se instalan en esta modalidad, guardándolos en la sección devDependences del fichero package.json.

- Por otro lado, las dependencias de producción son aquellos paquetes que necesitamos tener en la web final generada, como librerías Javascript necesarias para su funcionamiento o paquetes similares. Los paquetes instalados con el flag --save-prod, -P o directamente sin ningún flag se instalan en esta modalidad, guardándolos en la sección dependences del fichero package.json.

Veamos un ejemplo de instalación con ambos tipos de paquetes:

```
# Instala en modalidad de desarrollo el paquete "gh-pages"
$ npm install --save-dev gh-pages

+ gh-pages@3.1.0
added 50 packages from 12 contributors and audited 92 packages in 1.998s
```

```
# Instala en modalidad de producción la librería "Howler"
$ npm install howler

+ howler@2.2.0
added 1 package from 1 contributor and audited 93 packages in 1.615s
```

- En el primer caso estamos instalando el paquete gh-pages, una librería y comando CLI para desplegar fácilmente un proyecto en GitHub Pages. Como se trata de un paquete que no es necesario incluir en la web final (se utiliza en desarrollo para desplegar), pues lo instalamos con los flags --save-dev o -D.

- En el segundo caso, estamos instalando el paquete Howler, una librería Javascript que permite manipular y gestionar archivos multimedia de audio desde el navegador. En este caso se trata de una librería JS que si estará incluida en la versión definitiva de la página, por lo que la instalaremos con el flag --save-prod, -P o sin indicar ninguno, ya que es la opción por defecto.
