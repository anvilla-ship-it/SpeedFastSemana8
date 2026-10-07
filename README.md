# SpeedFast

Sistema de gestión de repartidores, pedidos y entregas desarrollado para la empresa SpeedFast.

## Tecnologías utilizadas

* Java
* IntelliJ IDEA
* MySQL
* JDBC
* Java Swing

## Descripción

La aplicación permite gestionar información de repartidores, pedidos y entregas mediante una interfaz gráfica conectada a una base de datos MySQL.

El sistema implementa operaciones CRUD:

* Crear registros.
* Consultar registros.
* Actualizar registros.
* Eliminar registros.

## Estructura del proyecto

```text
SpeedFast
├── src
│   ├── conexion
│   │   └── ConexionDB.java
│   ├── modelo
│   │   ├── Repartidor.java
│   │   ├── Pedido.java
│   │   └── Entrega.java
│   ├── dao
│   │   ├── RepartidorDAO.java
│   │   ├── PedidoDAO.java
│   │   └── EntregaDAO.java
│   ├── vista
│   │   └── VentanaPrincipal.java
│   └── main
│       └── Main.java
│
├── database
│   └── speedfast.sql
│
└── README.md
```

## Modelo de datos

La base de datos utilizada es:

`speedfast`

Tablas:

* `repartidores`
* `pedidos`
* `entregas`

Las relaciones entre las tablas se realizan mediante claves foráneas entre pedidos, repartidores y entregas.

## Funcionalidades

### Gestión de repartidores

* Registrar repartidores.
* Listar repartidores.
* Actualizar repartidores.
* Eliminar repartidores.

### Gestión de pedidos

* Registrar pedidos.
* Listar pedidos.
* Actualizar pedidos.
* Eliminar pedidos.
* Seleccionar tipo de pedido:

  * COMIDA
  * ENCOMIENDA
  * EXPRESS
* Seleccionar estado:

  * PENDIENTE
  * EN_REPARTO
  * ENTREGADO

### Gestión de entregas

* Registrar entregas.
* Listar entregas.
* Actualizar entregas.
* Eliminar entregas.
* Asociar un pedido con un repartidor.
* Registrar fecha y hora de la entrega.

## JDBC

La conexión con MySQL se realiza mediante la clase `ConexionDB`.

Las clases DAO utilizan:

* `PreparedStatement`
* `ResultSet`
* Manejo de excepciones SQL
* Cierre de recursos mediante `try-with-resources`

## Interfaz gráfica

La aplicación utiliza Java Swing y componentes como:

* `JFrame`
* `JPanel`
* `JTable`
* `JTextField`
* `JComboBox`
* `JButton`
* `JOptionPane`

## Base de datos

El script para crear la base de datos y las tablas se encuentra en:

`database/speedfast.sql`

## Ejecución

1. Tener instalado MySQL Server.
2. Crear la base de datos utilizando `database/speedfast.sql`.
3. Configurar el usuario y contraseña de MySQL en `ConexionDB.java`.
4. Tener agregado MySQL Connector/J al proyecto.
5. Ejecutar la clase:

`main.Main`

La aplicación abrirá la ventana principal de SpeedFast.

## Autor

Antonia Villa
