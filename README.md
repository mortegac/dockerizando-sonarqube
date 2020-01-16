

http://localhost/projects
USER: admin 
PASS: bitnami

##Paper
https://medium.com/@slryit/sonarqube-and-reactjs-the-right-way-5979d02c080d

##Configurar escáner SonarQube
Manejo del escáner SonarQube
La mayoría de los proyectos requieren el escáner SonarQube ( enlace Wiki para análisis de Javascript. Descárguelo en algún lugar de su disco y descomprímalo).
Crea un archivo `sonar-project.properties` en su proyecto.
Copie y pegue este contenido y modifíquelo:
```
sonar.projectKey = sleroy: reactjs-demo
sonar.projectName = ReactJS demo
sonar.sourceEncoding = UTF-8
sonar.javascript.file.suffixes = .js, .jsx
```

No olvide la línea sonar.javascript.file.suffixes=.js,.jsx, ¡es el truco para hacer que SonarQube funcione en archivos JSX !


##Configurar ESLint en tu proyecto
Queremos realizar el análisis de SonarQube con los resultados adicionales de ESLint. Eslint es una impresora popular que proporciona reglas recientes para muchos marcos de trabajo de javascript, incluido ReactJS.
Por lo tanto, ESLint a menudo se actualiza y contiene a través de su sistema de extensión, reglas y marcos que no encontrará en la instalación regular de SonarQube.
Si aún no ha creado un archivo de configuración de ESLint, aquí están los comandos:

``` eslint --init```

##Probar ESLint en el proyecto

```eslint```


##Agregar extension  de React a ESLint en el proyecto
```npm i eslint-plugin-react@latest --save-dev```


##Ejecutar onarQube Scanner
~/tools/sscanner/bin/sonar-scanner