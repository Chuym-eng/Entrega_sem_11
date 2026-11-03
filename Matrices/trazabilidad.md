# Matriz de trazabilidad
| Req | Descripción | CU | Clase | Prueba | ¿Cubierto? |
|---|---|---|---|---|---|
| REQ-001 | Inicio de sesión con bloqueo tras 3 intentos fallidos y control de acceso por rol | CU-001 | CLS-Administrador, CLS-Cajero, CLS-Encargado del almacen| PRU-001 | Pendiente |
| REQ-002 | Registrar productos | CU-002 | CLS-Productos | PRU-002 | Pendiente |
| REQ-003 | Registrar clientes con nombres, apellidos, DNI (formato fijo) y teléfono | CU-006 | CLS-Cliente | PRU-003 | Pendiente |
| REQ-004 | Consultar prendas | CU-003 | CLS-Producto | PRU-004 | Pendiente |
| REQ-005 | Registrar ventas | CU-004 | CLS-Venta, CLS-DetalleVenta, CLS-Cliente, CLS-Cajero | PRU-005 | Pendiente |
| REQ-006 | Calcular el total | CU-004 | CLS-Venta, CLS-DetalleVenta | PRU-006 | Pendiente |
| REQ-007 | Descontar stock | CU-004 | CLS-Producto, CLS-DetalleVenta | PRU-007 | Pendiente |
| REQ-008 | Generar comprobante interno de venta | CU-004 | CLS-Comprobante, CLS-Venta | PRU-008 | Pendiente |
| REQ-009 | Generar reportes de ventas por rango de fechas | CU-005 | CLS-Reporte, CLS-Venta, CLS-Administrador | PRU-009 | Pendiente |
| REQ-010 | Generar reportes de inventario por prenda, talla y color | CU-007 | CLS-Reporte, CLS-Producto | PRU-010 | Pendiente |
| REQ-011 | Consultar historial de ventas por fecha | CU-008 | CLS-Venta, CLS-DetalleVenta, CLS-Comprobante, CLS-Cliente | PRU-011 | Pendiente |
| REQ-012 | Alerta cuando el stock de un producto, por talla y color, sea menor a 10 unidades | CU-004, CU-003, CU-009 | CLS-Producto | PRU-012 | Pendiente |
| REQ-013 | Registrar pago con método y monto | CU-004 | CLS-Pago, CLS-Venta| PRU-013 | Pendiente |
| REQ-014 | Registrar reabastecimiento y actualizar stock | CU-009 | CLS-Reabastecimiento, CLS-Producto, CLS-Encargado del almacén | PRU-014 | Pendiente |

**Cobertura**

- Trazabilidad requisito → caso de uso → clase: 14 de 14 (100 %)
