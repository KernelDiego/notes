# Permisos en el comando `chmod`

## Tabla en base octal para los permisos

Los permisos se pueden indicar de dos maneras, por medio de una sintaxis en números octales (base 8) o por medio de caracteres. Explicaremos la base octal, que puede resultar un poco más compleja, pero que resulta más abreviada y universal. En base octal los permisos se expresan con tres dígitos, del 0 al 7.

El primer dígito corresponde a los permisos del `usuario`, el segundo a los del `grupo` y el tercero a los del `resto de usuarios`. Por ejemplo, posibles valores de permisos podrían ser 000, 644, 755, 777, etc.



| Numero | Binario | Lectura (r) | Escritura (w) | Ejecucion (x) |
| -------|---------|-------------|---------------|---------------|
| 0      | 000     | ❌          | ❌           | ❌           |
| 1      | 001     | ❌          | ❌           | ✔️           |
| 2      | 010     | ❌          | ✔️           | ❌           |
| 3      | 011     | ❌          | ✔️           | ✔️           |
| 4      | 100     | ✔️          | ❌           | ❌           |
| 5      | 101     | ✔️          | ❌           | ✔️           |
| 6      | 110     | ✔️          | ✔️           | ❌           |
| 7      | 111     | ✔️          | ✔️           | ✔️           |


Así, 0 significa que no hay ningún permiso y 7 que los tiene todos. Ahora, el permiso 000 significa que nadie tiene permiso para hacer nada con el fichero. 777 significa que todo el mundo tiene permisos para hacer cualquier cosa. 700 significa que existen permisos totales para el dueño del archivo, pero no para el resto de los usuarios. Un ejemplo completo de comando sería el siguiente:

```console
chmod 764 archivo.txt
```

Esto indica que el usuario dueño tendrá permisos totales sobre el fichero archivo.txt. El grupo tiene permiso de lectura y escritura (pero no de ejecución) y el resto de usuarios solo tienen permiso de lectura. Como modificadores u opciones del comando encontramos una muy útil, que sirve para gestionar los permisos de manera recursiva, en todas las carpetas y subcarpetas de un directorio.

```console
chmod -R 764 carpeta
```
