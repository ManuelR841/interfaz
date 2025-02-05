#Manuel Rogel 23210655
# 💡 Simplifica actualizaciones con `MERGE`

El operador `MERGE` en SQL Server permite combinar operaciones de `INSERT` y `UPDATE` en una sola sentencia. Esto es útil para sincronizar datos entre tablas de origen y destino.

## 📌 Ejemplo de uso:

```sql
MERGE INTO Destino AS d
USING Origen AS o
ON d.ID = o.ID
WHEN MATCHED THEN 
    UPDATE SET d.Nombre = o.Nombre, d.Edad = o.Edad
WHEN NOT MATCHED THEN 
    INSERT (ID, Nombre, Edad) VALUES (o.ID, o.Nombre, o.Edad);
```

✅ **Ventajas:**
- Reduce la complejidad del código.
- Mejora el rendimiento al minimizar transacciones separadas.
- Facilita la sincronización de datos en bases de datos grandes.

📖 Para más información, revisa la documentación oficial de SQL Server o consulta fuentes especializadas.
```

Este tip te servirá para optimizar operaciones de inserción y actualización en SQL Server. 🚀
