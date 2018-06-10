# Archetype Maven
Hay dos formas para crear una plantilla para un proyecto con Maven.
1.	A partir de un proyecto existente.
2.	Desde cero por l�nea de comandos.

## A partir de un proyecto existente
Dentro de la carpteta de un proyecto, utilizar plugin:

```
archetype:create-from-project
```
Copiar en nuevo directorio la carpeta:
target/generated-sources/archetype

Tenemos la siguiente estructura:
* /src
* /target
* pom.xml

Limpiar /target con:

```
mvn clean
```

Dentro de src/main/resources hay dos ficheros:
1.	Achetype-resources: plantilla del proyecto.
2.	META-INF/maven: contiene archetype-metadata.xml con la configuraci�n y opciones al generar un nuevo proyecto.

Cuando todo est� personalizado:

```
mvn install
```

Ahora tenemos disponible en nuestro cat�logo archetype de Maven.

## Desde cero por l�nea de comandos
Generar plantilla b�sica:

```shell
mvn archetype:generate -B -DarchetypeArtifactId=maven-archetype-archetype -DgroupId=com.package -DartifactId=artifactTemplate -Dversion=0.0.1-SNAPSHOT -Dpackage=package
```
