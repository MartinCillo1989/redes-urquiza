# Diagrama de Entidades

## Entidades

### Cliente
- **ClienteID** (PK)
- Nombre
- Email
- Teléfono
- Dirección
- FechaRegistro

### Pedido
- **PedidoID** (PK)
- FechaPedido
- Total
- Estado
- ClienteID (FK)

### Producto
- **ProductoID** (PK)
- Nombre
- Descripción
- Precio
- Categoría
- FechaRegistro

### Inventario
- **InventarioID** (PK)
- ProductoID (FK)
- CantidadDisponible
- CantidadReservada
- ÚltimaActualización

## Relaciones

- **Cliente** 1 ---- N **Pedido**  
  (Un cliente puede realizar múltiples pedidos.)

- **Pedido** N ---- 1 **Producto**  
  (Un pedido puede incluir múltiples productos.)

- **Producto** 1 ---- 1 **Inventario**  
  (Cada producto tiene un registro en inventario para su gestión.)

