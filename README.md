# 1. CONCEPTOS BÁSICOS
* Las bases de datos tiene un conjunto de cuatro propiedades que se denominan ACID:
  - Atomicidad: Las transacciones son completas.
  - Consistencia: La transacción llevará a la base de datos de un estado válido a otro estado válido.
  - Aislamiento: Una transacción no puede afectar a otras.
  - Durabilidad: Una vez realiza la operación, esta persistirá.
 
 # 2. LENGUAJES DE MYSQL
 * DDL (Lenguaje de definición)
 * DML (Lenguaje de Modificación)
 * DCL (Lenguaje de control: Grant y Revoke)
 * Lenguaje de transacciones (rollback y commit)

# 3.PHPMYADMIN Y MYSQL
1. **Cambiar el nombre de tabla**. Seleccionamos la tabla y menú de "Operaciones" o con la sentencia: ALTER TABLE cliente RENAME clientes;
2. **Borrar tabla** También seleccionando la tabla y menú de "Operaciones" o con la sentencia: DROP TABLE clientes;
3. **Añadir columnas**. Se puede utilizar la sentencia: ALTER TABLE tabla ADD column columna VARCHAR(45) NULL AFTER ID;
4. **Cambiar columna**. Se puede hacer desde el menú "Estructura" o con la sentencia: ALTER TABLE tabla CHANGE column columna_new VARCHAR(140) null DEFAULT "DATO";
5. **Eliminar Columna** ALTER TABLE tabla DROP column;
6. **Clave primaria** Identifica univocamente cada fila de la tabla. Ej de sentencia: 
ALTER TABLE Customer ADD PRIMARY KEY (SID);

8. **Clave foránea**. Es el campo de una tabla que se realaciona con otra tabla. Ej: 
ALTER TABLE tu_tabla
    ADD COLUMN [definición de columna],
    ADD CONSTRAINT `fk_relacion` FOREIGN KEY (columna_recién_creada)
        REFERENCES la_otra_tabla(columnaEnLaOtraTabla);

10. **Índices** Los índices permiten acelerar las búsquedas. Pueden ser de varios tipos:
  - Index. Permiten duplicados.
  - Unique. Los valores deben ser únicos.
  - FullText. Se utiliza para las columnas de tipo texto.
  - Spatial. Para columnas de tipo spatial.
  - Primary. Índice único y solo puede haber uno por tabla.

El comando es: ALTER TABLE tabla ADD INDEX indice (campo ASC/DESC)

11. **Privilegios y usuarios** Los usuarios y privilegios se pueden dar de alta desde el menú "Privilegios"
También se puede usar el siguiente comando para crear un nuevo usuario: 
CREATE USER 'newuser'@'localhost' IDENTIFIED BY 'password'; 

Para dar permisos:
GRANT SELECT, INSERT, UPDATE, DELETE, CREATE, DROP ON basededatos.* TO 'nombre_usuario'@'localhost';

12. **Roles** Es un identificador que agrupa una sería de privilegios. Se crean con:
CREATE ROLE rol;
GRANT SELECT, INSERT, UPDATE, DELETE, CREATE, DROP ON basededatos.* TO rol;

13. **FECHAS**
- La fecha actual: curdate(), now(), localtime() y localtimestamp(). Las últimas tres, devuelven fecha y hora.
- str_to_date(texto,formatofecha): Permite convertir texto en fecha
- date(texto) se convierte la cadena a date.
- datediff(fecha1,fecha2) se obtiene el número de días entre dos fechas.
- dateadd(fecha, interval 10 day) se suma días a la fecha
- extract(day from now()) para extraer el día de la fecha actual
- date_format(fecha, formato) para formatear una fecha en un formato distinto

14. **CADENAS**
- Concat(cadena1,' ', cadena2)
- Concat_ws(' ', cadena1,cadena2) Igual que la anterior, pero el carácter separador va al inicio.
- instr(cadena,cadenaabuscar) Devuelve la posición de la cadenaabuscar dentro de cadena.

15. **CONVERSIÓN**
- Cast(campo as datetime) Para convertir un campo a formato datetime.
- Convert('20011101', date): Para convertir una cadena a una fecha

16. CIFRADO
- AES_Encypt(cadena, llave). Para encriptar
- AES_Decrypt(cadena, llave). Para desencriptar
- md5(cadena) o sha(cadena) Para encriptar.
- sha2(cadena, numero de bits). Para encriptar, pero se indica los bits para encriptar

17. OTRAS FUNCIONEO
-

