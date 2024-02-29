# Inyección SQL: ¿Qué es y cómo funciona?

La inyección SQL es una vulnerabilidad de seguridad común que afecta a las aplicaciones web que interactúan con bases de datos. Permite a un atacante ejecutar comandos SQL no deseados en una base de datos a través de una entrada de usuario no validada. Esto puede llevar a la revelación de información confidencial, modificación de datos o incluso la eliminación de datos completos.

## Cómo funciona la inyección SQL

La inyección SQL ocurre cuando un usuario malintencionado ingresa datos manipulados en un formulario web u otra interfaz de entrada de datos. Si la aplicación web no valida ni filtra adecuadamente estos datos antes de enviarlos a la base de datos, el atacante puede insertar código SQL malicioso que se ejecutará en el servidor de la base de datos.

## Ejemplos de inyección SQL

### Ejemplo 1: Autenticación de usuario

Supongamos que una aplicación web tiene un formulario de inicio de sesión con los campos "nombre de usuario" y "contraseña". Si la aplicación simplemente concatena estos valores en una consulta SQL para verificar las credenciales del usuario, un atacante puede engañar al sistema ingresando una entrada como esta en el campo de nombre de usuario:

```
' OR '1'='1
```

La consulta resultante sería algo como:

```sql
SELECT * FROM usuarios WHERE nombre_usuario = '' OR '1'='1' AND contraseña = 'contraseña'
```

Esto devuelve verdadero para la condición '1'='1', lo que significa que el atacante puede iniciar sesión sin necesidad de conocer una contraseña válida.

### Ejemplo 2: Extracción de datos confidenciales

Supongamos que una aplicación web tiene una función de búsqueda que permite a los usuarios buscar productos por nombre. Si la consulta SQL no está protegida adecuadamente, un atacante podría utilizar una entrada como esta en el campo de búsqueda:

```
' UNION SELECT nombre, tarjeta_de_credito, 'x', 'x' FROM usuarios --
```

Esto podría manipular la consulta para extraer información sensible de la tabla de usuarios, como nombres y números de tarjetas de crédito, y mostrarlos en los resultados de búsqueda.

### Ejemplo 3: Eliminación de datos

Si una aplicación web permite a los usuarios eliminar elementos de una base de datos sin una protección adecuada, un atacante podría utilizar una entrada maliciosa para eliminar datos importantes. Por ejemplo:

```
'; DROP TABLE usuarios --
```

Esto podría resultar en la eliminación completa de la tabla de usuarios, lo que provocaría la pérdida de todos los datos almacenados en ella.

## Cómo prevenir la inyección SQL

Para prevenir la inyección SQL, es crucial utilizar consultas parametrizadas o preparadas, que separan los datos del código SQL. Además, se deben implementar prácticas de validación y filtrado de datos para asegurarse de que solo se ingresen valores válidos en la base de datos.


