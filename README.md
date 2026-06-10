# Proyección de crecimiento (calculadora por cliente)

Herramienta interactiva para presentar propuestas a clientes de la agencia: a partir de los datos actuales de una marca (facturación, gasto en ads, utilidad bruta y ticket promedio) muestra el escenario de hoy, el nuevo cobro propuesto (iguala + % sobre venta) y proyecciones de escalamiento en lenguaje simple para el cliente.

## Cómo usarla

Abre `index.html` en cualquier navegador. No necesita servidor ni dependencias.

- **Panel izquierdo** — información financiera del cliente en dos modos (pestañas arriba del panel):
  - **Triple Whale**: cuando hay datos directos — facturación, gasto en ads y utilidad bruta (con envíos incluidos; indica si ya trae descontado el fee).
  - **Unitaria**: cuando no hay Triple Whale — ticket promedio (Shopify), pedidos al mes, gasto en ads, COGS por pedido, envío por pedido (si lo absorbe la tienda) y % de pasarela de pagos. La calculadora arma la facturación, el CPA y la utilidad bruta automáticamente (se muestran en la cajita de "Con estos datos…").
  - **Gastos fijos (opcional)**: si se llenan, aparece el switch para proyectar sobre utilidad neta en lugar de bruta; los gastos fijos se mantienen constantes al escalar. El enfoque por defecto sigue siendo utilidad bruta.
  - Abajo va el nuevo cobro propuesto (nueva iguala + % sobre venta).
- **Hoy** — desglose actual: facturación, ads (% de la venta), ROAS/pedidos/ticket, lo que paga hoy (por pedido y % del ticket) y su utilidad con margen real.
- **¿Qué pasaría si vendemos…?** — slider de meta de venta con presets (×1.25 a ×3) y slider de % de gasto en ads (arranca en el % actual). Muestra las dos métricas grandes (lo que nos pagaría / su utilidad), el desglose, la barra de distribución de cada peso vendido y el contraste "quedarte como hoy vs tomar la propuesta".
- **Otras proyecciones** — tabla a ×1.25, ×1.5, ×2, ×2.5 y ×3 de la facturación base; la fila azul es la meta seleccionada.

## Varios clientes (discreto)

Cada cliente tiene su propia pestaña con datos financieros personalizados, pensada para que no se vea a simple vista durante una presentación:

- El selector es el **punto tenue en la esquina superior derecha** — casi invisible hasta pasar el mouse. Al hacer clic se abre el menú de clientes, "+ Nuevo cliente" y eliminar.
- También puedes abrir directo a un cliente con el hash de la URL: `index.html#koneli`.
- Un cliente nuevo se crea copiando los valores del actual; todos los cambios se guardan automáticamente por cliente en el navegador (localStorage).

## Supuestos del modelo

- Al escalar se mantiene el margen sobre producto (antes de ads) calculado de los datos base.
- El gasto en ads escala con el % del slider (por defecto, el % actual del cliente).
- La iguala es fija: no crece con la venta. El % sobre venta es cobro nuevo y se descuenta aparte en todos los escenarios.
- "Ganas extra" compara contra la utilidad de hoy con el esquema actual.
