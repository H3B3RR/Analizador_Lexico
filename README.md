Proyecto de Analizador Léxico
Asignatura
CL-2024 3- PROGRAMACIÓN DE SISTEMAS DE BASE I - Grupo I - 906531
Integrantes

	Nolasco Ramirez Heber Abdiel
	Gonzalez Morales Victor Eduardo
	Gonzalez Cavazos Erick Alan
	Hernandez Gonzalez Luis Angel


Descripción del Proyecto
Este proyecto consiste en un analizador léxico desarrollado en Java utilizando JFlex. El analizador léxico se encarga de leer un archivo de entrada que contiene código fuente y generar un archivo de salida con los tokens identificados en el código.

Estructura del Proyecto
El proyecto tiene la siguiente estructura de archivos:
entrada.txt
Lexer.class
lexer.flex
Lexer.java
Lexer.java~
Main.class
Main.java
README.md
salida.txt

Archivos y su Función
entrada.txt: Contiene el código fuente que será analizado por el analizador léxico.
Lexer.class: Archivo compilado de la clase Lexer.
lexer.flex: Archivo de especificación de JFlex que define las reglas léxicas.
Lexer.java: Archivo generado por JFlex a partir de lexer.flex, contiene la implementación del analizador léxico.
Lexer.java~: Copia de seguridad del archivo Lexer.java.
Main.class: Archivo compilado de la clase Main.
Main.java: Clase principal que ejecuta el analizador léxico.
README.md: Archivo de documentación del proyecto.
salida.txt: Archivo generado por el analizador léxico que contiene los tokens identificados.
Funcionamiento del Analizador Léxico
El analizador léxico lee el archivo entrada.txt, identifica los diferentes tokens presentes en el código fuente y los escribe en el archivo salida.txt. Los tokens pueden ser palabras clave, identificadores, operadores, delimitadores, literales, números, y texto no reconocido.

Ejecución
Para ejecutar el analizador léxico, se debe compilar y ejecutar la clase Main con los archivos de entrada y salida como argumentos:
    javac Main.java
    java Main entrada.txt salida.txt

Integrantes
[Espacio para los nombres de los integrantes que colaboraron en el proyecto]
Ejemplo de Salida
Dado el archivo de entrada entrada.txt, el archivo de salida salida.txt podría contener:
    PALABRA_CLAVE: function
    IDENTIFICADOR: suma
    TEXTO NO RECONOCIDO: (
    IDENTIFICADOR: a
    TEXTO NO RECONOCIDO: ,
    IDENTIFICADOR: b
    TEXTO NO RECONOCIDO: )
    DELIMITADOR: {
    PALABRA_CLAVE: if
    TEXTO NO RECONOCIDO: (
    IDENTIFICADOR: a
    TEXTO NO RECONOCIDO: >
    IDENTIFICADOR: b
    TEXTO NO RECONOCIDO: )
    DELIMITADOR: {
    PALABRA_CLAVE: return
    IDENTIFICADOR: a
    OPERADOR: -
    IDENTIFICADOR: b
    DELIMITADOR: ;
    DELIMITADOR: }
    PALABRA_CLAVE: else
    DELIMITADOR: {
    PALABRA_CLAVE: return
    IDENTIFICADOR: b
    OPERADOR: -
    IDENTIFICADOR: a
    DELIMITADOR: ;
    DELIMITADOR: }
    DELIMITADOR: }
    ...

Este proyecto es una herramienta útil para el análisis léxico de código fuente, permitiendo identificar y clasificar diferentes componentes del código.
