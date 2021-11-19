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

# 3.PHPMYADMIN
1. **Cambiar el nombre de tabla**. Seleccionamos la tabla y menú de "Operaciones" o con la sentencia: ALTER TABLE cliente RENAME clientes;
2. **Borrar tabla** También seleccionando la tabla y menú de "Operaciones" o con la sentencia: DROP TABLE clientes;
3. **Añadir columnas**. Se puede utilizar la sentencia: ALTER TABLE tabla ADD column columna VARCHAR(45) NULL AFTER ID;
4. **Cambiar columna**. Se puede hacer desde el menú "Estructura" o con la sentencia: ALTER TABLE tabla CHANGE column columna_new VARCHAR(140) null DEFAULT "DATO";
5. **Eliminar Columna** ALTER TABLE tabla DROP column;
6. **Índices** Los índices permiten acelerar las búsquedas. Pueden ser de varios tipos:
  - Index. Permiten duplicados.
  - Unique. Los valores deben ser únicos.
  - FullText. Se utiliza para las columnas de tipo texto.
  - Spacial. Para columnas de tipo spacial.
  - Primary. Índice único y solo puede haber uno por tabla.

El comando es: ALTER TABLE tabla ADD INDEX indice (campo ASC/DESC)

