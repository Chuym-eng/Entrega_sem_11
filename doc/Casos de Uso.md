# Casos de uso 
## CU-001: Iniciar sesión 
- Actor: Usuario (Administrador, Cajero, Encargado del almacén)
- Flujo principal:
  1. Se ingresa nombre de usuario y contraseña.
  2. El sistema valida que los datos sean correctos.
  3. El sistema redirige al usuario a su respectiva interfaz (Segun rol).
- Flujo de excepcion:
  1. El sistema permite un máximo de 3 intentos de ingreso.
  2. El sistema bloquea el acceso al usuario una vez sobrepasada los 3 intentos.
## CU-002: Registrar productos 
- Actor: Administrador, Encargado del almacén.
- Flujo principal:
  1. El usuario ingresa al módulo de productos.
  2. El sistema muestra el formulario de registro.
  3. El usuario ingresa el nombre, código, descripción, precio y cantidad inicial del producto.
  4. El sistema valida los datos ingresados.
  5. El sistema registra el producto en la base de datos.
  6. El sistema muestra un mensaje de confirmación.
- Flujo de excepción:
  1. Si faltan datos obligatorios, el sistema solicita completarlos.
  2. Si el código del producto ya existe, el sistema informa que el producto está registrado.
  3. Si el precio o la cantidad son negativos, el sistema rechaza el registro.
## CU-003: Consultar productos 
- Actor: Administrador, Cajero, Encargado del almacén.
- Flujo principal:
  1. El usuario ingresa al módulo de consulta de productos.
  2. El sistema muestra los productos registrados.
  3. El usuario ingresa el nombre o código del producto que desea buscar.
  4. El sistema busca coincidencias en la base de datos.
  5. El sistema muestra la información del producto, incluyendo su precio y stock disponible.
- Flujo de excepción:
  1. Si el producto no existe, el sistema muestra un mensaje indicando que no se encontraron resultados.
  2. Si el campo de búsqueda está vacío, el sistema solicita ingresar un criterio de búsqueda.
  3. Si ocurre un error de conexión con la base de datos, el sistema informa que no se pudo completar la consulta.
## CU-004: Registrar venta 
- Actor: Cajero.
- Flujo principal:
  1. El cajero ingresa al módulo de ventas.
  2. El sistema muestra la interfaz para registrar una nueva venta.
  3. El cajero busca y selecciona los productos que desea vender.
  4. El sistema verifica que exista stock suficiente para cada producto.
  5. El sistema calcula el subtotal y el importe total de la venta.
  6. El cajero confirma la venta e ingresa los datos de pago.
  7. El sistema registra la venta y actualiza el stock de los productos.
  8. El sistema genera el comprobante de venta.
  9. El sistema muestra la confirmación de la operación.
- Flujo de excepción:
  1. Si un producto no tiene stock suficiente, el sistema informa al cajero y no permite vender una cantidad superior a la disponible.
  2. Si los datos del pago son incorrectos, el sistema solicita corregirlos.
  3. Si ocurre un error al registrar la venta, el sistema informa del problema y evita descontar el stock sin que la venta quede registrada correctamente.
## CU-005: Generar reporte de ventas
- Actor: Administrador.
- Flujo principal:
  1. El administrador ingresa al módulo de reportes.
  2. El sistema muestra los filtros disponibles para generar el reporte.
  3. El administrador selecciona el periodo de consulta.
  4. El sistema consulta las ventas registradas durante el periodo seleccionado.
  5. El sistema calcula los totales y agrupa la información correspondiente.
  6. El sistema muestra el reporte de ventas.
  7. El administrador puede exportar o imprimir el reporte.
- Flujo de excepción:
  1. Si las fechas ingresadas son inválidas, el sistema solicita corregirlas.
  2. Si no existen ventas en el periodo seleccionado, el sistema muestra un mensaje indicando que no hay información disponible.
  3. Si ocurre un error al generar o exportar el reporte, el sistema informa que la operación no pudo completarse.
## CU-006: Registrar clientes
- Actor: Cajero, Administrador.
- Flujo principal:
  1. El usuario ingresa al módulo de gestión de clientes.
  2. El sistema muestra la opción para registrar un nuevo cliente.
  3. El usuario ingresa los datos del cliente, como nombres, apellidos y teléfono.
  4. El sistema valida que los datos ingresados sean correctos.
  5. El sistema verifica que el cliente no se encuentre registrado previamente.
  6. El sistema guarda la información del cliente en la base de datos.
  7. El sistema muestra un mensaje de confirmación del registro.
- Flujo de excepción:
  1. Si faltan datos obligatorios, el sistema solicita completarlos.
  2. Si el documento de identidad ya se encuentra registrado, el sistema informa que el cliente ya existe.
  3. Si los datos ingresados no cumplen con el formato requerido, el sistema solicita corregirlos.
  4. Si ocurre un error al guardar la información, el sistema informa que no se pudo completar el registro.
