# Calculadora de proyección de ventas

Herramienta interactiva para presentar propuestas a clientes de la agencia: a partir de los datos actuales de una marca (facturación, gasto en ads, utilidad bruta y ticket promedio) calcula el escenario actual, el nuevo cobro propuesto (iguala + % sobre venta) y proyecciones de escalamiento.

## Cómo usarla

Abre `index.html` en cualquier navegador. No necesita servidor ni dependencias.

1. **Datos actuales del cliente** — facturación, ads, utilidad bruta (con envíos incluidos) y ticket promedio del mes. Indica si la utilidad ya trae descontado el fee fijo actual.
2. **Escenario actual** — margen real, ROAS, % de gasto en ads, pedidos/mes, utilidad del cliente y lo que paga hoy (total, por pedido y % del ticket).
3. **Nuevo cobro propuesto** — nueva iguala mensual + % sobre venta (cobro nuevo, siempre se descuenta aparte).
4. **¿Qué pasaría si vendemos…?** — escribe una meta de facturación y ajusta el % de inversión en ads; muestra inversión, pedidos, pago a la agencia y el contraste "quedarte como hoy" vs "con la propuesta" con la ganancia extra mensual.
5. **Otras proyecciones** — tabla a 1.25×, 1.5×, 2×, 2.5× y 3× de la facturación base (siempre parte de la base hacia arriba), con la fila del escenario manual resaltada.

## Supuestos del modelo

- Al escalar se mantiene el margen sobre producto (antes de ads) calculado de los datos base.
- El gasto en ads escala con el % del slider (por defecto, el % actual del cliente).
- La iguala es fija: no crece con la venta.
- "Ganas extra" compara contra la utilidad de hoy con el esquema actual.
