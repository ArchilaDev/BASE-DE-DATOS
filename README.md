
# BASE DE DATOS

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
