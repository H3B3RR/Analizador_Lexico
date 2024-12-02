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



### Archivos y su Función
- **entrada.txt**: Contiene el código fuente que será analizado por el analizador léxico.
- **Lexer.class**: Archivo compilado de la clase `Lexer`.
- **lexer.flex**: Archivo de especificación de JFlex que define las reglas léxicas.
- **Lexer.java**: Archivo generado por JFlex a partir de `lexer.flex`, contiene la implementación del analizador léxico.
- **Lexer.java~**: Copia de seguridad del archivo `Lexer.java`.
- **Main.class**: Archivo compilado de la clase `Main`.
- **Main.java**: Clase principal que ejecuta el analizador léxico.
- **README.md**: Archivo de documentación del proyecto.
- **salida.txt**: Archivo generado por el analizador léxico que contiene los tokens identificados.

## Funcionamiento del Analizador Léxico
El analizador léxico lee el archivo `entrada.txt`, identifica los diferentes tokens presentes en el código fuente y los escribe en el archivo `salida.txt`. Los tokens pueden ser palabras clave, identificadores, operadores, delimitadores, literales, números, y texto no reconocido.

## Ejecución
Para ejecutar el analizador léxico, se debe compilar y ejecutar la clase `Main` con los archivos de entrada y salida como argumentos:

# Pasos para Generar, Compilar y Ejecutar el Analizador Léxico

## Requisitos Previos
- Tener instalado Java Development Kit (JDK).
- Tener instalado JFlex.

## Generar el Analizador Léxico
1. Crear el archivo `Lexer.flex` con el contenido del analizador léxico.
2. Abrir una terminal y navegar al directorio donde se encuentra `Lexer.flex`.
3. Ejecutar el siguiente comando para generar el analizador léxico:
    ```sh
    jflex Lexer.flex
    ```

## Compilar el Código Java
1. Asegurarse de que los archivos generados (`Lexer.java`) y `Main.java` están en el mismo directorio.
2. En la terminal, navegar al directorio donde se encuentran los archivos `.java`.
3. Ejecutar el siguiente comando para compilar los archivos:
    ```sh
    javac Main.java Lexer.java
    ```

## Ejecutar el Analizador Léxico
1. Crear un archivo de entrada `entrada.txt` con el contenido necesario para el análisis.
2. En la terminal, ejecutar el siguiente comando para ejecutar el programa:
    ```sh
    java Main entrada.txt salida.txt
    ```
3. El resultado del análisis léxico se guardará en el archivo `salida.txt`.


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


