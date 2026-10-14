# BASE DE DATOS

## DML(Lenguaje de manipulacion de datos):

-`SELECT`: Consultar registros de la BD.

-`INSERT`: Agregar datos a la BD.

-`UPDATE`: Actualizar o Modificar valores de los campos y registros.

-`DELETE`: Eliminar registros de una tabla.

## CLAUSULAS

-`FROM`:Especificar la tabla que va a ser utilizada.

-`WHERE`:Especifica condiciones que deben reunir los registros que se van a seleccionar.

-`GROUP BY`:Separar los registros seleccionados en grupos especificos.

-`HAVING`:Expresa la condicion que debe satisfacer cada grupo.

-`ORDER BY`:Ordena los registros seleccionados de acuerdo con un orden especifico.

## OPERADORES LOGICOS

- `AND` lógico: Ambos lados de la condicion son verdaderos.
- `OR` lógico: Algunos de los lados de la condicion sea verdadera.
- `NOT` -> Exactamente lo contrario.

##  OPERADORES DE COMPARACIÓN

- `<` Menor que
- `>` Mayor que
- `<>` Distinto de
- `<=` Menor o igual
- `>=` Mayor o igual

---

##  BETWEEN

Comprueba si un valor está dentro de un rango inclusivo:

```sql
SELECT * FROM Products
WHERE Price BETWEEN 10 AND 20;
```

---

##  LIKE

Compara cadenas de texto usando comodines como `%` o `_`.

```sql
SELECT * FROM Customers
WHERE CustomerName LIKE 'a%';
```

---

##  IN

Especificar registros de una base de datos.

```sql
SELECT nombre_columna
FROM nombre_tabla
WHERE nombre_columna IN (valor1, valor2, valor3);
```

---

##  OTROS VALORES DE COMPARACIÓN

- `NOT BETWEEN`: Comprueba si un valor está fuera de un rango.
- `NOT IN`: Comprueba que el valor no esté en la lista.
- `NOT LIKE`: Inverso de LIKE.
- `IS NULL`: Comprueba si un valor es nulo.
- `IS NOT NULL`: Comprueba si un valor no es nulo.

---

##  FUNCIONES DE AGREGADO

Toman múltiples valores de una columna después de agruparlos y devuelven un único valor resumido.

### COUNT()

Cuenta el número total de filas o valores no nulos.

```sql
SELECT nombre_columna
FROM nombre_tabla
WHERE nombre_columna IN (valor1, valor2, valor3);
```

### SUM()

Suma todos los valores de una columna numérica.

```sql
SELECT SUM(Quantity)
FROM OrderDetails;
```

### AVG()

Calcula el promedio (media aritmética) de los valores.

```sql
SELECT AVG(Price)
FROM Products;
```

### MAX()

Encuentra el valor máximo (el más alto) de la columna.

```sql
SELECT MAX(Price)
FROM Products;
```

### MIN()

Encuentra el valor mínimo (el más bajo) de la columna.

```sql
SELECT MIN(Price)
FROM Products;
```

--------------------------------------------------------------
## INSERTAR DATOS

```sql
CREATE TABLE(
    id_estudiante = int  PRIMARY KEY AUTO_INCREMENT ,
    nombre = varchar("55"),
    edad = int not null
    );

INSERT INTO NombreTabla VALUES(1,"santiago",10);
INSERT INTO NombreTabla VALUES (null, "santiago", 10);
```

## ACTUALIZAR DATOS

```sql
UPDATE NombreTabla SET nombre = "Santiago" WHERE id_estudiante = 1;
```

```sql
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;

```
SET: Un [SET] es un objeto de cadena que puede tener cero o más valores, cada uno de los cuales debe elegirse de una lista de valores permitidos especificada al crear la tabla. [SET]. Los valores de columna que constan de varios miembros de conjunto se especifican con miembros separados por comas ( ,). Como consecuencia, [SET] los valores de los miembros no deben contener comas.

Por ejemplo, una columna especificada como SET('one', 'two') NOT NULL , puede tener cualquiera de estos valores:
-------
''
'one'
'two'
'one,two'
-------

```sql
CREATE TABLE usuarios (
    id INT,
    idiomas SET('ingles', 'español', 'frances') NOT NULL
);

```

Sentencia SET (para variables)

Es un comando utilizado para asignar un valor a una variable de usuario o modificar una variable de configuración del sistema durante una sesión.
- Variables de usuario: Se usa para guardar un valor temporal en una variable con @.

```sql
SET @mi_variable = 100;
```

Variables del sistema: 

Se usa para cambiar parámetros de configuración de MySQL (por ejemplo, el modo SQL o el tamaño del búfer).

```sql
SET NAMES 'utf8mb4';
SET GLOBAL max_connections = 500;
```
