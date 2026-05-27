# 🌸 De flor en flor

Aplicación web para la gestión de una florería: agenda de pedidos, control de gastos e ingresos, directorio de clientes y análisis financiero.

## Características

### Resumen global
- Visualización en tiempo real de ventas totales (bruto), desglosadas por método de pago (efectivo, transferencia, tarjeta)
- Total de costos de envío
- Total de gastos
- Utilidad neta (Ventas − Envíos − Gastos)

### Pedidos
- Registro de pedidos con: nombre del cliente, WhatsApp, descripción del ramo y tipo de entrega
- Dos tipos de entrega: **recoge en local** o **envío a domicilio** (con costo de envío separado)
- Soporte para **dos pagos por pedido** con método de pago independiente (Efectivo, Transferencia, Tarjeta)
- Calculadora de total sugerido (arreglo + envío) en tiempo real
- Campo de fecha, hora y notas/dedicatoria
- Estados: **En espera** / **Entregado**
- Edición y eliminación de pedidos
- Enlace directo a **Google Maps** para direcciones de entrega
- Filtros por: búsqueda (nombre o WhatsApp), estado, rango de fechas

### Gastos
- Registro de gastos con concepto, categoría, monto y fecha
- Categorías disponibles: Flores e Insumos, Cuota de envíos, Gasolina, Transportes, Comida, Súper, Ahorro, Otros

### Clientes
- Directorio automático generado a partir de los pedidos registrados
- Acceso directo a **WhatsApp** de cada cliente

### Análisis
- Reporte financiero filtrable por período (ventas, envíos, gastos y utilidad)
- Gráfica de barras con balance de pagos por método (Efectivo, Transferencia, Tarjeta)
- **Respaldo por correo**: envía todos los datos en formato JSON via EmailJS
- **Importar respaldo**: carga datos desde un archivo `.json`

## Tecnologías

- HTML5 / CSS3 / JavaScript (vanilla) — sin frameworks
- [Chart.js](https://www.chartjs.org/) — gráficas
- [EmailJS](https://www.emailjs.com/) — envío de respaldo por correo
- `localStorage` — persistencia de datos en el navegador

## Uso

Abrir `index.html` directamente en el navegador. No requiere servidor ni instalación.

Los datos se guardan localmente en el navegador (`localStorage`). Para no perder información, usar la función de **Respaldo Correo** o exportar el JSON regularmente.

## Estructura de datos

Los datos se almacenan en `localStorage` con las siguientes claves:

| Clave | Contenido |
|---|---|
| `flor_v25_pedidos` | Array de pedidos |
| `flor_v25_gastos` | Array de gastos |
| `flor_v25_clientes` | Array de clientes |
