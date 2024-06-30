# Tarea SQL
Vista cliente-invoice.
Vemos las columnas que necesitamos desde sus tablas originales  y las unimos con JOIN:

1.- Vista de invoice_view
```
CREATE VIEW invoice_view AS
SELECT i.id, i.code, i.created_at, i.total, c.full_name
FROM invoice i
JOIN clients c ON c.id = i.client_id;

```
Captura: 
![Captura de pantalla 2024-06-30 154941](https://github.com/CarlosQ18a/Tarea_class/assets/146890782/9980ff3e-88b7-48d5-8957-58501ee0cbb9)


2.- Vista detail-product
```
CREATE VIEW detail_view AS
SELECT d.id, d.quantity, p.description ,d.price, d.quantity * d.price AS subtotal
FROM product p
JOIN detail d ON p.id = d.productid;
```
Captura:
![Captura de pantalla 2024-06-30 154620](https://github.com/CarlosQ18a/Tarea_class/assets/146890782/84b20efc-fb8a-4aa0-b8b1-fa90ebf3fb48)

